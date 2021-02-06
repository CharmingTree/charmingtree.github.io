---
layout: post
title: JAVA 일반적인 프로그래밍 원칙 정리 Effective Java
hide_title: false 
bootstrap: true                                   # Add bootstrap to the page
tags: [Java] [Java StdLib]
---
## JAVA Standard Library 

#### <br/>

<br/>

## NavigableMap 분석

* 지정된 타겟으로 가장 가까운 요소를 반환한다

* sortedMap의 확장 인터페이스 메소드가 구현되어 있다

* 오름차순, 내림차순 퍼포먼스는 대게 오름차순이 빠르다

  

## Method 

#### lowerEntry

```java
Map.Entry <K,V> lowerEntry(K key)
```

##### 지정된 키보다 작은 키중에서 제일 큰 엔트리 반환한다. 키가 존재 하지 않을 경우는 null을 반환한다.

***

#### lowerKey

```java
K lowerKey(K key)
```

##### 지정된 키보다 작은 키중에 제일 큰 키를 반환한다. 키가 존재 하지 않을 경우 null을 리턴한다.

***

#### floorEntry

```java
Map.Entry <K,V> floorEntry(K key)
```

##### 지정된 키와 같거나 작은 엔트리를 반환한다. 키가 존재 하지 않을 경우는 null을 반환한다.

***

#### floorKey

```java
K floorKey(K key)
```

##### 지정된 키와 같거나 작은 키를 반환한다. 키가 존재 하지 않을 경우 null을 리턴한다.

***

#### ceilingEntry

```java
Map.Entry <K,V> ceilingEntry(K key)
```

##### 지정된 키와 같거나 큰 엔트리를 반환한다. 키가 존재 하지 않을 경우 null을 리턴한다.

***

#### ceilingKey

```java
K ceilingKey(K key)
```

##### 지정된 키와 같거나 큰 키를 반환한다. 키가 존재 하지 않을 경우 null을 리턴한다.

***

#### higherEntry

```java
Map.Entry <K ,V > higherEntry(K  key)
```

##### 지정된 키보다 다음으로 큰 키에 대한 엔트리를 반환한다. 키가 존재 하지 않을 경우 null을 리턴한다.

***

#### higherKey

```java
K  higherKey(K  key)
```

##### 지정된 키보다 다음으로 큰 키에 대한 키를 반환한다. 키가 존재 하지 않을 경우 null을 리턴한다.

***

#### firstEntry

```java
Map.Entry <K ,V > firstEntry()
```

##### 맵 내에 최소의 키를 가지는 엔트리를 반환한다.  이 맵이 empty인 경우 null을 반환한다.

***

#### lastEntry

```java
Map.Entry <K ,V > lastEntry()
```

##### 맵 내에 최대의 키를 가지는 엔트리를 반환한다. 이 맵이 empty인 경우 null을 반환한다.

***

#### pollFirstEntry

```java
Map.Entry <K ,V > pollFirstEntry()
```

##### 맵 내에서 최소의 키를 가지는 엔트리를 반환하고 맵내에서 해당 키맵핑 요소를 삭제한다. 이 맵이 empty인 경우 null을 반환한다.

***

#### pollLastEntry

```java
Map.Entry <K ,V > pollLastEntry()
```

##### 맵 내에서 최대의 키를 가지는 엔트리를 반환하고 맵내에서 해당 키맵핑 요소를 삭제한다. 이 맵이 empty인 경우 null을 반환한다.

***

#### descendingMap

```java
NavigableMap <K ,V > descendingMap()
```

##### 맵내 요소를 역순의 뷰를 리턴한다. 

***

navigableKeySet

```
NavigableSet <K > navigableKeySet()
```

이 맵에 포함된 navigableSet 뷰를 리턴합니다. Set의 반복자는 오름차순이다. 맵에 변경은 현재 Set에 반영되고, 세트에 대한 변경 역시 맵에 반영된다. 

***

#### descendingKeySet

```java
NavigableSet <K > descendingKeySet()
```

##### 이 맵에 포함된 키의 역순서 navigableSet 뷰를 리턴합니다. 맵에 변경은 현재 Set에 반영되고, Set에 대한 변경 역시 맵에 반영된다.

***

#### subMap

```java
NavigableMap <K ,V > subMap(K  fromKey,
                         boolean fromInclusive,
                         K  toKey,
                         boolean toInclusive)
```

##### 맵의 fromKey ~ toKey의 키 범위를 가지는 부분의 뷰를 리턴합니다. fromKey와 toKey가 동일한 경우, emptyMap을 반환한다. fromInclusive가 true면 open(fromKey포함), false면 close(fromKey 미포함),  toInclusive가 true면 open, false면 close다. 반환되는 맵은 원본과 연결되어 있기 때문에 변경될 경우 원본까지 변경 된다. 반환된 맵에 key 범위외의 키가 삽입되거나, from이 to보다 큰경우 또는 원본 맵의 범위를 초과하는 경우 IllegalArgumentException을 throw 한다.

***

#### headMap

```java
NavigableMap <K ,V > headMap(K  toKey,
                          boolean inclusive)
```

##### toKey보다 작은 범위의 맵의 뷰를 리턴합니다. inclusive가 true일경우 toKey까지 포함된 범위를 반환한다. 반환되는 맵은 원본을 참조하기 때문에 변경이 일어날 경우 원본까지 변경되니 주의해야 한다.

***

#### tailMap

```java
NavigableMap <K ,V > tailMap(K  fromKey,
                          boolean inclusive)
```

##### fromKey보다 큰 범위의 맵의 뷰를 리턴합니다. inclusive가 true일 경우 fromKey까지 포함된 범위를 반환한다. 반환되는 맵은 원본을 참조하기 때문에 변경이 일어날 경우 원본까지 변경되니 주의해야 한다.

***

#### subMap

```java
SortedMap <K ,V > subMap(K  fromKey,
                      K  toKey)
```

##### 맵의 fromKey(open) ~ toKey(close)의 키 범위를 가지는 부분의 뷰를 반환한다. fromKey와 toKey가 동일한 경우 emptyMap을 반환한다. 반환되는 맵은 원본을 참조하기 때문에 변경될 경우 원본까지 변경되니 주의해야 한다.

##### subMap(fromKey, true, toKey, false) 와 등가이다. 

##### 리턴타입이 SortedMap인 점이 다르다

***

headMap

```java
SortedMap <K ,V > headMap(K  toKey)
```

##### 맵의 toKey보다 작은 키를 가지는 부분의 뷰를 반환한다. 반환되는 맵은 원본을 참조하기 때문에 변경될 경우 원본까지 변경되니 주의해야 한다. toKey 범위 외의 키를 삽입하려고 하면 오류가 발생한다.

##### headMap(toKey, false)와 등가이다.

***

#### tailMap

```java
SortedMap <K ,V > tailMap(K  fromKey)
```

##### 맵의 fromKey 이상의 키를 가지는 부분의 뷰를 반환한다. 반한되는 맵은 원본을 참조하기 때문에 변경될 경우 원본까지 변경되니 주의해야 한다. fromKey 범위 외의 키를 삽입하려고 하면 오류가 발생한다.

##### tailMap(fromKey, true)와 등가이다.



