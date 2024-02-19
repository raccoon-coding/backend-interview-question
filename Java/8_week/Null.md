# Null
Null은 값이 할당되지 않은 변수 및 객체를 의미하며 두 참조값이 null을 가리키고 있으면 두 참조는 같은 것이라고 가정한다.

하지만 nullpointer문제는 실제 가동하고 있는 어플에서 많이 발견될만큼 흔한 오류인데 이 null을 처리하는 방식은 assert 명령어 사용, Object사용등이 있다.
## Assert
assert는 JDK 1.4부터 도입된 명령어로 메소드에 들어온 파라미터 혹은 객체가 null을 참조하고 있는지 체크하고, 선처리를 할 수 있도록 도와준다.

하지만 assert는 예외처리 방식이 아닌 검사이므로 Pass를 제공한다. 따라서 테스트과정에서 많이 사용하고 있다.

## Objects
Java 8, 9이후로 객체가 null을 참조하고 있는지 확인하는 메소드가 추가되었다.

Java 8
- isNull(Object obj)
- nonNull(Object obj)
- requireNonNull(T obj)
- requireNonNull(T obj, String message)
- requireNonNull(T obj, Supplier<String> messageSupplier)

Java 9
- requireNonNullElse(T obj, T defaultObj)
- requireNonNullElseGet(T obj, Supplier<? extends T> supplier)

### 참고 자료
- https://eastglow.github.io/back-end/2020/01/10/Java-%EC%9E%90%EB%B0%94%EC%97%90%EC%84%9C-null%EC%9D%84-%EC%95%88%EC%A0%84%ED%95%98%EA%B2%8C-%EB%8B%A4%EB%A3%A8%EB%8A%94-%EB%B0%A9%EB%B2%95.html
- https://yeh35.github.io/blog.github.io/documents/java/java-assert/