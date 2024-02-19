# Tight Coupling and Loose Coupling

## Tight Coupling (강한 결합)
객체 의존 결합에서 강한 결합이란 어떤 객체가 다른 객체에 강한 의존성을 가지고 있다라는 말이다.

의존성이란 다른 객체에 대해서 얼마나 많은 정보를 알고 있느냐에 대한 척도입니다.

따라서 강한 결합성 즉 강한 의존성을 가진다면 한 객체가 다른 객체에 너무나 많은 구현 정보를 알고 있게 되고, 이에 따라서 코드의 수정이나 업데이트가 일어날 때 전파가 전 범위에서 일어나게 된다.

## Loose Coupling (약한 결합)
느슨한 결합은 어떤 객체가 다른 객체에 대해서 최소한의 정보만 알고 있는 것을 말한다. 

따라서 약한 결합은 DI(Dependency Injection)를 통하거나 interface를 통해서 만들 수 있다.

DI는 말 그대로 의존성을 주입 받는 것이다. 객체가 다른 객체의 메서드를 사용해야 할 때, 그 객체를 parameter로 주입 받아서 사용하게끔 하는 것을 말한다.

이렇게 되면 객체가 필요한 메서드의 객체를 생성하지 않아도 되므로 메서드 객체의 변화로 인한 코드 수정이 없어도 된다.

Interface 방식은 API를 구현한 후, 다른 객체에 대해서 정보를 알고 싶을 때 객체의 api만 알고 있고 그 내부 과정을 모르도록 하는 것을 목표로 한다. 따라서 interface도 DI를 기반으로 하나, 이런 방식은 심지어 메서드 코드도 모르게 되므로 더욱 객체 지향적인 코드로 변화할 수 있다.


### 참고 자료
- https://citronbanana.tistory.com/8
- https://velog.io/@damiano1027/Java-%EA%B0%95%ED%95%9C-%EA%B2%B0%ED%95%A9%EA%B3%BC-%EC%95%BD%ED%95%9C-%EA%B2%B0%ED%95%A9
- https://leirbag.tistory.com/65
- https://velog.io/@heetaeheo/JAVA-%EA%B0%9D%EC%B2%B4-%EC%A7%80%ED%96%A5%EC%9D%98-%EA%B0%95%ED%95%9C-%EA%B2%B0%ED%95%A9%EA%B3%BC-%EC%95%BD%ED%95%9C-%EA%B2%B0%ED%95%A9
- https://hoho-hobi.tistory.com/220
