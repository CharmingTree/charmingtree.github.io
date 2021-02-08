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
<br/>
--------
<br/>
<br/>
### 스트림을 사용하기 좋은 상황은 대략 이 정도.
* 원소들의 시퀀스를 일관되게 변환한다.
* 원소들의 시퀀스를 필터링 한다.
* 원소들의 시퀀스를 하나의 연산을 사용해 결합한다(더하기, 연결하기, 최솟값 구하기 등)
* 원소들의 시퀀스를 컬렉션에 모은다 (공통된 속성을 기준으로 묶는다)
* 원소들의 시퀀스에서 특정 조건을 만족하는 원소를 찾는다.

### 특정 K/V 여부 확인 

```java
boolean isPotnVia = coList.stream().anyMatch((s)->{
            return s.get("opcode").equals("CREATE") && s.get("metypea").toString().startsWith("P"); 
        });
```

<br/>

--------

<br/>

### 특정 K/V 개수 확인

```java
long swCnt = coList.stream().filter((s)->{
           if (s.get("opcode").equals("CREATE"))
           {
               return s.get("switchyn").equals("Y") ? true : false;
           }
           else {
               return false;
           }
        }).count();
```

<br/>

------

<br/>

### 요소 문자열 연결

```java
Optional<Object> resultOrderList = orderList.stream().sorted().reduce((s1, s2) -> s1 + ", " + s2);
        resultOrderList.ifPresent(System.out::println);
```

<br/>

-----

<br/>

### List\<Map\> 형태 groupby 하기

```java
logger.info("{}", coList.stream().collect(Collectors.groupingBy((map)-> map.get("opcode"))).entrySet());
```

</br>





