# AWS Personalize

##### *초기 모델 Trend*

 인기 있는 상품 / 공통 성향이 있는 사람들 / 쓰지 않던 상품 제안

##### *개인화*

 룰 기반 추천 ( 인기 있는 상품 카운트 )
 Collaborative Filtering , Matrix Factorization
 Session 기반 추천 및 Deep Learning

##### *Personalize*

 API를 통해서 Service에 적용 가능하다.
 Data 준비에 대해서만 Personalize 사용 고객이 준비해주면 된다.

##### *데이터 파이프라인*

 주안점: 사용자 중심 , ITEM 중심 , 사용자 - ITEM Interaction 이에 따라서 schema 지정, 이에 따라 Data Format 을 구성 및 준비

 데이터를 S3 업로드 -> API 를 통해 Personalize 연동 -> 알고리즘 선택을 통해 트레이닝 (AutoML 최적화)
 
 배치성 / real-time
 
##### *Data Formatting 과 형식만 잘 잡혔다면 데이터를 올리고 난후 모델 생성은 매우 간단하다*

사람들이 클릭을 했을때 특정 상품에 대해서 관심을 최근에 얼마나 갖고 있었는가를 가지고 이후상품에 대한 추천을 하는 모델



<hr />

<img width="618" alt="스크린샷 2019-09-13 오후 6 20 55" src="https://user-images.githubusercontent.com/48753593/64904722-df71d400-d708-11e9-9f6e-cbd902d68fcc.png">
<img width="482" alt="스크린샷 2019-09-13 오후 6 21 08" src="https://user-images.githubusercontent.com/48753593/64904723-e0a30100-d708-11e9-8f38-a03dcbee971d.png">
<img width="1014" alt="스크린샷 2019-09-15 오후 3 39 52" src="https://user-images.githubusercontent.com/48753593/64919359-de15d980-d7e4-11e9-8510-03138076ef5c.png">
<img width="1002" alt="스크린샷 2019-09-15 오후 3 43 12" src="https://user-images.githubusercontent.com/48753593/64919360-df470680-d7e4-11e9-9b1b-2abda0ba8e53.png">
<img width="728" alt="스크린샷 2019-09-15 오후 3 46 16" src="https://user-images.githubusercontent.com/48753593/64919361-e0783380-d7e4-11e9-91ba-3fd73098c666.png">
<img width="990" alt="스크린샷 2019-09-15 오후 3 47 45" src="https://user-images.githubusercontent.com/48753593/64919362-e110ca00-d7e4-11e9-8c8e-fccfbc284241.png">
<img width="715" alt="스크린샷 2019-09-15 오후 3 50 56" src="https://user-images.githubusercontent.com/48753593/64919363-e66e1480-d7e4-11e9-9ad2-5a18b3a6ef53.png">
<img width="1003" alt="스크린샷 2019-09-15 오후 3 53 22" src="https://user-images.githubusercontent.com/48753593/64919365-e79f4180-d7e4-11e9-8a51-c3aecbad9155.png">
<img width="1004" alt="스크린샷 2019-09-15 오후 3 54 47" src="https://user-images.githubusercontent.com/48753593/64919367-ea9a3200-d7e4-11e9-8583-472fcc09f815.png">
<img width="976" alt="스크린샷 2019-09-15 오후 3 54 52" src="https://user-images.githubusercontent.com/48753593/64919370-fede2f00-d7e4-11e9-8c8c-d9e566e89138.png">
<img width="984" alt="스크린샷 2019-09-15 오후 3 56 51" src="https://user-images.githubusercontent.com/48753593/64919371-ff76c580-d7e4-11e9-89b4-b60553aeed31.png">
<img width="974" alt="스크린샷 2019-09-15 오후 3 57 55" src="https://user-images.githubusercontent.com/48753593/64919372-043b7980-d7e5-11e9-8ec9-515d03ba23a3.png">
<img width="985" alt="스크린샷 2019-09-15 오후 3 59 18" src="https://user-images.githubusercontent.com/48753593/64919373-043b7980-d7e5-11e9-93df-ebba5ea021ce.png">
<img width="996" alt="스크린샷 2019-09-15 오후 3 59 47" src="https://user-images.githubusercontent.com/48753593/64919374-043b7980-d7e5-11e9-9313-c4857c2a78ac.png">
<img width="993" alt="스크린샷 2019-09-15 오후 4 00 56" src="https://user-images.githubusercontent.com/48753593/64919375-043b7980-d7e5-11e9-8467-0d5b844ed112.png">
<img width="984" alt="스크린샷 2019-09-15 오후 4 01 46" src="https://user-images.githubusercontent.com/48753593/64919376-04d41000-d7e5-11e9-87d1-b935dbd9510a.png">
<img width="979" alt="스크린샷 2019-09-15 오후 4 03 08" src="https://user-images.githubusercontent.com/48753593/64919377-04d41000-d7e5-11e9-8a5b-213b81ab5128.png">
<img width="991" alt="스크린샷 2019-09-15 오후 4 04 08" src="https://user-images.githubusercontent.com/48753593/64919378-04d41000-d7e5-11e9-9e51-f5eae37717e0.png">
<img width="1002" alt="스크린샷 2019-09-15 오후 4 08 12" src="https://user-images.githubusercontent.com/48753593/64919379-04d41000-d7e5-11e9-82bf-79db37347db8.png">
<img width="995" alt="스크린샷 2019-09-15 오후 4 10 48" src="https://user-images.githubusercontent.com/48753593/64919380-056ca680-d7e5-11e9-9bc6-0d45e5b05adb.png">
<img width="984" alt="스크린샷 2019-09-15 오후 4 28 01" src="https://user-images.githubusercontent.com/48753593/64919397-2df4a080-d7e5-11e9-84ed-83138f669e99.png">
<img width="978" alt="스크린샷 2019-09-15 오후 4 27 47" src="https://user-images.githubusercontent.com/48753593/64919398-2df4a080-d7e5-11e9-8908-753bfdc69982.png">
<img width="973" alt="스크린샷 2019-09-15 오후 4 27 38" src="https://user-images.githubusercontent.com/48753593/64919399-2e8d3700-d7e5-11e9-8d18-275c85df6eb9.png">
<img width="990" alt="스크린샷 2019-09-15 오후 4 27 29" src="https://user-images.githubusercontent.com/48753593/64919400-2e8d3700-d7e5-11e9-8ead-5d8cd029dc91.png">
<img width="967" alt="스크린샷 2019-09-15 오후 4 26 54" src="https://user-images.githubusercontent.com/48753593/64919401-2e8d3700-d7e5-11e9-8ee5-eae503e07914.png">
<img width="979" alt="스크린샷 2019-09-15 오후 4 26 21" src="https://user-images.githubusercontent.com/48753593/64919402-2f25cd80-d7e5-11e9-945a-72d3380f7050.png">
<img width="982" alt="스크린샷 2019-09-15 오후 4 25 54" src="https://user-images.githubusercontent.com/48753593/64919403-2f25cd80-d7e5-11e9-9630-43faa7418fd7.png">
<img width="970" alt="스크린샷 2019-09-15 오후 4 20 13" src="https://user-images.githubusercontent.com/48753593/64919404-2f25cd80-d7e5-11e9-9e52-23d5a48b1836.png">
<img width="986" alt="스크린샷 2019-09-15 오후 4 12 58" src="https://user-images.githubusercontent.com/48753593/64919405-2fbe6400-d7e5-11e9-858c-730e7ca487cc.png">
<img width="983" alt="스크린샷 2019-09-15 오후 4 11 07" src="https://user-images.githubusercontent.com/48753593/64919406-2fbe6400-d7e5-11e9-9344-3cd0f5b14ec0.png">
<img width="981" alt="스크린샷 2019-09-15 오후 4 31 55" src="https://user-images.githubusercontent.com/48753593/64919407-31882780-d7e5-11e9-8b70-ea4a2ee45a1d.png">
<img width="969" alt="스크린샷 2019-09-15 오후 4 32 18" src="https://user-images.githubusercontent.com/48753593/64919409-3220be00-d7e5-11e9-825e-eafc0b42b2db.png">
<img width="1007" alt="스크린샷 2019-09-15 오후 4 35 24" src="https://user-images.githubusercontent.com/48753593/64919410-3220be00-d7e5-11e9-983b-da5ebb490bad.png">
<img width="992" alt="스크린샷 2019-09-15 오후 4 35 32" src="https://user-images.githubusercontent.com/48753593/64919411-3220be00-d7e5-11e9-9fdd-acdbc3c9700b.png">
<img width="979" alt="스크린샷 2019-09-15 오후 4 41 50" src="https://user-images.githubusercontent.com/48753593/64919412-3220be00-d7e5-11e9-848d-2c2ab7162eb2.png">
<img width="962" alt="스크린샷 2019-09-15 오후 4 42 28" src="https://user-images.githubusercontent.com/48753593/64919413-32b95480-d7e5-11e9-975d-a51558f8adee.png">
<img width="983" alt="스크린샷 2019-09-15 오후 4 43 00" src="https://user-images.githubusercontent.com/48753593/64919414-32b95480-d7e5-11e9-8dfa-57a524267327.png">

