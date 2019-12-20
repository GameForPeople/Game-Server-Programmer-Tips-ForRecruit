# game-server-base-keywords
신입 게임 서버 프로그래머, 시험 및 기술 면접 예상 키워드 정리

## C++

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

> * C-style Array vs STL::Vector 
> * Vector(Array) vs List
> * unordered_map vs map
> * stack vs queue

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

## 네트워크


 
