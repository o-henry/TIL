# Node.js

<img width="974" alt="스크린샷 2019-10-06 오후 3 11 43" src="https://user-images.githubusercontent.com/48753593/66265110-ad591b00-e84b-11e9-9c56-463992e883be.png">


<hr />

##### URL Module
    주소 정보가 담긴 주소 문자열을 url 모듈을 사용하여 URL 객체로 만들거나 또는 URL 객체에서 일반 문자열로 변환하는 일을 합니다.
    url 모듈을 통해 주소 문자열을 객체로 만들면 문자열 안에 있던 정보를 나누어 객체의 속성으로 보관 합니다.
    따라서 요청 프로토콜이 http 인지 https 인지를 구별하거나 요청 파라미터를 확인하고 싶다면 url 객체가 갖고 있는 속성 값을 확인하면 됩니다.
    
    대표적인 url 모듈의 주요 메서드
      parse() - 주소 문자열을 파싱하여 URL 객체를 만들어 줍니다.
      format() - URL 객체를 주소 문자열로 반환 합니다.
      
      ```js
        var url = require('url');
      ```
