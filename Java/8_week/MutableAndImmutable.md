# Mutable and Immutable
## Mutable (가변 객체)
가변 객체는 말 그대로 변경을 허용하는 객체이다. 따라서 객체 수정이 가능하고, 이에 따라서 동시성 이슈를 발생시킬 수 있는 여지가 있다. 대표적으로 int, double이 존재한다.

## Immutable (불변 객체)
불변 객체는 말 그대로 변경을 허용하지 않는 객체이다. 따라서 수정해도 객체를 수정하는 것이 아닌, 재할당을 통해 새로운 객체를 만들어내는 방식으로 동작한다. 따라서 가변 객체보다 Cost를 더 많이 사용한다.

그러나 불변 객체는 Thread Safe하므로 대부분 실무에서 불변 객체를 권장하는 편이다.(Setter 지양하기) 대표적으로 String이 존재한다.

### 참고 자료
- https://velog.io/@guswlsapdlf/Java%EC%9D%98-Mutable%EA%B3%BC-Immutable
- https://cdy0510.github.io/2018/05/10/mutable-immutable/