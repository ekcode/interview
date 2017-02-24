---
layout: post
title: 자바 제네릭이란?
---

# 정의
클래스, 인터페이스 그리고 메소드를 정의할 때 그것들과 함께 사용될 타입을 파라미터로 넘길 수 있게 하는 것이다. 서로 다른 타입에 대해서 같은 코드를 반복할 필요없이 하나의 코드로 두 개 이상의 타입에 대응할 수 있다. 보통의 메소드 파라미터는 값`(value)`을 넘기지만 제네릭은 타입을 넘기는 점이 다르다.

# 장점
* 컴파일 시점에 에러를 찾아서 고칠 수 있다. 
* 타입 안정성이 높아지고, 타입 변환`(casting)`을 하지 않아도 된다.


# 예제
제네릭을 사용하지 않고 타입 캐스팅을 하는 코드[^1]
```java
List list = new ArrayList();
list.add("hello");
String s = (String) list.get(0);
```

제네릭으로 구현한 코드
```java
List<String> list = new ArrayList<String>();
list.add("hello");
String s = list.get(0);   // no cast
```


[^1]: [https://docs.oracle.com/javase/tutorial/java/generics/why.html](https://docs.oracle.com/javase/tutorial/java/generics/why.html)
