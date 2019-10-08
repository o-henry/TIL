# AWS Personalize
 > 사용자에게 꼭 필요한 추천상품을 AWS 에서 제공하는 Algorithms(recipe)을 통해 검색 없이도 추천해줄 수 있는 기능. 
 
 > 이는 즉 매출 상승에 영향을 미친다 (AWS 의 지표 로는 30% 이상 증가)
 
 
## Personalize

 ### Data Pipeline

 사용자 중심 / ITEM 중심 / 사용자 - ITEM Interaction 인지에 따라서 **Schema 지정 및 Data Format 을 구성 및 준비**
 
 생성한 데이터를 S3에 업로드 한다.
 
 API 를 통해 Personalize 연동 
 
 알고리즘(레시피) 선택을 통해 트레이닝 (AutoML 최적화)
 
 
![undefined](https://user-images.githubusercontent.com/48753593/66401545-48a1ea00-ea1e-11e9-94cb-ad9690c86c8e.png)
![inawisdom-1](https://user-images.githubusercontent.com/48753593/66401650-75560180-ea1e-11e9-8977-975f9c191f94.gif)
![product-page-diagram_amazon_personalize_how-it-works 3ceac8883c7d6bd67d7cf26d8a7d505520d02a40](https://user-images.githubusercontent.com/48753593/66401654-76872e80-ea1e-11e9-93d8-2c3f32bed16f.png)
 
##### Data Formatting 과 형식만 잘 잡혔다면 데이터를 올리고 난후 모델 생성은 매우 간단하다

사람들이 클릭을 했을때 특정 상품에 대해서 관심을 최근에 얼마나 갖고 있었는가를 가지고 이후상품에 대한 추천을 하는 모델


<hr />

### Personalize Update

 ##### Airflow를 활용한 방법 
  
  특정 시간마다 S3 부터 생성 하는 과정을 반복한다. 데이터가 클수록 소요시간이 길어진다 
 
 ##### PutEvents API를 활용한 방법.
 
  PutEvents를 통해 요구하는 형태의 데이터를 모은다. Cloud Watch를 통해 생성된 데이터를 확인한다.
  
 최종적으로 create solution version -> campaign update 를 통해 추천결과를 업데이트 한다.
 
 trainning을 주기적으로 해야한다.
 
 put event 시 데이터는 들어가 있고, 트레이닝만 다시해주면 된다.
 
 #### Personalize 생성과정 

Process

1.	사용자 ID, 항목 ID 등에 대한 Personalize 예약 키워드를 사용하여 데이터 세트를 정의하는 스키마를 생성합니다.
2.	모델 구축 및 예측에 사용되는 데이터 세트를 포함하는 데이터 세트 그룹을 생성합니다. 여기에는 사용자-항목 상호 작용(“누가 무엇을 좋아하는지”), 사용자 및 항목 데이터 세트가 포함될 수 있습니다. 아래의 예제에 나와 있듯이 마지막 2개는 선택 사항입니다.
3.	Personalize로 데이터를 보냅니다.
4.	솔루션을 생성합니다. 즉, 추천 레시피를 선택하고 데이터 세트 그룹에서 훈련합니다.
5.	새로운 샘플을 예측하는 캠페인을 생성합니다.

 
 Stack: Django(Python) 와 mongoDB를 활용하여 Personalize recommendation 값을 받아올 것.
 
 1. AWS Personalize guide 에 따라서, 스키마를 만들고 Pandas 를 통해 csv 파일을 생성, S3 bucket에 추가한다.
 
