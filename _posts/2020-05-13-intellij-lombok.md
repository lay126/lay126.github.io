---
title:  "Lombok @Getter,@Setter 사용 (IntelliJ)"
excerpt: "IntelliJ에서 Lombok으로 설정한 @Getter,@Setter @Data에 대해 get/set메소드가 나타나지 않는 경우"

categories:
  - java
tags:
  - java, springboot, lombok, intelliJ
last_modified_at: 
---


```java
@Data
@Getter@Setter
@ToString
public class Menu {

    @Id
    private Long id;
    private String title;

}
```
