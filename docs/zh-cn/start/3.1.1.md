<h2>3.1.1. Maven安装</h2><br>

Spring Boot与Apache Maven 3.3或更高版本兼容。如果尚未安装Maven，则可以按照[maven.apache.org](https://maven.apache.org/)上的说明进行操作。

在许多操作系统上，Maven可以与程序包管理器一起安装。如果您使用OSX Homebrew，请尝试```brew install maven```。Ubuntu用户可以运行```sudo apt-get install maven```。具有[Chocolatey](https://chocolatey.org/)的 Windows用户可以从```choco install maven```提示符下运行。

Spring Boot依赖使用的groupId为org.springframework.boot。通常，您的Maven POM文件会从spring-boot-starter-parent项目继承，并声明对一个或多个[“Starters”](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-starter)的依赖。Spring Boot还提供了一个可选的[Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-maven-plugin)来创建可执行jars。

以下是一个典型的```pom.xml```文件：

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>myproject</artifactId>
    <version>0.0.1-SNAPSHOT</version>

    <!-- Inherit defaults from Spring Boot -->
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.2.1.RELEASE</version>
    </parent>

    <!-- Override inherited settings -->
    <description/>
    <developers>
        <developer/>
    </developers>
    <licenses>
        <license/>
    </licenses>
    <scm>
        <url/>
    </scm>
    <url/>

    <!-- Add typical dependencies for a web application -->
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>

    <!-- Package as an executable jar -->
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>

</project>
```

```spring-boot-starter-parent``` 是使用Spring Boot的一种很好的方法，但是可能并不总是适合。有时您可能需要从其他父POM继承，或者您可能不喜欢我们的默认设置。在这种情况下，请参阅[using-spring-boot.html](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-maven-without-a-parent)以获取使用import范围的替代解决方案。