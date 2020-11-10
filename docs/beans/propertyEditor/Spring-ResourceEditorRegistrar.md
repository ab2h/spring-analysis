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
# Spring ResourceEditorRegistrar

- 类全路径: `org.springframework.beans.support.ResourceEditorRegistrar`





- 该类实现`PropertyEditorRegistrar`  关注方法

  ```java
  	@Override
  	public void registerCustomEditors(PropertyEditorRegistry registry) {
  		ResourceEditor baseEditor = new ResourceEditor(this.resourceLoader, this.propertyResolver);
  		doRegisterEditor(registry, Resource.class, baseEditor);
  		doRegisterEditor(registry, ContextResource.class, baseEditor);
  		doRegisterEditor(registry, InputStream.class, new InputStreamEditor(baseEditor));
  		doRegisterEditor(registry, InputSource.class, new InputSourceEditor(baseEditor));
  		doRegisterEditor(registry, File.class, new FileEditor(baseEditor));
  		doRegisterEditor(registry, Path.class, new PathEditor(baseEditor));
  		doRegisterEditor(registry, Reader.class, new ReaderEditor(baseEditor));
  		doRegisterEditor(registry, URL.class, new URLEditor(baseEditor));
  
  		ClassLoader classLoader = this.resourceLoader.getClassLoader();
  		doRegisterEditor(registry, URI.class, new URIEditor(classLoader));
  		doRegisterEditor(registry, Class.class, new ClassEditor(classLoader));
  		doRegisterEditor(registry, Class[].class, new ClassArrayEditor(classLoader));
  
  		if (this.resourceLoader instanceof ResourcePatternResolver) {
  			doRegisterEditor(registry, Resource[].class,
  					new ResourceArrayPropertyEditor((ResourcePatternResolver) this.resourceLoader, this.propertyResolver));
  		}
  	}
  ```



- doRegisterEditor 方法

```java
private void doRegisterEditor(PropertyEditorRegistry registry, Class<?> requiredType, PropertyEditor editor) {
   if (registry instanceof PropertyEditorRegistrySupport) {
      // 属性编辑器覆盖默认的编辑器
      ((PropertyEditorRegistrySupport) registry).overrideDefaultEditor(requiredType, editor);
   }
   else {
      // 注册自定义的属性编辑器
      registry.registerCustomEditor(requiredType, editor);
   }
}
```



- 这里主要涉及到`org.springframework.beans.PropertyEditorRegistrySupport`的两个方法 在 [Spring-PropertyEditorRegistrySupport
](/docs/beans/propertyEditor/Spring-PropertyEditorRegistrySupport.md)













