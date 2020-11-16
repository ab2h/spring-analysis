# Spring BeanFactory 阅读指南
- **BeanFactory** 主要用来访问 Spring Bean 容器, 它作为访问容器的根接口. 有很多拓展的接口. 
    - `org.springframework.beans.factory.HierarchicalBeanFactory`
    - `org.springframework.beans.factory.ListableBeanFactory`
    - `org.springframework.beans.factory.config.ConfigurableBeanFactory`
    - `org.springframework.context.ApplicationContext`
    - ...
    
- 本节将围绕 `BeanFactory` 接口展开. 介绍 BeanFactory 系列接口. 