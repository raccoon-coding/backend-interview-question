# Concurrency
## Concurrency Error
Thread는 CPU 작업의 한 단위이다.
여기서 MultiThread 방식은 멀티태스킹을 하는 방식 중, 한 코어에서 여러 Thread를 이용해서 번갈아 작업을 진행하는 것이다. 따라서 공유 자원이 Process단위보다 더 많아진 만큼 에러가 발생할 확률이 올라간다. 이러한 에러를 동시성 이슈라고 한다.

### Thread Safe
1. 암시적 Lock(synchronized)
   
    문제가 발생할 수 있는 변수 혹은 메서드에 synchronized를 넣어서 Lock을 걸어버리는 방식이다.
2. 명시적 Lock(ReentrantLock)
   
    문제가 발생할 수 있는 코드에 lock이라는 변수를 만들어서 개발자가 직접 Lock을 걸어버리는 경우이다. 이 경우 개발자가 섬세하게 unlock을 다 해줘야 한다. unlock을 안한 경우 큰 문제가 생길 수 있다.
3. Thread Safe 객체 사용(Atomic, 원자성 : 한번에 명령을 처리하는 단계)

    애초에 Lock을 최적화해서 객체 자체가 Thread Safe한 객체를 사용하는 것이다. 대표적으로 concurrent패키지 안에 있으며 HashMap이 여기에 포함된다.
4. 불변 객체(Immutable Instance) 사용

   애초에 수정이 불가능한 객체를 사용하는 것이다. 우리가 알고있는 객체는 String이 대표적이며, BackEnd에서 사용하는 경우 Setter를 만들지 않는 것이다.

### 참고자료
- https://velog.io/@mooh2jj/%EB%A9%80%ED%8B%B0-%EC%8A%A4%EB%A0%88%EB%93%9C%EC%9D%98-%EB%8F%99%EC%8B%9C%EC%84%B1-%EC%9D%B4%EC%8A%88
- https://devwithpug.github.io/java/java-thread-safe/