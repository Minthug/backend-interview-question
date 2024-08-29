1. RESTful API 개발:
    "Spring Boot를 사용하여 RESTful API를 개발한 경험이 있나요? 
        - CRUD 작업을 위한 엔드포인트 설계, 요청/응답 처리, 그리고 예외 처리는 어떻게 구현했나요? 
        - @RestController와 @RequestMapping 어노테이션의 활용 방법에 대해 설명해주세요."
        네 RESTful 원칙에 따라 엔드포인트를 설계했습니다.
        GET, POST, PATCH, DELETE로 조회, 생성, 정보 업데이트를 위한 patch, 사용자 삭제 등에 Delete 이렇게
        HTTP method와 URI를 조합해 직관적인 API를 구성했습니다.

        @RestController 어노테이션을 사용해 컨트롤러를 정의하고 각 엔드포인트에 맞는 메서드를 구현했습니다.
        데이터는 @RequestBody, @PathVariable 등을 통해 사용해 데이터를 받았고, 응답은 ResponseEntity 를 통해 상태 코드와 함께 반환했습니다.

2. 데이터베이스 연동:
    "Spring Data JPA를 사용하여 데이터베이스와 연동하는 프로젝트를 진행했다면, 엔티티 설계와 리포지토리 구현 과정에 대해 설명해주세요. 
        - N+1 문제를 어떻게 해결했나요? 복잡한 쿼리의 경우 어떤 방식으로 처리했나요?"

        네 
        엔티티 설계 시에는 도메인 모델을 기반으로 JPA 어노테이션을 활용해서 관계 설정 시 
        @OneToMany, @ManyToOne등을 사용해 엔티티간의 관계를 명확히 표현했습니다.

        리포지토리의 경우엔 Data JPA의 JpaRepository를 확장해 기본적인 CRUD 작업을 쉽게 구현했습니다.

        N+1 문제는 JPQL의 Join fetch를 사용해 N+1 문제를 해결했습니다.

        복잡한 쿼리 같은경우 @Query 어노테이션을 사용해 복잡한 쿼리를 직접 작성해 제목 검색 기능 등을 작성했습니다.
    3. 보안 구현:
        "Spring Security를 사용하여 인증과 인가를 구현한 경험이 있나요?
            - JWT를 이용한 토큰 기반 인증을 구현하는 과정 
            - 역할 기반의 접근 제어(RBAC)를 설정하는 방법에 대해 설명해주세요."
            
            JWT를 이용한 토큰 기반 인증을 구현하기 위해 Auth0의 java-jwt 라이브러리를 사용했습니다.
            의존성을 추가하고 유틸리티 클래스를 구현하고 인증 필터 등을 넣고 security 설정을 했습니다.

            위 라이브러리의 장점은 JWT 생성 및 검증을 쉽게 할 수 있으며 보안성이 높고 커스터마이징이 용이한 장점을 갖고 있어 활용해서 프로젝트를 진행했습니다.

            역할 기반의 접근 제어를 설정하는 방법은 
            Spring security를 사용해 RBAC를 구현했는데
            ENUM 클래스에 ROLE_USER 와 ADMIN을 두 가지 주요 역할을 정의했습니다.
            URL 기반 securityFilterChain을 구성해 URL 패턴별로 접근 권한을 설정했습니다.

            또한 HTTP 메서드별 권한 설정을 했는데 각 메서드에 따라 다른 권한을 부여해주었고

            소셜 로그인을 위해 OAuth2 설정도 포함했습니다.
            