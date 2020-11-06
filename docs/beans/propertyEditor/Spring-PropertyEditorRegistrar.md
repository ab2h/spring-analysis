<!--
  ~
  ~ Copyright 2020 HuiFer All rights reserved.
  ~
  ~ Licensed under the Apache License, Version 2.0 (the "License");
  ~ you may not use this file except in compliance with the License.
  ~ You may obtain a copy of the License at
  ~
  ~      http://www.apache.org/licenses/LICENSE-2.0
  ~
  ~ Unless required by applicable law or agreed to in writing, software
  ~ distributed under the License is distributed on an "AS IS" BASIS,
  ~ WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  ~ See the License for the specific language governing permissions and
  ~ limitations under the License.
  ~
  -->
# Spring  PropertyEditorRegistrar

- 类全路径: `org.springframework.beans.PropertyEditorRegistrar`
- `PropertyEditorRegistrar` 接口 通过`PropertyEditorRegistry` 将`PropertyEditor`注册到容器





```java
public interface PropertyEditorRegistrar {

   /**
    * Register custom {@link java.beans.PropertyEditor PropertyEditors} with the given {@code
    * PropertyEditorRegistry}.
    * <p>The passed-in registry will usually be a {@link BeanWrapper} or a
    * {@link org.springframework.validation.DataBinder DataBinder}.
    * <p>It is expected that implementations will create brand new
    * {@code PropertyEditors} instances for each invocation of this method (since {@code
    * PropertyEditors} are not threadsafe).
    * 属性编辑器注册方法
    *
    * @param registry the {@code PropertyEditorRegistry} to register the custom {@code
    *                 PropertyEditors} with
    */
   void registerCustomEditors(PropertyEditorRegistry registry);

}
```





详细实现方法请查看子类： [ResourceEditorRegistrar](/docs/beans/propertyEditor/Spring-ResourceEditorRegistrar.md)