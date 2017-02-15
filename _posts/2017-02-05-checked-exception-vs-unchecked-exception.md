---
layout: post
title: checked exception과 unchecked exception은 어떻게 다른가요?
---

# checked exception
* 반드시 예외처리하는 코드를 작성하여야 한다. try/catch/finally로 감싸거나 throws 구문을 사용해 메소드 밖으로 던져야 한다.
* 예외 처리를 하지 않으면 컴파일 에러가 발생한다.
* 정상적인 로직으로 간주한다. 트랜잭션 처리 중에 checked exception이 발생하더라도 rollback되지 않는다.[^1]
* 예외 처리가 반드시 필요하다고 판단될 때 사용한다.

# unchecked exception
* 자바에서는 RuntimeException을 상속받았을 경우 unchecked exception이 된다.
* 예외처리를 명시적으로 할 필요 없다.
* 런타임 시점에 에러가 발생한다.
* 예상하지 못한 예외이기 때문에 트랜잭션 중간에 unchecked exception이 발생하면 rollback 된다.

# 언제 사용해야 하나
* 어떤 예외 상황에 대해 클라이언트가 처리해야할 책임이 있다면 checked exception을 사용해야 한다.
* 예외가 발생했을 때 클라이언트가 특별히 처리할 수 없다면 unchecked exception을 사용해야 한다. 대부분의 예외 상황이 여기에 해당된다.


[^1]:[http://www.nextree.co.kr/p3239/](http://www.nextree.co.kr/p3239/)
