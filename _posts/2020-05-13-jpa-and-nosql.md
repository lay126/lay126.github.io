## SPRING-BOOT, JPA, MONGODB 를 같이 쓰려고 했던 나의 뻘짓
결론부터 이야기하자면, spring-boot에서 jpa와 mongodb를 같이 쓰는것은 권장되지 않는다.   
이유는 관계형DB API인 JPA와 논-관계형DB인 mongodb는 그 성격이 다르기 때문인데, 이를 인지하지 못하고 약 3일 밤낮을 JPA와 mongodb설정에 쏟아부었다.   


- https://play.google.com/books/reader?id=KdSrDQAAQBAJ&hl=ko&printsec=frontcover&pg=GBS.PA55.w.4.0.12.0.5
- https://brunch.co.kr/@springboot/107
