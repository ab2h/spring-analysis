# Spring StringValueResolver 阅读路线
- 本节主要围绕接口 `StringValueResolver` 作为展开, 介绍其实现类的实现细节. 这个接口作用为字符串解析. 阅读时主要围绕类图进行了解. 
    - [StringValueResolver](images/StringValueResolver.png)
    
- 实现类分析:
    1. [Spring-EmbeddedValueResolver](/docs/utils/StringValueResolver/Spring-EmbeddedValueResolver.md)
    1. [Spring-PlaceholderResolvingStringValueResolver](/docs/utils/StringValueResolver/Spring-PlaceholderResolvingStringValueResolver.md)
    1. [Spring-StaticStringValueResolver](/docs/utils/StringValueResolver/Spring-StaticStringValueResolver.md)
    
- 在 Spring 中与 `StringValueResolver` 关联性比较强的有 `env.propertyResolver` Spring 环境属性解析. 
    有类似从 java 环境中读取 java.home 等行为的解析详细请查看[Spring-env-PropertyResolver](/docs/env/PropertyResolver/Readme.md)
    
    
    