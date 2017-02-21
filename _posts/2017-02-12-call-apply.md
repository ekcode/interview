---
layout: post
title: call()과 apply()는 어떤 차이가 있나요?
---

# call()과 apply()란?
메소드를 호출할 때 this가 가리키는 대상을 지정할 수 있다.

# 차이점
메소드의 파라미터를 전달하는 방식만 다르다. call()은 arguments 객체를 넘기고, apply()는 배열을 넘긴다.

예)
```
call(this, arg1, arg2, arg3)
apply()는 apply(this, [num1, num2, num3])
```
