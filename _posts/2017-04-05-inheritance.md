---
layout: post
title: (OOP)상속(Inheritance)의 잘못된 예
---

상속과 구성 모두 객체 지향 프로그래밍의 기본적인 요소이다. 다만 상속은 구성을 대체할 수도 있고 그 반대도 가능하기 때문에 개발자가 오용을 하는 경우가 발생한다는 점이다. 즉, 상속이 적절한 패턴임에도 구성으로 구현을 한다던가, 구성을 사용해서 쉽게 해결할 수 있는 문제를 상속을 사용해서 코드가 불필요하게 복잡해지는 경우를 들 수 있다.


# 상속의 잘못된 예
```
class Stack extends ArrayList {
    public void push(Object value) ...
    public Object pop() ...
}
```
1. (의미적 측면) subtype인가? Stack은 ArrayList의 서브타입이 아니다.[^1]
1. (기술적 측면) 캡슐화를 위반. Stack에서 구현한 메소드들을 제외한 나머지 ArrayList의 메소드들은 숨겨져야 한다.
1. 즉, ArrayList와 Stack은 전혀 다른 구현 모델이므로 상속을 해서는 안된다.

# 올바른 상속의 조건
1. super/sub 클래스가 논리적으로 같은 도메인이어야 한다.
1. 서브클래스는 수퍼클래스의 적절한 서브타입이어야 한다.
1. 수퍼클래스의 구현이 서브클래스가 필요로 하거나 사용가능해야 한다.
1. 서브클래스에 의한 개선은 부가적이어야 한다.(LSP)

# 구성은 언제 사용하는가
1. 실제로 상속이 필요한 경우는 매우 제한적이다. 위 조건을 만족하지 않는다면 구성으로 구현해야 한다. 구성은 상속보다 직관적이고 단순하며 재사용성이 좋다.



[^1]:[composition-vs-inheritance-how-choose](https://www.thoughtworks.com/insights/blog/composition-vs-inheritance-how-choose)
