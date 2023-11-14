# Spring Security_Authorization

- DB와 연동하여(동적) 자원 및 권한을 설정하고 제어
- URL 방식
- Method 방식 (메소드 호출 시) - method, pointcut


## URL


MANAGER - MANAGER_ROLE

ROLE_RESOURCE - RESOURCES(MENU)


- /manager - hasRole("MANAGER")
- Authentication
- FilterInvocation
- AccessDecisionManager (-> AuthorizationManager)


---
- SecurityMetadataSource <- url방식 : FilterInvocationSecurityMetadatSource
- <- 구현 : UrlFilterInvocationSecurityMetadataSource
- 맵 (자원, 권한정보)


https://github.com/spring-projects/spring-security/pull/12328/commits/3cb39c86fb9f8254b85f49d8cea9447f3327a002


---
## PermitAllFilter
- 인증 및 권한심사를 할 필요가 없는 자원
- 