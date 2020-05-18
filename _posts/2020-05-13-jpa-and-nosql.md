---
title:  "SPRING-BOOT에서 JPA & MONGODB"
excerpt: "관계형 DB API인 JPA와 비 관계형 MONGODB는 같이 사용할 수 없다."

categories:
  - java
tags:
  - java 
  - spring boot
  - jpa
  - mongodb
last_modified_at: 
---
## SPRING-BOOT, JPA, MONGODB 를 같이 쓰려고 했던 나의 뻘짓
결론부터 이야기하자면, spring-boot에서 jpa와 mongodb를 같이 쓰는것은 권장되지 않는다.   
이유는 관계형DB API인 JPA와 비 관계형DB Nodql 계열인 mongodb는 태생적으로 그 성격이 다르기 때문에 상호 호환성이 맞지 않는다.   
사용이 불가능 한 것은 아니지만, -호환이 가능하다- 정도일 뿐, 권장되는 조합은 아니다.   

특히나 JPA의 장점이 되는 어노테이션을 사용할 수 없으며, 관계형 DB의 Join을 편하게 해주는 JPA의 어노테이션도 사용 하지 않는다.   
ex) @OneToMany, @ManyToMany.... 


이를 인지하지 못하고 약 3일 밤낮을 JPA와 mongodb설정에 쏟아부었다.   


- https://play.google.com/books/reader?id=KdSrDQAAQBAJ&hl=ko&printsec=frontcover&pg=GBS.PA55.w.4.0.12.0.5
- https://brunch.co.kr/@springboot/107
