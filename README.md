# ✨ BTS (Bithumb NTF SNS) 💰

## 담당자 백인준

## 👉 프로젝트 소개

- 프로젝트명은 **Bithumb의 NFT와 SNS 서비스를 결합하여 BTS로 지었습니다.** 다양한 작가들의 그림과 아트를 NFT 코인 경매로 만나볼 수 있으며 빗썸 코인 유저들과 열린 소통을 할 수 있도록 SNS 커뮤니티도 활성화 시켰습니다.

## Jenkins 서버 

jenkins server url : http://15.165.43.193/

## jenkins 구성도 

<img width="750" alt="jenkins-docker-springboot-cicd" src="https://user-images.githubusercontent.com/58027908/135604568-283645a4-7cf9-422e-bf9a-771616890c9e.png">

기본적으로는 master branch 에 push 를 하게 되면 git hub 에 webhook 이벤트가 발생되어서 젠킨스에서 빌드를 수행하게 된다.

1. 로컬에서 깃헙 저장소로 푸쉬
2. 마스터 브랜치에 push 이벤트시 젠킨스 에서 해당 리포지토리의 gradle 빌드
3. docker image 빌드 
4. 이것을 publish over ssh 플러그인을 통해 해당 서버로 전달
5. 전달받은 jar ,dockerfile 을 런시켜서 spirng boot 가 뜨워진다 .

