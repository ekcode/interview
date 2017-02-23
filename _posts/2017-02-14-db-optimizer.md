---
layout: post
title: 오라클 옵티마이저에 대해서
---

오라클 옵티마이저는 CBO`(Cost-Based Optimizer)`와 RBO`(Rule-Based Optimizer)` 두 종류가 있다. 통계 정보가 있으면 CBO, 없으면 RBO를 사용한다.[^1] 오라클11g 이후부터는 CBO만 지원을 한다. 

옵티마이저가 항상 잘 동작하지는 않는다. 옵티마이징에 필요한 모든 팩터들을 옵티마이저가 완벽하게 분석할 수는 없으며, 하드웨어 성능에 따라서도 실행계획에 차이가 발생할수 있다. 또한 통계정보 자체가 부정확하다면 최적의 실행계획을 수립할 수 없다.[^2]

옵티마이저가 항상 최선의 계획을 수립할 수 없으므로 테이블이나 인덱스의 실행계획을 개발자가 직접 바꿔야할 필요가 있는데 이때 사용되는 것이 힌트(Hint)이다.

[^1]:[http://www.oraclejavanew.kr/bbs/board.php?bo_table=LecOrccleTun&wr_id=80](http://www.oraclejavanew.kr/bbs/board.php?bo_table=LecOrccleTun&wr_id=80)
[^2]:[http://www.dbguide.net/db.db?cmd=view&boardUid=148218&boardConfigUid=9&categoryUid=216&boardIdx=139&boardStep=1](http://www.dbguide.net/db.db?cmd=view&boardUid=148218&boardConfigUid=9&categoryUid=216&boardIdx=139&boardStep=1)
