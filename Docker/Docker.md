## Docker

도커(Docker)는 리눅스의 응용 프로그램들을 소프트웨어 컨테이너 안에 배치시키는 일을 자동화하는 오픈 소스 프로젝트이다. 

도커 웹 페이지의 기능을 인용하면 다음과 같다.

서버에서 이야기하는 컨테이너도 이와 비슷한데 다양한 프로그램, 실행환경을 컨테이너로 추상화하고 동일한 인터페이스를 제공하여 프로그램의 배포 및 관리를 단순하게 해줍니다.

백엔드 프로그램, 데이터베이스 서버, 메시지 큐등 어떤 프로그램도 컨테이너로 추상화할 수 있고 조립 PC, AWS, Azure, Google cloud 등 어디에서든 실행할 수 있습니다.

![vm-vs-docker](https://user-images.githubusercontent.com/48753593/64954349-471e4f80-d8c0-11e9-8968-e8234d4962cc.png)

<img width="1162" alt="스크린샷 2019-09-16 오후 8 51 32" src="https://user-images.githubusercontent.com/48753593/64955886-4edff300-d8c4-11e9-9172-2b03832e8ce4.png">

#### 서버 분산 처리 용이

![1_344Hiafp_XQXYVmuTOQzHA](https://user-images.githubusercontent.com/48753593/64953288-6f587f00-d8bd-11e9-89bb-15e47b5b4f95.png)

<hr />

![docker1](https://user-images.githubusercontent.com/48753593/64953787-b7c46c80-d8be-11e9-8b9e-cdeda84225dd.jpg)


<hr />

### Docker-Compose 
  컨테이너를 Stack-Service-Task 라는 세가지 가상 계층으로 구분해 관리한다.



혹시, 특이한 부분을 찾으셨나요? 버전정보가 클라이언트와 서버로 나뉘어져 있습니다. 도커는 하나의 실행파일이지만 실제로 클라이언트와 서버역할을 각각 할 수 있습니다. 도커 커맨드를 입력하면 도커 클라이언트가 도커 서버로 명령을 전송하고 결과를 받아 터미널에 출력해 줍니다.

![docker-host](https://user-images.githubusercontent.com/48753593/64958176-71c0d600-d8c9-11e9-84cf-63edb4a367ff.png)
