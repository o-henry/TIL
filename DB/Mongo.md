
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
