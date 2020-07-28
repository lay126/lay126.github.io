---
title:  "JAVA8 Stream API"
excerpt: "[책] 가장 빨리 만나는 자바8 - 2장. 스트림 API"

categories:
  - java
tags:
  - java 
  - java8
last_modified_at: 
---

## 스트림
연산의 스케쥴링은 구현체에게 이임.
값들의 묶음을 처리하고 원하는 작업을 지정하는 추상화체.

- Collection, Array, generator, for 에서 Stream을 생성 가능
- 요소 선택 : filter, 요소 변환 : map,limit,distinct, sorted
- 결과 얻기 : Reduction 연산자 (count, max, min, findFirst, findAny) 사용 
- Optinal type : null값을 안전하게 처리. isPresent, orElse를 활용하여 값을 안전하게 사용
- 스트림 결과는 Colletion, Array, String, Map으로 받을 수 있다.
- Collectors의 groupingBy, partitioningBy 메소드는 스트림 내용을 그룹으로 분할하여 준다
- 병렬스트림 사용시엔은 side effect를 조심한다

     
#### Collection과 Stream의 차이점 (Stream기준으로..)
- 스트림은 요소를 보관하지 않음.
- 스트림은 원본을 변경하지 않음. 결과 새로운 스트림으로 반환.
- 스트림 연산은 가능한 지연 처리 된다. - 결과가 필요하기 전까지는 실행되지 않는다 -
- 스트림 연산은 loop문 보다 가독성이 좋다.
- 스트림 연산은 병렬화가 쉽다
