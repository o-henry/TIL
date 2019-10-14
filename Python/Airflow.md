### Airflow

Airflow 를 통해 workflow를 분산처리 할 수 있다.

interval 하게 원하는 시간대에 airflow 내에 구현된 코드를 실행 시킬 수 있으며, 주기적 업데이트가 필요한 부분에 경우 활용할 수 있다.

(현재는 Personalize API를 Pythonoperator 를 통해 airflow 내의 함수를 생성, 실행 해주는 형태로 airflow를 활용하고 있다.)



#### Airflow 활용
```
airflow scheduler 는
파이썬을 기반으로 하는 작업 흐름을 실행, 관리하는 오픈소스 플랫폼 입니다.
DAG -> 여러 개의 테스크가 합쳐져서 동작하는 하나의 데이터 워크 플로우


airflow 구현중 어려웠던 점

*동기적으로 처리해야할 부분 
  airflow는 주어진 task를 성공 / 실패 유무로 판단.
  airflow task 코드가 실행이 되면 성공으로 간주 해 버림.
  문제는 우리는 Personalize 데이터가 생성된 후에 다음 task를 실행해야 한다는 점. 
  => 정해진 5~10분마다 진행상황을 확인해주는 코드를 작성.
  Personalize에서 응답을 확인할수 있는 API를 활용 분기를 통해서 문제를 해결

*새로 생성되는 값에 대한 처리.
  상위 Task 에서 생성되는 데이터 를 토대로 다음 Task를 생성해야 하는데 airflow 내에서의 변수 전달 필요.
  => x_com 사용

*airflow 테스트 에 소요되는 시간
  airflow로 자동화 로직(데이터 워크플로우)을 만들때 결과를 기다리는데 3시간 가량 소요. 디버깅의 어려움
  => airflow 가 task가 에러없이 실행되면 success 되는 점을 이용, 상위 task 에서 success 가 되게하고 하위 task 원하는 데이터를 받아오는지 테스트 해서 소   요시간을 줄임

```
