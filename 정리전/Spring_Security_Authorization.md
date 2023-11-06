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
- 