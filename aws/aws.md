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

Slide 확인
