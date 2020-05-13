---
title:  "Lombok @Getter,@Setter 사용 (IntelliJ)"
excerpt: "IntelliJ에서 Lombok으로 설정한 @Getter,@Setter에 대해 get/set메소드가 나타나지 않는 경우"

categories:
  - java
tags:
  - java springboot lombok intelliJ
last_modified_at: 
---
## IntelliJ에서 Lombok으로 설정한 @Getter,@Setter @Data에 대해 get/set메소드가 나타나지 않는 경우
     
- IntelliJ에 Lombok Plugin 설치    
Lombok은 Complie시에 get/set method를 생성하므로, IDE에서 개발시에는 get/set메소드를 사용 할 수 없다.   
Project의 mvn or gradle에 lombok 설정을 해 준 후, IntelliJ Preference > Plugins 에서 Lombok을 설치 한 후 재기동 한다.   
Lombok이 검색되지 않는 경우, 당황하지 않고 IntelliJ를 재기동 해 본다.
![](https://github.com/lay126/lay126.github.io/blob/master/assets/images/intellij-lombok-1.png)
    
        
- 객체에 어노테이션 설정               
모델 객체에는 @Data을 지정하여 Lombok 대상임을 명시한다.   
클래스에 @Getter/@Setter를 지정하면 객체 내부 필드에 대해 모두 생성된다. 
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
   
       
-  get/set 메소드 사용   
아래와 같이 자동완성에 get/set메소드가 표시된다. 
![](https://github.com/lay126/lay126.github.io/blob/master/assets/images/intellij-lombok-2.png)

   
#### 추가
이 외에 추가적으로, IntelliJ Preference > Build,Excution,Deploy > Complier > Annotaion Processors 에서 Enable Annotation Processing 이 활성화 되어있는지도 체크해 본다.
