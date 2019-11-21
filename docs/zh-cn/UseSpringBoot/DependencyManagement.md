<h2>1.1. 依赖管理</h2><br>

每个Spring Boot版本都提供了它所支持的依赖关系的列表。实际上，您不需要为构建配置中的所有这些依赖项提供版本，因为Spring Boot会为您管理该版本。当您升级Spring Boot本身时，这些依赖项也会以一致的方式升级。

<b>注：</b>您仍然可以指定版本，并在需要时覆盖Spring Boot的默认版本。

依赖列表可与Spring Boot一起使用的所有spring模块以及完善的第三方库列表。该列表作为可与[Maven](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-maven-parent-pom)和[Gradle](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-gradle)一起使用的[依赖列表```(spring-boot-dependencies)```](http://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/htmlsingle/#using-boot-maven-without-a-parent)。

<b>注：</b>Spring Boot的每个发行版都与Spring Framework的基本版本相关联。我们强烈建议您不要指定其版本。
