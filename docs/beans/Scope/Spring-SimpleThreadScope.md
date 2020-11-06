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

# Spring SimpleThreadScope



- 类全路径: `org.springframework.context.support.SimpleThreadScope`







## 内部变量



```java
private final ThreadLocal<Map<String, Object>> threadScope =
      new NamedThreadLocal<Map<String, Object>>("SimpleThreadScope") {
         @Override
         protected Map<String, Object> initialValue() {
            return new HashMap<>();
         }
      };
```



- 内部变量`threadScope` 是ThreadLocal 中存储了 Map 的这么一个对象







## 方法列表

### get

- 逻辑

1. 从ThreadLocal中获取容器
   1. 容器中获取实例
      1. 实例不存在
         1. objectFactory创建
         2. 设置到容器

```java
@Override
public Object get(String name, ObjectFactory<?> objectFactory) {
   // ThreadLocal 中获取容器
   Map<String, Object> scope = this.threadScope.get();
   // 容器中获取
   Object scopedObject = scope.get(name);
   // 不存在
   if (scopedObject == null) {
      // 从 ObjectFactory 中获取
      scopedObject = objectFactory.getObject();
      // 设置到容器
      scope.put(name, scopedObject);
   }
   return scopedObject;
}
```







### remove



```java
@Override
@Nullable
public Object remove(String name) {
   Map<String, Object> scope = this.threadScope.get();
   return scope.remove(name);
}
```





### getConversationId

- 当前线程的name



```java
@Override
public String getConversationId() {
   return Thread.currentThread().getName();
}
```