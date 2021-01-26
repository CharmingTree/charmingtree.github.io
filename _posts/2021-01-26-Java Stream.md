---
layout: post
title: 자바 스트림 Java Stream
hide_title: false 
bootstrap: true                                   # Add bootstrap to the page
tags: [Java]
---

이펙티브 자바 스트림에 관해 읽고서 정리
* 스트림 파이프라인은 지연 평가(lazy evaluation) 이다.
* 스트림 API는 메서드 연쇄를 지원하는 플루언트(Fluent)다. e.g) Instance.chainMethod1().chainMethod2()..... 



### 스트림을 사용하기 좋은 상황은 대략 이 정도.
* 원소들의 시퀀스를 일관되게 변환한다.
* 원소들의 시퀀스를 필터링 한다.
* 원소들의 시퀀스를 하나의 연산을 사용해 결합한다(더하기, 연결하기, 최솟값 구하기 등)
* 원소들의 시퀀스를 컬렉션에 모은다 (공통된 속성을 기준으로 묶는다)
* 원소들의 시퀀스에서 특정 조건을 만족하는 원소를 찾는다.
