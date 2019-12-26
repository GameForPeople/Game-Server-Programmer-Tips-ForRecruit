## <a name="network"></a> 1. 네트워크, I/O
 - 웹에 대한 지식이 없어, 관련 내용이 없습니다. (예외 1. https vs http 2. https 보안 로직 3. Get vs Post)
 
#### 기초
> * TCP와 UDP의 기본적인 정의, 특징, 비교
> * UDP가 TCP보다 빠른 이유(헤더 사이즈에 따른 체크섬 비용, 재전송 관련 불필요 데이터 처리)
> * TCP 헤더의 각 필드와 그 역할 (+UDP 헤더 구성)
> * TCP Checksum 동작 원리
> * TCP ACK-SEQ 동작 원리
> * TCP 상태
> * TCP 3way-hand-shaking의 정의, 이유, 각 과정에서 일어나는 일
> * TCP 4way-hand-shaking와 다양한 연결 종료 상태, 우아한 종료

> * 소켓 옵션들 정리(소켓 수준, ip수준, tcp 수준)
> * 네이글 알고리즘 (TCP_NODELAY) 및 네이글 알로리즘에서의 Send가 이루어지는 조건
> * 위와 관련하여, MTU, MSS 약자 및 정의

> * 멀티쓰레드 모델
> * Select 모델 원리
> * Overlap 모델 원리와 장단점
> * Overlap Callback VS Overlap Event 비교
> * IOCP 모델 원리와 장점

> * 블로킹 vs 논블로킹
> * 동기 vs 비동기
> * 블로킹 개념 vs 동기 개념

> * 대칭키 암호화 vs 비대칭키 암호화
> * 스푸핑, 스누핑, syn flooding,

> * silly window syndrome?
> * Tcp Packet Loss algorithm
> * TCP 혼잡 제어, 흐름 제어는 어케?

> * IP, Port, MAC ADDR ?
> * OSI 7계층의 각 계층 명칭 및 간단한 정의, 역할 등 서술
> * p2p NAT 투과 : 홀 펀칭(TCP) & Simple traversal of UDP through NAT(UDP)

___

#### 심화
> * Boost/Asio 모델
> * EPOLL 모델
> * IOCP의 단점(Memory lock/unlock), Zero-Recv, Zero-Recv Overhead
> * `Registered io` 모델

> * 블록체인
> * Serverless architecture
> * Special OS?

___
 
[[이전]](https://github.com/GameForPeople/Game-Server-Programmer-Tips-ForRecruit/tree/master/C.%20%ED%95%84%EA%B8%B0%20%EC%8B%9C%ED%97%98%20%EB%B0%8F%20%EA%B8%B0%EC%88%A0%20%EB%A9%B4%EC%A0%91%20%EC%9D%B4%EB%A1%A0%20%ED%82%A4%EC%9B%8C%EB%93%9C)