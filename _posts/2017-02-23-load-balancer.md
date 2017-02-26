---
layout: post
title: 로드 밸런서의 역할
---
 
가장 기본적인 기능은 부하 분산이다. 클라이언트의 요청을 스케줄링 알고리즘에 따라 여러 서버에 분산시킨다.
그리고 클라이언트는 직접적으로 백엔드-서버`Backend-server`에 요청을 할 수 없다. 즉, 백엔드-서버의 시스템 구성을 클라이언트 입장에서는 알지 못한다.  

이 밖에도 벤더에 따라 차이는 있지만 아래와 같은 기능을 기본적으로 제공한다.[^1]

* 특정 서버의 가중치를 높혀서 성능이 좋은 서버에 요청을 더 많이 보낼 수 있다.
* SSL 암호화/복호화 연산을 처리함으로서 서버의 부담을 줄인다.
* DDos와 같은 공격으로부터 서버를 보호하는 역할을 한다.
* gzip 압축을 통해서 응답시간을 줄일 수 있다.
* 캐시 서버 역할을 수행한다.
* Health checking을 통해 장애가 발생한 서버를 서비스에서 제외한다.
* 방화벽`firewall` 역할을 한다.


[^1]:[https://en.wikipedia.org/wiki/Load_balancing_(computing)](https://en.wikipedia.org/wiki/Load_balancing_(computing))
