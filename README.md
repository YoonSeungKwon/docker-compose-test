컨테이너간 통신은 같은 네크워크에 있을 경우 컨테이너 이름으로 통신
컨테이너에서 localhost는 컨테이너의 가상 환경을 의미하므로 IP를 다른 컨테이너로 설정해야 한다.
프론트에 리버스 프록시 서버(Nginx)가 있을 경우 CORS및 proxy_pass설정을 안하면 name resolve 에러가 뜰 수 있음 또한 포트 포워딩을 리버스 프록시 서버로 하고, 프론트에서의 요청을 컨테이너 명으로 매핑해 줘야함
