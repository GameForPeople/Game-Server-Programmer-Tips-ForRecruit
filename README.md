# Game-Server-Programmer-Tips-ForRecruit
>해당 문서는 제가 채용 과정에서 경험한 내용들을 바탕으로, 
>
>다른 신입 게임 서버 프로그래밍 파트 지원자분들에게 도움이 될 수 있도록 간단하게 정리했습니다.

## Index

#### A. 2019년 신입 서버 공채 후기[->](#chapter0)

#### B. 포트폴리오 팁[->](#chapter1)

#### C. 자소서 및 기술 면접 팁[->](#chapter2)

#### D. 필기 시험 및 기술 면접 이론 키워드[->](#chapter3)
   >[0. C++](#cpp)
   >
   >[1. 네트워크, I/O](#network)
   >
   >[2. 멀티 스레드 & 동기화 프로그래밍](#multithread)
   >
   >[3. 자료 구조 & 알고리즘](#algorithm)
   >
   >[4. 데이터 베이스](#database)

#### E. 기타 링크
 * [국내 게임 회사 채용 사이트 모음](https://github.com/GameForPeople/korea-game-career-site)

## <a name="chapter0"></a>A. 2019년 신입 서버 공채 후기

## <a name="chapter1"></a>B. 포트폴리오 팁

## <a name="chapter2"></a>C. 자소서 및 기술 면접 팁

## <a name="chapter3"></a>D. 필기 시험 및 기술 면접 이론 키워드

### <a name="cpp"></a>0. C++

#### 기초
> * `Called By Reference`와 `Called By Value`의 정의, 비교 등
> * `복사 생성자`와 `이동 생성자`의 정의, 비교, 호출되는 경우 등
> * `이동 의미론`과 `임시 객체`, `RValue`에 대하여
> * 

> * 대입을 통한 초기화 VS 초기화 리스트
> * 대리 생성자, 두 단계 초기화, 기본 멤버 초기화

> * `public, protected, private`상속 비교
> * `virtual, override, final`의 용도
> * 순수 가상 함수와 추상 클래스, 인터페이스 `abstract, interface`
> * 상위 클래스의 소멸자(공개 가상 소멸자, 비공개 비가상 소멸자)
> * 가상 함수 테이블 정의 및 동작 원리

> * Try Exception (try, catch, throw) 및 주의사항(memory Leak, dead Lock)
> * `noexcept` 의 정의와 강한 예외 안정성 보장
> * 

> * Template??, generic programming, Template Meta programming
> * Class Template, Function Template
> * 명시적 클래스 특수화, 명시적 함수 특수화, template instance
> * variadic template, parameter pack, fold expression
> * type_traits library

> * `RAII`(Resource Acquisition Is Initialization)
> * 스마트 포인터 (`unique_ptr`, `shared_ptr`, `weak_ptr`) 특징 및 비교
> * make_unique, make_shared.. why?
> * `Shared_ptr`의 Reference Count와 Overhead
> * `unique_ptr`의 리소스 이전
> * 스마트 락 (`lock_guard`, `unique_lock`, `scoped_lock`) 특징 및 비교
> * 

> * 호출 가능한 객체 ( callable object )
> * lambda Function( 기본 문법, lambda capture, noexcept) 
> * std::function vs function ptr> 
> * std::mem_fn, std::bind

> * C++ Memory Order ( memory_order_seq_cst, memory_order_acqire, memory_order_release , memory_order_relexed)
> * atomic header (std::atomic<T>, atomic_thread_fence) ,  Load, Store, Exchange, Campare and Set
> * atomic flag? (with spin lock)
> * mutex vs shared_mutex vs critical section(winapi)

> * 연산자 오버로딩
> * attribute
> * #pragma pack()
> * auto
> * 형변환 ( static_cast, reinterpret_cast, dynamic_cast )
> * 암시적 형변환, explicit
> * mutable
> * C++11 : thread
> * union
> * pair, tuple

> * new vs delete
> * override vs overload
> * Struct VS Class
> * using VS typedef
> * if VS Switch (jump statement vs  branch statement) (vs Function Pointer Arr 성능 비교)
> * const vs constexpr, macro vs constexpr
> * enum vs namespace enum vs enum class
> * Try Exception VS assert vs static assert
> * #ifdef vs if constexpr 
> * volatile vs atomic
> * stdcall vs cdecl 

#### 심화
> * C++의 방향성
> * C++20 : multi-thread(atomic smart pointer, Latch, barrier, jthread), concepts, Coroutine, Module ...
> * Boost Library?
> * async, future, promise
> * Coroutine VS Thread
> * std::move , std::forward , std::ref
> * this_thread namespace, thread_local
> * import(module) vs include
> * 그 외 자잘한 것들 : if-init, Structured binding, std::optional, std::any...


### <a name="network"></a> 1. 네트워크, I/O
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

#### 심화
> * Boost/Asio 모델
> * EPOLL 모델
> * IOCP의 단점(Memory lock/unlock), Zero-Recv, Zero-Recv Overhead
> * `Registered io` 모델

> * 블록체인
> * Serverless architecture
> * Special OS?

### <a name="multithread"></a> 2. 멀티 스레드 & 동기화 프로그래밍 & 관련 이론

#### 기초
> * 스레드? 프로세스? ( 멀티 쓰레드 vs 멀티 프로세스 )
> * 멀티 쓰레드에서의 동기화 방안
> * 멀티 스레드를 해야하는 이유(발열, 고성능)
> * Data Race? 최소 조건?
> * mutual exclusion(상호 배제)
> * Critical Section(임계영역?)
> * ?? Context Switch

> * Lock 프로그래밍?
> * Lock 방안 : 세마포어 vs 뮤텍스 vs 모니터
> * 성긴 동기화, 세밀한 동기화, 낙천적 동기화, 게으른 동기화
> * 데드락 발생 조건과 방지방법 (원리적 수준, 언어적 수준)
> * Lock Overhead
> * Priority inversion & Convoying

> * Spin Lock의 장점, 단점, 언제 사용?
> * rwLock? (ex, srwlock, shared_mutex)
> * TAS vs TTAS vs Back-Off

> * Lock-Free 프로그래밍?
> * Atomic 연산?
> * CAS(Compare and Swap)?
> * C++ Memory Order
> * atomic 라이브러라의 is_lockfree?의 true 조건, false인 T의 경우 동기화는?

> * Cache Line?
> * 싱글 스레드에서 캐시 라인을 고려한 프로그래밍? (공간 지역성)
> * 멀티 스레드에서 캐시 라인을 고려한 프로그래밍? (캐시 일관성 오버헤드)
> * 메모리 얼라인먼트( + 패킹, 패딩 바이트), ~~메모리 시리얼라이즈~~
> * Write Buffering에 의한 중간값 문제

> * ABA문제의 원인과 해결 방안
> * Heterogeneous vs Homogeneous ,, 클라는? 서버는? 미래에는?

#### 심화
> * 다양한 라이브러리에 대한 상식 (Parallel Patterns Library(MS), Intel-TBB, OpenMP)
> * 상식 수준의 유명한 문제들 (잠자는 이발사, 식사하는 철학자, Cigarette Smokers Problem, readers-writers, producer-consumer)
> * 멀티 스레드 특화 언어들에 대한 기본 지식
> * 함수형 언어들에 대한 특징, 지식

### <a name="algorithm"></a>3. 자료 구조 & 알고리즘
 - 해당 항목 에서는 온라인/오프라인 코딩 테스트의 알고리즘이 아닌, 기술 면접과 시험에서의 주제를 다룹니다.

#### 기초
> * C-style Array vs STL::Vector 
> * Vector(Array) vs List
> * map vs unordered_map
> * stack vs queue
> * queue vs deque
> * STL 각 컨테이너들은 어떤 자료구조로 되어 있는가 (priority_queue? map? unordered_map?)

> * big-O?
> * 각 컨테이너에서의 탐색 비용
> * 각 컨테이너에서의 정렬 비용

> * 정렬 알고리즘에 대한 특징(워스트 케이스, 요구 사항) 및 비용 - 퀵, 버블, 선택, 삽입, 힙, 레딕스..
> * 각 정렬 알고리즘 정도는 손코딩

> * 트리 구조의 Best, Worst 케이스 
> * AVL Tree VS Red-Black Tree 선택 기준은?

> * 재귀 함수의 장/단점, 꼬리 재귀(Tail Recusion)?
> * 팩토리얼 & 하노이탑 & 피보나치 손코딩

> * DFS, BFS
> * Pre-order, Post-order, In-order
> * 다익스트라?
> * A*?

> * 해싱?
> * 많이 사용되는 해싱 함수들? (std::hash는 ?)
> * 해싱 충돌 극복(체이닝, 오픈 어드레스, 더블 해싱)의 각 특징 및 장단점
> * rehash?

#### 심화
> * 허프만 알고리즘?
> * SkipList?
> * Vector Heap?
> * JPS(Jump Point Search)?

## <a name="database"></a> 4. DB

#### 기초
> * DB 용어
> * 트랜잭션과 ACID
> * 기본 키, 후보 키, 대체 키, 슈퍼 키, 외래 키
> * 외래 키 옵션 (RESTRICT, CASCADE, SET NULL, SET DEFAULT...) 
> * 각 정규화 단계 및 특징
> * 무결성 제약 조건 종류 및 특징
> * Join 종류
> * 샤딩, 파티셔닝 종류 및 주의 사항 

> * 인덱스
> * 클러스터링 인덱스, 논클러스트링 인덱스
> * B+트리의 삽입, 삭제, 탐색

> * SQL 정의어 조작어 제어어
> * SQL 기본 Query 작성 (정렬, 조인, 그룹 등등)

> * ODBC
> * Stored procedure? 장점?

> * NoSQL 정의, 특징, 종류
> * NoSQL VS RDBMS (핫해핫해)

