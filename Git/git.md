### git Ignore

AWS 의 access key 와 같이 hub에 올라가서는 안되는 값의 경우 git ignore를 해주어야 한다. (보안상 매우 중요한 부분)

<img width="292" alt="스크린샷 2019-10-08 오후 10 57 29" src="https://user-images.githubusercontent.com/48753593/66402012-13e26280-ea1f-11e9-88d0-33f29c241f7a.png">
<img width="141" alt="스크린샷 2019-10-08 오후 10 57 36" src="https://user-images.githubusercontent.com/48753593/66402010-1349cc00-ea1f-11e9-9f50-8c121124839a.png">
<img width="243" alt="스크린샷 2019-10-08 오후 10 57 43" src="https://user-images.githubusercontent.com/48753593/66402006-12b13580-ea1f-11e9-8b95-f59ccadd3ad3.png">

위 그림처럼 ignore 하고 싶은 데이터가 담긴 파일명 자체를 ignore 안에 추가하거나, 확장자 자체를 ignore 할 수 있다.

ignore 된 파일은 editor 상에서 그림과 같이 회색으로 바뀌고, github에도 파일이 올라가지 않는다.
