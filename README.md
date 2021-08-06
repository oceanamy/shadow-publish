# shadow-publish

#### 介绍
仅自用，shadow 远程依赖包。


## 项目地址
https://github.com/Tencent/Shadow

或

https://gitee.com/Tencent/Shadow



## 方法

ext.shadow_version = '2.1.0-02276915-SNAPSHOT'

```
android{
    ...
    allprojects {
        repositories {
            maven { url "https://gitee.com/amyocean/shadow-publish/raw/master" }
        }
    }
}
```
### 宿主

```
    implementation "com.tencent.shadow.dynamic:host:$shadow_version"
```
### Manager
```
    implementation "com.tencent.shadow.dynamic:manager:$shadow_version"
    compileOnly "com.tencent.shadow.core:common:$shadow_version"
    compileOnly "com.tencent.shadow.dynamic:host:$shadow_version"
```
### 插件
```
    classpath "com.tencent.shadow.core:gradle-plugin:$shadow_version"
```
