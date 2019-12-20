<h2>4.2 添加Classpath依赖</h2>

Spring Boot提供了许多“Starters”，使您可以将jars添加到Classpath中。示例程序中已经在POM的```parent```节点使用了```spring-boot-starter-parent```，它是一个特殊的starter，提供了有用的Maven默认设置。同时，它也提供一个```dependency-management```节点，这样对于期望（”blessed“）的依赖就可以省略```version```标记了。

其他“Starters”提供了在开发特定类型的应用程序时可能需要的依赖项。由于我们正在开发Web应用程序，因此我们添加了```spring-boot-starter-web```依赖项。在此之前，我们可以通过运行以下命令来查看当前的状态：

```java
$ mvn dependency:tree

[INFO] com.example:myproject:jar:0.0.1-SNAPSHOT
```

该mvn dependency:tree命令显示项目依赖关系的树形表示。您可以看到它spring-boot-starter-parent本身不提供任何依赖关系。要添加必要的依赖项，请编辑您的依赖项，pom.xml并spring-boot-starter-web在该parent部分的正下方添加依赖项：

```
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
</dependencies>
```

如果您再次运行```mvn dependency:tree```，您会发现还有许多其他依赖项，包括Tomcat Web服务器和Spring Boot本身。