<<<<<<< HEAD
# 네트워크
=======
# 네트워크 기본
>>>>>>> 96aa9004bac69a02ad19749b6c5480605a7d645e

- 네트워크: 컴퓨터들이 통신 기술을 이용하여 망형태로 연결된 통신 형태
- 의존적 관계가 성립하는 규칙(프로토콜)을 계층구조로 나타낸 것이 osi7 layer
<<<<<<< HEAD
- NIC(Network Interface Card) = LAN(Local Area Network) 카드  
: 네트워크 안에서 통신을할 때 사용하는 H/W
- MAC address(= 하드웨어 주소(피지컬 address)): NIC의 식별자  
=======
- 소켓의 실체는 file 이다 (mp3파일 같은)  
그러한 파일 형태의 네트워크 추상화가 이루어진 파일을 소켓이라고 한다  
소켓을 열었다, 닫았다 라는 말  
파일 즉 소켓을 여는 주체가 무엇이냐 하면 프로세스이다  
어떤 프로세스가 어떤 소켓 즉 파일을 열었다 라고 할 수 있다
- HTTP 프로토콜 + SSL 프로토콜 = HTTPS

  

- 2=이더넷 (드라이버에서 NIC(Network Interface Card=랜 카드) 수준) 까지 핵심 식별자가 있는가?  
식별하는 주소 : MAC주소 식별자 = 하드웨어 주소(피지컬 address)  
⇒ MAC address는 랜카드(NIC)에 붙는다(식별한다)  
>>>>>>> 96aa9004bac69a02ad19749b6c5480605a7d645e
컴퓨터에 랜카드가 3개 꽂혔다 => MAC address 3개

---

- L3 = 인터넷 프로토콜  
식별자 : IP주소(v4, v6있는디 일단 v4만 다룸)  
⇒ 인터넷을 사용하는 컴퓨터를 식별
- IP주소: host의 식별자

---

- L4 = TCP / UDP  
port 번호  
다루는 영역에 따라 port 식별자를 말하는 방법이 다름  
L2(H/W) : Interface 식별자  
네트워크(L3, L4) : Service 식별자  
<<<<<<< HEAD
PC, 서버 단위로 보는 사람들(프로그램관리, S/W개발) : Process 식별자
=======
end point에서만 보는 경우(PC, 서버 관리하는 사람들) : Process 식별자
>>>>>>> 96aa9004bac69a02ad19749b6c5480605a7d645e

---

- Host : computer + network => 인터넷(네트워크)에 연결된 컴퓨터
- Host는 2가지 : end-point, switch  
switch : network 그 자체를 이루는 host(infra structure) => Host의 목적이 네트워크 자체를 확장하거나 기능 요소
- End-point ? (단말기)  
Host인데 네트워크 이용 주체  
네트워크라는 인프라 스트럭처를 쓰는 것
- End-point중 대표적인 것  
단말기의 역할에 따른 분류  
클라이언트, 서버  
Peer : 소비와 제공이 동시에 될 때
- 컴퓨터인데 네트워크에 연결되는 컴퓨터 : host  
Host인데 네트워크 자체를 이루면 switch  
네트워크 인프라 이용주체 : end-point
- Switch 의 종류
Router(L3스위치 일종, 제일 대표적)  
IPS : security switch 보안 스위치  
Tab, aggregation : 관리 목적

---

- 교차로가 스위치, 경로선택의 근거를 이정표 라고 할 때,  
스위치(교차로)에서 경로 선택을 하느 것 => 네트워크에서는 interface를 선택하는 것 = switching스위칭  
IP주소(네트워크계층:L3)를 근거로 스위칭을 한다면 => L3스위칭  
라우터마다 이정표가 있는데 이것이 라우팅 테이블이다.  
MAC주소로 스위칭 => L2스위칭  
port번호로 스위칭 => L4스위칭  
Http => L7 스위칭
- 네트워크에서는 이동할 때 비용을 생각한다  
그 주제중 하나가 Matric값이다. 비용이 싼 게 좋은 것  
일단 Matirc = 비용 으로 알고 있기
- 고속도로망 : 네트워크(인터넷)  
자동차 : packet 패킷  
교차로 : router 라우터 => 스위치  
이정표 : routing table

---

- NIC(Network Interface) = LAN 카드  
네트워크의 규모 : WAN > MAN > LAN
- MAC주소는 NIC 의 식별자  
Packet 은 L2에서 말하는 인터넷에서의 단위  
L2 수준의 유통 데이터 단위 : Frame
- 랜카드라는 표현보다는 NIC 이라고 한다  
LAN은 네트워크의 규모를 말한다  
NIC은 H/W이며 PC(host)한대가 인터페이스를 여러개를 가질수도 있다

---

- L2 Access switch  
L2스위치로 Mac주소로 스위칭을 한다
- 허브(스위치)의 단자 하나도 Interface라고 부른다 = Port 라고도 한다
- Link-up : lan케이블이 연결된 상황  
Link-down : 연결이 끊겼을 때  
Uplink : 상위(ex:L3)로 나아갈 때
- L2 Distribution switch 란?  
쉽게 생각하면 L2 Access 스위치를 위한 스위치  
L2고성능 스위치  
L2 access를 모아서 스위칭 함

---
Broadcast  
- host가 속해있는 네트워크 전체를 대상으로 하는 통신
- Broadcast 사용범위를 잘 생각해야한다(효율을 떨어뜨리기 때문)
- Broadcast통신이 끝날 때까지 다른 것들은 통신을 못한다  
브로드캐스트는 최소화해야한다
- 브로드캐스트 범위를 줄여줘서 네트워크 운영효율을 올릴 수 있다  
대신 브로드캐스트가 꼭 필요한 경우 반응하지 않는 문제가 생길 수 있다
- H/w : Physical  
S/w : logical (비슷항 의미로 Virtual)
- Cpu : machine  
소프트웨어로 구현한 cpu : virtual machine  
H/w 를 s/w로 구현하는 기술 : 가상화 기술
- 네트워크 최소 단위 : LAN => 피지컬로 설명되는 네트워크가 주로 LAN이다(이해를 돕기 위한 내용 실제로는 아니다)  
인터넷 => WAN => 논리적 네트워크
