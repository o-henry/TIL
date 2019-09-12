
### HTTP Protocol

웹에서 브라우저와 서버간에 데이터를 주고받기 위한 방식.

### HTTP Request & HTTP Response
HTTP 프로토콜로 데이터를 주고받기 위해서는 요청(Request)을 보내고 응답(Response)을 받아야 합니다.

### URL 
서버에 자원을 요청하기 위해 입력하는 영문 주소.
![URL 구조](https://joshua1988.github.io/images/posts/web/http/url-structure.png )
### HTTP 요청 메서드
URL을 이용하면 서버에 특정 데이터를 요청할 수 있다. 
요청한 데이터에 특정 동작을 수행하고 싶으면 HTTP 요청 메서드를 이용한다.


>GET : 존재하는 자원에 대한 요청

>POST : 새로운 자원을 생성

>PUT : 존재하는 자원에 대한 변경

>DELETE : 존재하는 자원에 대한 삭제

>HEAD : 서버 헤더 정보를 획득. GET과 비슷하나 Response Body를 반환하지 않음

>OPTIONS : 서버 옵션들을 확인하기 위한 요청. CORS에서 사용

### HTTP 상태 코드
HTTP Status Code는 서버에서 설정해주는 응답(Response) 정보.
이 상태 코드로 에러 처리를 할 수 있다.

![structure](https://joshua1988.github.io/images/posts/web/http/http-full-structure.png)

### HTTP GET / POST Method

#### GET Method
GET is used to request data from a specified resource.
GET is one of the most common HTTP methods.

#### POST Method
POST is used to send data to a server to create/update a resource.


