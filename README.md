codespace생성
##terminal
docker pull jupyter/minimal-notebook #docker로 컨테이너 생성 -> docker pull함
docker images #여기에 나온 imageid를 계속쓸것
#container는 어떤 프로그램을 실행되고 있는 상태만 떠줌 -> healthy (jupyter가 실행중인것)
#실행 프로그램이 없으면 stop이 됨
docker run -d -p 8888:8888 e75d34b8f32 #image로 만든 컨테이너의 8888포트를 외부환경의 8888포트와 연결하는 것
#포트 연결해서 표출하게 함
#여러 개의 컨테이너를 동일 포트로 열었으나 다른 포트로 연결되도록 함
#별도의 주소를 만들어서 포트창에 포트가 하나 만들어짐
#로컬주소복사 -> 새로운 창에 붙여 넣으면 저 포트로 접속됨
docker logs 5da5cf15deab #docker id하고 token복사
#로컬주소복사 -> token 넣어주면 새로운창으로 jupyter lab 생성가능

docker image rm imageid --제거
docker image ls imageid --이미지 목록
docker container ls
docker container rm
docker network ls networkid

