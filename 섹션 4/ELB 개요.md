

```
Load balancer란?
-네트워크 트래픽을 분산하는 서비스

-Elastic Load balancer?
-AWS 로드밸런서 서비스
-네트워크 트래픽을 EC2 인스턴스, 컨테이너, IP 주소 등 여러 대상으로 자동으로 분산 가능
-애플리케이션의 가용성과 내구성을 높일 수 있음
-로드밸런서가 비정상 대상을 감지하면, 해당 대상으로 트래픽 라우팅을 중단하고 정상대상으로만 트래픽 라우팅
대상이 다시 정상으로 감지되면 트래픽을 해당 대상으로 다시 라우팅 가능

- Elastic Load balance의 종류

1) Application Load balancer
-layer 7
- http, https
- http header content를 사용해 라우팅 요청 처리
- 웹 애플리케이션, 서비스에 적합 

2) Network Load balancer
-layer4
- TCP, UDP, TLS
- Protocol, Port Number를 사용해 라우팅 요청 처리
- 수백만의 대용량 트래픽 처리에 적합 


3) Gateway Load balancer
-Layer 3 - Gateway Load balancer endpoint
-layer 4 - gateway load balancer
-GENEVE protocol을 사용하여 encapsulation 트래픽 전송
- Transparency한 네트워크 게이트웨이를 제공하므로
  보안 검사를 위한 방화벽, IPS, IDS 등의 원본 패킷의 데이터가 중요한
  가상 어플라이언스에 적합


4) Elastic Load balancer 구성(Gateway Load balancer 제외)
- 클라이언트가 리스너로 접속
-> 리스너가 타겟 그룹으로 라우팅

리스너
-구성한 프로토콜 및 포트를 사용해 연결 요청을 확인하는 기능
-리스너에서 정의한 규칙에 따라 로드밸런서가 대상그룹에서 대상으로 라우팅하는 방법이 결정됨
-클라이언트와 대상간의 연결을 위한 프로토콜 및 포트 번호로 구성

타겟 그룹
-대상의 모임
- 타겟
1) EC2 인스턴스
2) EC2 Auto Scaling Group
3) IP Address
4) Lambda
5) Application Load balancer


```
