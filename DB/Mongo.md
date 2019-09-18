## Mongo DB
    mongo db는 NOSQL
    고정 schema가 존재하지 않는다
    이러한 특성을 동적 스키마라 한다. 이것은 collection 내의 document가 각자의 고유한 field를 가질 수 있다는 것을 의미한다.

## docker 터미널에서 mongo DB 설정
  
  ### *docker pull mongo*
  
  <img width="485" alt="스크린샷 2019-09-18 오후 9 30 19" src="https://user-images.githubusercontent.com/48753593/65148624-8e8d1300-da5b-11e9-9fc8-62df64ac1e10.png">
    
  ### *docker images*
    
<img width="479" alt="스크린샷 2019-09-18 오후 9 30 25" src="https://user-images.githubusercontent.com/48753593/65148625-8e8d1300-da5b-11e9-8caf-a1a9023ea337.png">

  ### *docker run --name (mongodb) mongo*
  
  <img width="588" alt="스크린샷 2019-09-18 오후 9 32 37" src="https://user-images.githubusercontent.com/48753593/65148843-e7f54200-da5b-11e9-9a15-aef909b83254.png">

  ### *docker run -d -p 27017-27019:27017-27019 --name (mongodb) mongo*
    aleredy error => 
    docker ps -a ( 실행 중인 상태 확인 ) => 
    docker stop mongodb => 
    docker rm mongodb
    
  <img width="591" alt="스크린샷 2019-09-18 오후 9 35 33" src="https://user-images.githubusercontent.com/48753593/65148995-43273480-da5c-11e9-8859-97e79e2408cd.png">

  
  <img width="591" alt="스크린샷 2019-09-18 오후 9 34 33" src="https://user-images.githubusercontent.com/48753593/65148936-1f63ee80-da5c-11e9-8857-89913673fe7c.png">

  ### *docker exec -it (mongodb) bash
  <img width="579" alt="스크린샷 2019-09-18 오후 9 35 58" src="https://user-images.githubusercontent.com/48753593/65149043-5cc87c00-da5c-11e9-97c7-c7955c6c8b54.png">


## mongo shell - 명령어 

  ### mongo
    mongo 내부.
  <img width="584" alt="스크린샷 2019-09-18 오후 9 38 02" src="https://user-images.githubusercontent.com/48753593/65149201-a2854480-da5c-11e9-85ac-96fce7b18025.png">
  
<img width="594" alt="스크린샷 2019-09-18 오후 9 38 16" src="https://user-images.githubusercontent.com/48753593/65149203-a31ddb00-da5c-11e9-92d1-e89dc02a0fda.png">

  ### use (db name) 
     use는 현재 존재하지않는 dbname 도 사용 가능하다
   <img width="180" alt="스크린샷 2019-09-18 오후 9 39 17" src="https://user-images.githubusercontent.com/48753593/65149299-cfd1f280-da5c-11e9-98d1-58e95b069083.png">
   <img width="186" alt="스크린샷 2019-09-18 오후 9 39 30" src="https://user-images.githubusercontent.com/48753593/65149298-cfd1f280-da5c-11e9-8bb3-a1a78e4d194f.png">

<img width="157" alt="스크린샷 2019-09-18 오후 9 42 35" src="https://user-images.githubusercontent.com/48753593/65149553-40790f00-da5d-11e9-86a5-ad27efdf7c25.png">

<img width="610" alt="스크린샷 2019-09-18 오후 9 42 29" src="https://user-images.githubusercontent.com/48753593/65149552-3fe07880-da5d-11e9-90dc-74b29ae15371.png">


