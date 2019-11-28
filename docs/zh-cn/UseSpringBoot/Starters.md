<h2>1.5. Starters</h2><br>

Starters是一组便捷的依赖项描述符的集合，您可以在应用程序中包括它们。您可以一站式获取所需的所有Spring和相关技术，而不必复制粘贴大量的示例代码和依赖描述符。例如，如果要开始使用Spring和JPA进行数据库访问，请在项目中包含```spring-boot-starter-data-jpa```依赖项。

Starters包含许多启动项目并快速运行所需的依赖项，并且提供一组受支持的受管理传递性的依赖集合。


<b>名字叫什么:</b><br>
&emsp;&emsp;所有官方Starters都遵循类似的命名方式:```spring-boot-starter-*```，其中*是特定类型的应用程序。这种命名结构旨在在您需要寻找Starters时提供帮助。许多IDE中的Maven集成使您可以按名称搜索依赖项。例如，在安装了适当的Eclipse或STS插件的情况下，您可以按```ctrl-space```，然后键入“ spring-boot-starter”以获取完整列表。


如“[Creating Your Own Starter](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-custom-starter)”部分中所述，第三方starters不应以```spring-boot```开头，因为它跟Spring Boot官方artifacts冲突。一个acme的第三方starter通常命名为```acme-spring-boot-starter```。


Spring Boot在该org.springframework.boot组下提供了以下应用程序启动器：

表1. Spring Boot应用程序启动器
名称