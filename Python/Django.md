### Django

1.	명세 만들기 ( 프로젝트 목표를 상세히 다루고, 기능과 외형, 사용자 인터페이스를 설명하는 문서 )

2.	프로젝트 폴더 만들기 ( 여기선 learning_log )

3.	가상 환경 만들기
    + python3 -m venv 11_env
    + 위 명령어가 실행되지 않을 경우virtualenv 설치하기 (pip3 install --user virtualenv)
    + cd learning_log$ virtualenv 11_env
    
4.	가상 환경 활성화 하기
    +	learning_log$ source 11_env/bin/activate
    
5.	장고 설치하기
    +	(11_env) learning_log$ pip3 install Django
    
6.	장고에서 프로젝트 만들기
    + django-admin.py startproject learning_log .
    
7.	DB 만들기
    + python3 manage.py migrate
    + SQlite 는 단 하나의 파일만 사용하는 데이터 베이스. 단순한 애플리케이션에 이상적 이다


<img width="1100" alt="스크린샷 2019-09-12 오후 4 18 39" src="https://user-images.githubusercontent.com/48753593/64762962-09e15700-d57a-11e9-8ed5-b1edd6a24710.png">

<img width="624" alt="스크린샷 2019-09-12 오후 4 25 51" src="https://user-images.githubusercontent.com/48753593/64762961-0948c080-d57a-11e9-92e0-ff2299b6811b.png">

<img width="1242" alt="스크린샷 2019-09-12 오후 4 25 55" src="https://user-images.githubusercontent.com/48753593/64762960-0948c080-d57a-11e9-9505-449331d0ddb8.png">