# QueryDslRepository 구조
## Spring Data Repository와 QueryDsl Repository 분리

### UserRepository : Spring Data Repository
```java
interface UserRepository extends JpaRepository<User,Long>
```
<br>

### UserQueryRepository : QueryDsl Repository
```java
public class UserQueryRepository {
    private final JPAQueryFactory jpaQueryFactory;
}
```
- JPAQueryFactory Bean 등록
```java
import com.querydsl.jpa.impl.JPAQueryFactory;
import jakarta.persistence.EntityManager;
import jakarta.persistence.PersistenceContext;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class QuerydslConfig {
    @PersistenceContext
    private EntityManager entityManager;

    @Bean
    public JPAQueryFactory jpaQueryFactory() {
        return new JPAQueryFactory(entityManager);
    }

}
```