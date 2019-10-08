### Airflow

Airflow 를 통해 workflow를 분산처리 할 수 있다.

interval 하게 원하는 시간대에 airflow 내에 구현된 코드를 실행 시킬 수 있으며, 주기적 업데이트가 필요한 부분에 경우 활용할 수 있다.

현재는 Personalize API를 Pythonoperator 를 통해 airflow 내의 함수를 생성, 실행 해주는 형태로 airflow를 활용하고 있다.
