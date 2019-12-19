<h2>1.2.3 使用Spring Boot Maven插件</h2><br>

Spring Boot包含一个[Maven插件](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-maven-plugin)，可以将项目打包为可执行jar。如果要使用插件，请将该插件添加到您的```<plugins>```部分，如以下示例所示：

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```

<b>注：</b>如果您使用Spring Boot启动器的父pom，则只需添加插件。除非您要更改父级中定义的设置，否则无需对其进行配置。