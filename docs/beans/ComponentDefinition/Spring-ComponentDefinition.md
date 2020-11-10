# Spring ComponentDefinition
- 类全路径: `org.springframework.beans.factory.parsing.ComponentDefinition`
- 类图:
    ![ComponentDefinition](./images/ComponentDefinition.png)
- `ComponentDefinition` 是一个接口, 先对其方法进行分析在了解实现类. 


## 方法列表

```java
public interface ComponentDefinition extends BeanMetadataElement {

	/**
	 * 获取名称
	 */
	String getName();

	/**
	 * 获取描述
	 */
	String getDescription();

	/**
	 * 获取bean定义列表
	 */
	BeanDefinition[] getBeanDefinitions();

	/**
	 * 获取内部的 bean定义列表
	 */
	BeanDefinition[] getInnerBeanDefinitions();

	/**
	 * 获取关联的bean定义列表
	 */
	BeanReference[] getBeanReferences();

}
```

## 实现类分析
- [AbstractComponentDefinition](/docs/beans/ComponentDefinition/Spring-AbstractComponentDefinition.md)
    - [CompositeComponentDefinition](/docs/beans/ComponentDefinition/Spring-CompositeComponentDefinition.md)
        - [AspectComponentDefinition](/docs/beans/ComponentDefinition/Spring-AspectComponentDefinition.md)
    - [PointcutComponentDefinition](/docs/beans/ComponentDefinition/Spring-PointcutComponentDefinition.md)
    - [AdvisorComponentDefinition](/docs/beans/ComponentDefinition/Spring-AdvisorComponentDefinition.md)
- [BeanComponentDefinition](/docs/beans/BeanMetadataElement/Spring-BeanComponentDefinition.md)