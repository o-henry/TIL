### Django
#### 장고 란?
    파이썬으로 만들어진 웹 프레임워크 (web application framework)
    쉽고 빠르게 웹사이트를 개발할 수 있도록 돕는 구성요소로 이루어진 웹 프레임워크.
    웹사이트를 구축할 때, 비슷한 유형의 요소들이 항상 필요합니다.
    회원가입, 로그인, 로그아웃과 같이 사용자 인증을 다루는 방법이나 웹사이트의 관리자 패널, 폼, 파일 업로드와 같은 것들 말이지요.
    그런데 정말 다행이게도, 오래전에 어떤 웹 개발자들이 새로운 웹 사이트를 개발할 때 서로 비슷한 문제들에 직면한다는 것을 깨달았습니다.
    그래서 팀을 조직했고요. 바로 사용할 수 있는 구성요소들을 갖춘 여러 프레임워크를 만들었답니다. 
    장고도 그중에 하나인 거죠. 다시 발명해야 하는 문제로부터 해방감을 주고요. 새로운 웹사이트를 개발할 때 뒤따르는 간접비용의 부담을 덜어준답니다

<hr />

#### Setting

1.	명세 만들기 ( 프로젝트 목표를 상세히 다루고, 기능과 외형, 사용자 인터페이스를 설명하는 문서 )

2.	프로젝트 폴더 만들기 ( 여기선 learning_log )

3.	가상 환경 만들기 

    > *Virtualenv는 프로젝트 기초 전부를 Python/Django와 분리해줍니다*  
    > *웹사이트가 변경되어도 개발 중인 것에 영향을 미치지 않는다는 것입니다*
    
    ```
     python3 -m venv 11_env
     위 명령어가 실행되지 않을 경우 virtualenv 설치하기 (pip3 install --user virtualenv)
     cd learning_log$ virtualenv 11_env
    ```
    
4.	가상 환경 활성화 하기
    ```
    learning_log$ source 11_env/bin/activate
    ```
5.  pip 최신 버전 확인 하기

     ```
    (11_env) ~$ python3 -m pip install --upgrade pip
      ```
   
    
6.	장고 설치하기
    ```
     (11_env) learning_log$ pip3 install Django
    ```
    
7.	장고에서 프로젝트 만들기
    ```
     django-admin.py startproject learning_log .
    ```
    
8.	DB 만들기
    ```
    python3 manage.py migrate
    SQlite 는 단 하나의 파일만 사용하는 데이터 베이스. 단순한 애플리케이션에 이상적 이다
    ```
    
9. 프로젝트 보기
    ```
     python3 manage.py runserver
     ```
    

<img width="1100" alt="스크린샷 2019-09-12 오후 4 18 39" src="https://user-images.githubusercontent.com/48753593/64762962-09e15700-d57a-11e9-8ed5-b1edd6a24710.png">

<img width="624" alt="스크린샷 2019-09-12 오후 4 25 51" src="https://user-images.githubusercontent.com/48753593/64762961-0948c080-d57a-11e9-92e0-ff2299b6811b.png">

<img width="1242" alt="스크린샷 2019-09-12 오후 4 25 55" src="https://user-images.githubusercontent.com/48753593/64762960-0948c080-d57a-11e9-9505-449331d0ddb8.png">

 10. 앱 시작
    + startapp appname 명령어는 장고가 앱을 만드는데 필요한 기반 구조를 만들게 합니다.
    <img width="680" alt="스크린샷 2019-09-12 오후 4 38 15" src="https://user-images.githubusercontent.com/48753593/64763884-e3242000-d57b-11e9-99b7-e56269817791.png">


### Structure 
<img width="1000" alt="스크린샷 2019-09-12 오후 8 26 31" src="https://user-images.githubusercontent.com/48753593/64780542-a1a36d00-d59b-11e9-9e0b-d46fe43d9ea8.png">

### flow
![Django-Request-Response-Call-Cycle](https://user-images.githubusercontent.com/48753593/64783557-0910eb00-d5a3-11e9-93bb-c56c28cc895e.png)

### Make Prjoect

7. django-admin.py startproject learning_log . 을 하면, 아래와 같은 디렉토리 구조가 보입니다.
    
    ```
    djangogirls
    ├───manage.py
    └───mysite
        settings.py
        urls.py
        wsgi.py
        __init__.py
    ```

manage.py 는 사이트 관리를 도와주는 역할을 하는 스크립트 입니다. 이 스크립트로 컴퓨터에서 웹 서버를 시작할 수 있습니다.

settings.py 는 웹사이트 설정이 있는 파일.

urls.py 는 urlresolver가 사용하는 패턴 목록을 포함하고 있습니다.


<hr />

> https://tutorial.djangogirls.org/ko/django_start_project/

<img width="1255" alt="스크린샷 2019-09-14 오후 3 22 14" src="https://user-images.githubusercontent.com/48753593/64904717-da148980-d708-11e9-8bcf-479d3cfef0f4.png">

### View

    MVC Framework에서 말하는 Controller와 비슷한 역활
    View는 필요한 데이타를 모델 (혹은 외부)에서 가져와서 적절히 가공하여 웹 페이지 결과를 만들도록 컨트롤하는 역활
    View들은 Django App 안의 views.py 라는 파일에 정의하게 되는데, 각 함수가 하나의 View를 정의한다.
    
### Model
    Model 작성
    DB를 획기적으로 컨트롤하는 방법을 알아봅시다.
    Django Model은 Django ORM(Object-relational mapping)에서 기본적으로 제공하는 기능 중 하나 입니다. 
    데이터베이스를 “객체”의 형태로 사용할 수 있도록 도와줍니다.
    Django 모델은 class로 정의하게 되는데, 보통 정의된 모델은 그와 대응하는 DB의 한 테이블, 
    모델의 인스턴스는 해당 테이블의 한 행과 매핑됩니다. 이제 Post 모델을 작성해 봅시다.
    
### MTV 패턴

    Model은 데이타를 표현하는데 사용되며, 하나의 모델 클래스는 DB에서 하나의 테이블로 표현된다
    View는 Model로부터 데이터를 읽거나 저장할 수 있으며, Template를 호출하여 데이터를 UI 상에 표현하도록 할 수 있다.
    Template는 HTML을 생성하는 것을 목적으로 하는 컴포넌트 이다.
    


<hr />

#### 가상 머신 - 프로젝트 생성 - App 생성

<hr />

### 프로젝트 대 앱
    프로젝트와 앱은 무엇이 다를까요? 앱은 특정한 기능(블로그나 공공 기록물을 위한 데이터베이스나, 간단한 설문조사 앱)을 수행하는 웹 어플리케이션을 말합니다. 프로젝트는 이런 특정 웹 사이트를 위한 앱들과 각 설정들을 한데 묶어놓은 것입니다. 프로젝트는 다수의 앱을 포함할 수 있고, 앱은 다수의 프로젝트에 포함될 수 있습니다.
