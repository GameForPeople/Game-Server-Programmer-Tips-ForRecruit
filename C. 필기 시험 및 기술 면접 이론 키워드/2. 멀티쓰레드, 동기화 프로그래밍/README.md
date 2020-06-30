## <a name="multithread"></a> 2. 멀티 스레드 & 동기화 프로그래밍

#### 기초
> * 스레드? 프로세스? ( 멀티 쓰레드 vs 멀티 프로세스 )
> * 멀티 쓰레드에서의 동기화 방안
> * 멀티 스레드를 해야하는 이유(발열, 고성능)
> * Data Race
> * mutual exclusion(상호 배제)
> * Critical Section(임계영역?)
> * Context Switch
> * Dead Lock의 조건(명칭 암기)과 이를 극복해내는 방안 (..식사하는 철학자)

> * Lock 프로그래밍?
> * Lock 방안 : 세마포어 vs 뮤텍스 vs 모니터
> * 성긴 동기화, 세밀한 동기화, 낙천적 동기화, 게으른 동기화
> * 데드락 발생 조건과 방지방법 (원리적 수준, 언어적 수준)
> * Lock Overhead
> * Priority inversion & Convoying

> * Spin Lock의 장점, 단점, 언제 사용?
> * TAS vs TTAS vs Back-Off
> * rwLock, ReadLock? WriteLock? 어떻게? (ex, srwlock, shared_mutex)

> * Lock-Free 프로그래밍?
> * Atomic 연산?
> * CAS(Compare and Swap)?
> * C++ Memory Order
> * atomic is_lockfree?의 true, false?, false동기화는?

> * Cache Line?
> * 싱글 스레드에서 캐시 라인을 고려한 프로그래밍? (공간 지역성)
> * 멀티 스레드에서 캐시 라인을 고려한 프로그래밍? (캐시 일관성 오버헤드)
> * 메모리 얼라인먼트( + 패킹, 패딩 바이트), ~~메모리 시리얼라이즈~~
> * Write Buffering에 의한 중간값 문제

> * ABA문제의 원인과 해결 방안
> * Heterogeneous vs Homogeneous 에 대한 자신의 생각은?
___

#### 심화
> * 다양한 라이브러리에 대한 상식 (Parallel Patterns Library(MS), Intel-TBB, OpenMP)
> * 상식 수준의 유명한 문제들 (잠자는 이발사, 식사하는 철학자, Cigarette Smokers Problem, readers-writers, producer-consumer)
> * 멀티 스레드 특화 언어들에 대한 기본 지식
> * 함수형 언어들에 대한 특징, 지식
> * 락프리 프로그래밍 경험
___
 
[[이전]](https://github.com/GameForPeople/Game-Server-Programmer-Tips-ForRecruit/tree/master/C.%20%ED%95%84%EA%B8%B0%20%EC%8B%9C%ED%97%98%20%EB%B0%8F%20%EA%B8%B0%EC%88%A0%20%EB%A9%B4%EC%A0%91%20%EC%9D%B4%EB%A1%A0%20%ED%82%A4%EC%9B%8C%EB%93%9C)
