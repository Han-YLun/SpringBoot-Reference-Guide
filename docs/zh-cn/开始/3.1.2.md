<h2>3.1.2. Gradle安装</h2><br>

Spring Boot与5.x兼容。4.10也支持但这种支持已取消，将在未来的版本中删除。如果尚未安装Gradle，则可以按照[gradle.org](https://gradle.org/)上的说明进行操作。

Spring Boot的依赖可通过groupId ```org.springframework.boot```来声明。通常，您的项目声明对一个或多个[“Starters”](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-starter)的依赖。Spring Boot提供了一个很有用的[Gradle plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins.html#build-tool-plugins-gradle-plugin)，可用于简化依赖项声明和创建可执行jars。




<br>

<b>注:</b><br>
&emsp;&emsp;当您需要构建项目时，Gradle Wrapper提供了一种获取Gradle的好方法。这是一个小的脚本和库，您随代码一起提交以引导构建过程。<br>
&emsp;&emsp;有关详细信息，请参见[docs.gradle.org/current/userguide/gradle_wrapper.html](docs.gradle.org/current/userguide/gradle_wrapper.html)。有关Spring Boot和Gradle入门的更多详细信息，可以在Gradle插件参考指南的[“Getting Started section”](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/gradle-plugin/reference/html//#getting-started)部分中找到。
