# Scope 阅读路线
- 本节主要围绕 Scope 接口做展开, 分析 Scope 接口的作用和子类实现的细节. 其涉及到的类如下  
    1. `org.springframework.beans.factory.config.Scope`
    2. `org.springframework.web.context.request.AbstractRequestAttributesScope`
    3. `org.springframework.web.context.request.RequestScope`
    4. `org.springframework.web.context.request.SessionScope`
    5. `org.springframework.context.testfixture.SimpleMapScope`
    6. `org.springframework.web.context.support.ServletContextScope`
    7. `org.springframework.context.support.SimpleThreadScope`
    8. `org.springframework.transaction.support.SimpleTransactionScope`
    9. `org.springframework.messaging.simp.SimpSessionScope`
    
    
    
- Scope 接口比较简单, 主要围绕 Scope 去看每个实现类就好了. 

- [Spring-Scope](/docs/beans/Scope/Spring-Scope.md)
- [Spring-AbstractRequestAttributesScope](/docs/beans/Scope/Spring-AbstractRequestAttributesScope.md)
- [Spring-ServletContextScope](/docs/beans/Scope/Spring-ServletContextScope.md)
- [Spring-SimpleMapScope](/docs/beans/Scope/Spring-SimpleMapScope.md)
- [Spring-SimpleThreadScope](/docs/beans/Scope/Spring-SimpleThreadScope.md)
- [Spring-SimpleTransactionScope](/docs/beans/Scope/Spring-SimpleTransactionScope.md)
- [Spring-SimpSessionScope](/docs/beans/Scope/Spring-SimpSessionScope.md)
