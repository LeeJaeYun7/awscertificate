

```
대상 유형
1) 인스턴스
- 개별 인스턴스 or EC2 Auto Scaling Groups

2) IP 주소

3) Lambda 함수
- Application load balancer

4) Application load balancer
- Network load balancer

프로토콜
- 타겟 그룹의 프로토콜에 따라 라우팅
- 선택하는 프로토콜에 따라 연결할 수 있는 LB가 다름

상태 검사
-등록된 타겟에게 상태 확인 메시지를 보내서 대상의 상태를 확인

속성(Attriubutes) - HTTP/HTTPS
-Application Load balancer에서 사용

-등록 취소 지연
-> Auto Scaling 축소 등으로 등록 취소된 인스턴스에 더 이상의 요청을 보내지 않도록 하는 기능

- 느린 시작 기간
- 알고리즘
1) 라운드 로빈
2) 최소 미해결 요청
  
- 고정
1) 클라이언트가 세션을 유지한 상태라면 모든 요청을 동일한 인스턴스로 유지하는 기능
2) 세션 데이터를 잃지 않으려는 상태정보를 유지하는 서버에 적합

속성 - TCP/UDP/TLS

- 등록 취소 지연은 동일한 기능
- 등록 취소 시 연결 종료
-> 등록 취소 지연에 도달 했을 때 NLB가 활성 연결 종료

- 프록시 프로토콜 v2
- 클라이언트 IP 주소 보존
-> 들어오는 모든 트래픽의 클라이언트 IP를 애플리케이션에 전달

- 고정
-클라이언트가 세션을 유지한 상태라면 모든 요청을 동일한 인스턴스로 유지하는 기능
- 세션 데이터를 잃지 않으려는 상태정보를 유지하는 서버에 적합


고정 세션
- 고정 세션은 대상 그룹의 동일한 대상으로 클라이언트 트래픽을 라우팅하는 기능
- Application Load balancer, Network Load balanacer 모두 사용 ㅏㄱ능
- Application Load balancer는 쿠키 필요

교차 영역 로드밸런싱
1) 교차 영역 로드 밸런싱 비활성화
2) 교차 영역 로드 밸런싱 활성화

- EC2 웹 서버 생성 스크립트






```
