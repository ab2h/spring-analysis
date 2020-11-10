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

# Spring propertyEditor 阅读路线
• 本节主要围绕属性编辑器做展开. 其涉及到的类
1. org.springframework.beans.PropertyEditorRegistrar
2. org.springframework.beans.PropertyEditorRegistry
3. org.springframework.beans.support.ResourceEditorRegistrar
4. org.springframework.beans.PropertyEditorRegistrySupport
5. 其他
## 阅读路线
从`org.springframework.beans.PropertyEditorRegistry` 作为第一个入口. 
紧接着了解它的实现类`org.springframework.beans.PropertyEditorRegistrySupport`
在上述类了解后关注 `org.springframework.beans.PropertyEditorRegistrar` 并且了解其实现类 `org.springframework.beans.support.ResourceEditorRegistrar`
### 相关文档

- [Spring-PropertyEditorRegistry](/docs/beans/propertyEditor/Spring-PropertyEditorRegistry.md)
- [Spring-PropertyEditorRegistrySupport](/docs/beans/propertyEditor/Spring-PropertyEditorRegistrySupport.md)
- [Spring-PropertyEditorRegistrar](/docs/beans/propertyEditor/Spring-PropertyEditorRegistrar.md)
- [Spring-ResourceEditorRegistrar](/docs/beans/propertyEditor/Spring-ResourceEditorRegistrar.md)