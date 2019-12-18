<h2>8.开发人员工具</h2>

Spring Boot包含一组额外的工具，这些工具可以使应用程序开发体验更加愉快。该```spring-boot-devtools```模块可以包含在任何项目中，以提供其他开发功能。要包括devtools支持，请将模块依赖项添加到您的构建中，如以下Maven和Gradle清单所示：


<b>Maven</b>

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-devtools</artifactId>
        <optional>true</optional>
    </dependency>
</dependencies>
```

<b>Gradle</b>

```xml
configurations {
    developmentOnly
    runtimeClasspath {
        extendsFrom developmentOnly
    }
}
dependencies {
    developmentOnly("org.springframework.boot:spring-boot-devtools")
}
```


<b>注：</b>运行打包的应用程序时，将自动禁用开发人员工具。如果您的应用程序是从```java -jar```特殊的类加载器启动的，或者从特殊的类加载器启动的，则将其视为“生产应用程序”。如果那对您不适用（即如果您从容器中运行应用程序），请考虑排除devtools或设置```-Dspring.devtools.restart.enabled=false```系统属性。

<b>注：</b>在Maven中将依赖项标记为可选，或```developmentOnly```在Gradle中使用自定义配置（如上所示）是一种最佳做法，可防止将devtools过渡地应用到使用项目的其他模块。


<b>注：</b>重新打包的存档默认情况下不包含devtools。如果要使用某个远程devtools功能，则需要禁用```excludeDevtoolsbuild```属性以包含它。Maven和Gradle插件均支持该属性。


