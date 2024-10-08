1. JPA는 무엇인가?

JPA는 ORM 기반의 자바 API입니다
JPA는 개발자는 데이터베이스 작업보단 비즈니스 로직 처리 작업에 더욱 집중할 수 있게 해주며
객체 지향적인 방식으로 데이터베이스를 다룰 수 있게 돕고 DB 스키마 변경에 유연하게 대응할 수 있으며 개발 생산성과 유지 보수성을 높이는데 도움을 줍니다.

```
⚙️ 구체적으로 어떤 도움을 주는가 ?
엔티티 매핑이나 JPQL, 캐싱 등에 도움을 주고 있습니다.
```

2. Spring IoC(Inversion of Control)와 DI(Dependency Injection)에 대해 설명해주세요. 
이들이 왜 중요하며 어떤 장점을 제공하나요? 
⭐️ 왜 사용하는가? ⭐️
> 코드 간소화를 통해 비즈니스 로직에 집중할 수 있게 돕고 의존성을 쉽게 테스트 할 수 있게 되어 단위 테스트가 쉬워집니다.
기존 코드를 변경하지않고 새로운 기능을 추가할 수 있어 확장성과 객체간의 낮은 결합도를 챙겨 유지보수와 확장서에 좋습니다.

Ioc란 제어의 역전을 뜻하는데 프로그램의 흐름을 개발자가 아닌 프레임워크가 관리하는 소프트웨어 디자인 원칙입니다.

DI란 Ioc가 구현하는 실제적인 방법이며,
객체가 필요롤 하는 의존성을 외부에서 주입하는 구체적인 메커니즘입니다.

DI는 정적, 동적 의존관계가 있는데 정적은 import만 보고 클래스의 관계를 판단이 가능하고
동적은 코드가 실행하기 전까지 의존 관계를 알수 없습니다. 

Ioc가 더 넓은 개념이고 DI는 더 세부적인 개념입니다.

중요성과 장점은 
낮은 결합도, 테스트 용이성, 코드 재사용성, 관심사의 분리가 있습니다.


3. Spring Bean이란 무엇이며, Bean의 생명주기에 대해 설명해주세요. Bean의 스코프 종류와 각각의 특징도 언급해주세요.
스프링 특징에 IoC 제어의 역전이 있습니다.
Bean 이전에는 사용자가 직접 new 연산을 통해 객체를 생성하고 메서드를 호출했습니다
IoC가 적용되고 이런 객체 생성과 사용자의 제어권을 스프링에게 넘겨서
사용자는 직접 new 를 이용해 생성한 객체를 사용하는것이 아닌 스프링에 의해 관리 받는 자바 객체를 사용합니다. 이를 Bean이라 합니다.

빈의 생명주기는
스프링 컨테이너 생성 > 스프링 빈 생성 > 의존 관계 주입 > 초기화 콜백 > 사용 > 소멸전 콜백 > 스프링 종료 
으로 되고 있습니다.

스코프 종류와 특징으론
Singleton 
기본스코프이며 스프링 컨테이너당 하나의 인스턴스만 생성한다이며 모든 요청이 같은 인스턴스를 공유합니다.

prototype   
요청할때마다 새로운 인스턴스를 생성하며, 독립적인 상태가 필요한 경우에 사용합니다

request
HTTP 요청당 하나의 인스턴스를 생성합니다. 웹어플리케이션에 사용됩니다

session
HTTP 세션당 하나의 인스턴스를 생성하며 웹어플리케이션의 사용자별 데이터 관리에 사용됩니다.

application
servletContext 당 하나의 인스턴스를 생성하며 웹 어플리케이션 전체에서 공유되는 데이터를 사용합니다.

websocket
웹소켓 세션당 하나의 인스턴스를 생성합니다.

4. Spring AOP(Aspect-Oriented Programming)란 무엇인가요? AOP의 주요 개념(Aspect, Advice, Pointcut, Join Point)에 대해 설명하고, 어떤 상황에서 유용하게 사용될 수 있는지 예를 들어주세요.

AOP는 관점 지향 프로그래밍이라고 불리며 어떤 로직을 기준으로 핵심적인 관점, 부가적인 관점으로 나뉘어 보고 관점을 기준으로 각각 모듈화하겠다는 것 입니다.

AOP 주요 개념은
Aspect
여러 클래스에 걸쳐 있는 공통 관심사를 모듈화 하는 것입니다
Advice
조인포이트에서 Aspect가 취할 동작입니다
Pointcut
실제로 aspect를 적용할 조인포인트를 선별하는 표현식입니다.
Join Point
프로그램 실행 중 aspect 를 적용하는 지점입니다.

AOP는 다양한 상황에서 사용되는데 로깅, 트랜잭션 관리, 보안 및 인증이 있는데
로깅을 통해 애플리케이션 전반에 걸쳐 일관된 로깅을 적용하고, 트랜잭션은 @Transaction 어노테이션으로 간단히 활용함으로써 
데이터베이스 트랜잭션을 시작, 커밋, 롤백하는 로직을 분리할 때 등에 있으며 보안 및 인증은 Spring Security 에서 AOP 개념을 사용합니다.

5. Spring MVC 아키텍처에 대해 설명해주세요. DispatcherServlet의 역할과 요청 처리 흐름에 대해 자세히 설명해주세요.

MVC 아키텍쳐는 Model View Controller로 
Model은 DB와 상호작용하며 비즈니스 로직을 처리하는 모듈 입니다
View는 클라이언트에게 보여지는 결과화면을 처리하는 모듈이고 
Controller는 클라이언트 요청이 들어오면 그 입력을 처리하고
어떤 로직을 실행시킬 것인지 제어하는 모듈의 역할을 합니다.

DispatcherServlet은 front Controller로도 불리고 있습니다.
'/' 경로에 매핑하여 들어오는 모든 요청을 처리하는 역할을 맡고있는데
Mapping 어노테이션을 활용해 매핑해놓은 컨트롤러의 메소드로 요청을 전달해주는 방식입니다.

DispatcherServlet가 클라이언트 요청을 받고 (중앙 제어실)
핸들러매핑이 알맞은 컨트롤러를 찾습니다
그리고 핸드매핑을 실행할 컨트롤러 메서드를 찾습니다
컨트롤러의 메서드를 실행하여 그 결과 모델로서 DispatcherServlet 반환
뷰리졸버는 알맞은 JSP 파일을 찾습니다.
뷰는 JSP 파일을 모델의 정보를 토대로 클라이언트에게 반환합니다

6. Spring에서 트랜잭션 관리는 어떻게 이루어지나요? 선언적 트랜잭션과 프로그래밍적 트랜잭션의 차이점과 각각의 사용 방법에 대해 설명해주세요.

선언적 트랜잭션 관리, 프로그래밍 방식 트랜잭션, 트랜잭션 속성 설정, 트랜잭션 관리자 설정 등이 있습니다.

선언적 트랜잭션은 어노테이션을 사용하는 방식과 XML 설정을 통한 레거시 방식이 있습니다.
대게 어노테이션 방식을 사용합니다
선언적 트랜잭션은 비즈니스 로직과 트랜잭션 처리 로직을 분리하고있는데 그로인한
코드 간결성과 유지 보수에 큰 강점을 갖고 있습니다.
간단하고 명확한 그리고 대부분 일반적이 상황에서 선언적 트랜잭션을 사용합니다

프로그래밍적 트랜잭션은 트랜잭션 경계를 프로그래밍적으로 직접 설계해야합니다.
물론 더 세밀한 트랜잭션 제어가 가능한 점이 있습니다.
그로 인한 코드의 복잡해질 수 있는 단점을 갖고 있습니다.
트랜잭션의 경계를 동적으로 결정해야할 때 더 세밀한 제어가 필요할 때, 특정 조건에 따라 트랜잭션 동작을 변경할 때 사용합니다.


7. Spring Security의 주요 특징과 인증(Authentication) 및 인가(Authorization) 처리 방식에 대해 설명해주세요.

Spring security의 주요 특징으로는 포괄적인 보안 솔루션, 유연한 설정, 다양한 인증 방식을 지원하고 세션관리와 CSRF, XSS등 웹 보안 위협 대응이 있습니다.

인증 처리 방식은 사용자가 누구인지에 확인 과정입니다.
사용자가 아이디와 패스워드를 입력하면 (credentials)
AuthenticationManager가 인증 검증 한 뒤
성공 시 인증 된 사용자 정보를 SecurityContext에 저장합니다.

인가 처리 방식은 인증된 사용자가 특정 리소스에 접근할 권한이 있는지 확인하는 과정인데
인증된 사용자가 특정 URL로 접근하려고 할 때, AccessDecisionManager가 해당 사용자의 권한과 리소스에 필요한
권한 비교하여 접근 가능 여부를 결정합니다.

```
JWT와 spring security에 대해 설명하고
어떻게 사용했는지 설명하기
상태 비저장 인증, 보안 강화, 성능 최적화 , 크로스 도메인 인증

어케 사용 ?
사용자 로그인 시 JWT 토큰 생성 생성된 토큰은 클라이언트에게 반환되어 이후 요청의 Authorization 헤더에 포함
커스텀 필터를 구현해 시큐리티 필터 체인에 추가
매 요청마다 JWT 토큰을 검증 후 유효한 경우 Authentication 객체 생성 SecurityContext 설정

Access Refresh Token 으로 액세스 만료시 리프레시를 사용해 새로운 Access Token 발급받는 프로세스 구현
또한 토큰 만료 시간을 적절히 설정해 보안 강화 및 HTTPS 사용해 토큰 전송시 암호화
```


8. Spring Boot란 무엇이며, Spring Framework와의 주요 차이점은 무엇인가요? Spring Boot의 자동 구성(Auto-configuration) 원리에 대해 설명해주세요.

Spring boot는 독립적이고 실행 가능한 Spring 기반 어플리케이션을 쉽게 만들 수 있게 해주는 프레임워크입니다.
복잡한 설정 없이 빠르게 Spring 애플리케이션을 개발하고 실행할 수 있게 해주는 도구라고 생각하면 좋습니다.

-> 주요 차이점은
크게 설정의 복잡성, 서버, 의존성, 유연성, 마이크로서비스, 학습곡선 등이 있습니다.
핵심적으로 boot는 자동 구성, 의존성 관리 최소화, 내장 서버 제공이 있으며 개발 방식 역시 어노테이션 기반의 설정과 
대부분의 설정이 자동으로 처리되어 빠른 개발이 가능합니다.

framework는 XML 기반에 Java 설정 클래스가 필요하고 서버, 데이터베이스 수동 연결과 수동으로 구성해야하는 점
모든 의존성을 직접 관리해야합니다. 물론 세밀한 작업이 가능하지만 개발자의 작업 너무 많이 생기는 점이 있습니다.

자동 구성 원리는 조건부 구성과 우선순위의 핵심 개념을 가지고 있습니다.
애플리케이션이 시작 시 @EnableAutoConfiguration을 감지하고 Spring.factories파일에서 구성 클래스 목록을 로드
각 자동 구성 클래스의 조건을 평가하고 조건 만족 시 해당 구성 적용 합니다.


9. Spring Data JPA란 무엇인가요? 
JPA와 Hibernate와의 관계, 그리고 Spring Data JPA가 제공하는 주요 기능들에 대해 설명해주세요.

Data JPA는 기존 JPA를 한 단계 더 추상화 시켜 개발 용이성을 상당히 올려주는 인터페이스입니다.
Data Jpa는 repository라는 인터페이스를 제공주는데
사용자가 레포지토리 인터페이스에 정해진 규칙대로 메서드를 입력하면, 스프링이 알아서 해당 메서드에 적합한 쿼리를 날리는
구현체를 만들어 Bean으로 등록해줍니다.

Hibernate는 JPA의 구현체 입니다.
JPA와 hibernate는 마치 자바의 인터페이스와 해당 인터페이스를 구현한 클래스와 같은 관계입니다.

Data JPA제공하는 주요기능은
앞서 언급한 Repository 인터페이스와 메서드 이름을 통한 쿼리 생성
페이징, 정렬과 @Query 어노테이션, Auditing, Specification, 관계 매핑, 쿼리 결과 매핑, 커스텀 Repository 구현
이 있습니다.

Repo인터페이스는 기본적인 CRUD 연산을 위한 메서드 자동 구현 (CrudRepo, JpaRepo)
사용자가 레포지토리 인터페이스에 정해진 규칙대로 메서드를 입력하면, 스프링이 알아서 해당 메서드에 적합한 쿼리를 날리는
구현체를 만들어 Bean으로 등록

@Query 어노테이션은 복잡한 쿼리를 직접 정의 기능 제공하고

어노테이션을 이용한 자동 시간 기록, 동적 쿼리 생성을 위한 인터페이스 제공, @OneToMany 같은 엔티티 간의 관계 정의
클래스 기반의 DTO 프로젝션와 인터페이스 기반의 프로젝션을 제공하고 커스텀 레포 구현을 통한 특정 레포지토리에 사용자 정의 구현 기능 등이 있습니다.

10. @Controller, @Service, @Repository 어노테이션의 차이점과 각각의 역할에 대해 설명해주세요. 이들이 어떻게 Spring의 레이어드 아키텍처를 구현하는 데 도움이 되나요?

일단 컨트롤러 서비스 레포지토리 어노테이션은 큰 차이점에 대해선
위치하는 계층에 대해 먼저 말씀드리겠습니다.
컨트롤러는 프레젠테이션 계층에
즉, 최상위 계층에 위치하고 서비스는  중간인 비즈니스 계층 레포지토리는 최하위 데이터 계층에 위치합니다.

또한 주요 역할은 컨트롤러는 웹 요청과 응답을 처리하고 URL 매핑 및 뷰 반환 처리 중점을 두며
서비스는 비즈니스 로직 처리와 트랜잭션 관리에 중점이 있고 레포지토리는 데이터 접근 로직 처리와 데이터베이스 연산 중점이 있습니다.

의존성 주입 패턴의 차이도 있는데 
@컨트롤러는 @서비스에 의존하고 @서비스는 @레포지토리에 의존 @레포지토리는 일반적으로 다른 스프링 컴포넌트에 의존하지 않아서
이 패턴은 계층간 단방향 의존성을 강제합니다.


AOP 적용 차이으로도 큰 차이가 있습니다
컨트롤러는 주로 로깅과 보안 관련 AOP이고 서비스는 트랜잭션 관리 AOP, 레포지토리는 주로 성능 모니터링 관련 AOP 입니다.

레이어드 아키텍처를 구현하는데 크게 도움을 주게됩니다.
특히 의존성 주입 패턴과 각 어노테이션이 위치하는 계층으로 인해 각 계층은 제 위치에서 책임에만 집중하고 의존성 단방향은 일관성을 유지하게 됩니다.


11. Spring의 프로파일(Profile) 기능은 무엇이며 어떤 상황에서 유용하게 사용될 수 있나요? 프로파일을 설정하고 활성화하는 방법에 대해 설명해주세요.
특정 환경이나 상황에 따라 다른 Bean 설정 이나 속성을 적용할 수 있게 해주는 기능입니다
개발 테스트 운영 환경별 다른 설정 적용해 각 환경에 맞는 상황 맞게 사용함으로써 개발부터 배포까지 과정을 더 유연하고 관리하기
쉽게 만들어 유용하게 사용할 수 있습니다.

프로파일 설정하고 활성하는 방법은 
프로그래밍적 방식으로 JVM 옵션에 할당하는 방법과 application.properties와 환경변수를 사용하는 방식 등이 있고
XML 설정하는 방식과 자바 설정으로 config 클래스에 @Profile 어노테이션을 자바 설정하는 방식이 있습니다.

사용해본적있나요 ?
local과 prod 프로파일 설정으로 적용해 
개발 단계에서는 관계없지만 운영 단계에서 사용자에게 불필요한 노출을 줄이기 위해 yml파일을 수정해서 사용했습니다.
