<h2>1.5. Starters</h2><br>

Starters是一组便捷的依赖项描述符的集合，您可以在应用程序中包括它们。您可以一站式获取所需的所有Spring和相关技术，而不必复制粘贴大量的示例代码和依赖描述符。例如，如果要开始使用Spring和JPA进行数据库访问，请在项目中包含```spring-boot-starter-data-jpa```依赖项。

Starters包含许多启动项目并快速运行所需的依赖项，并且提供一组受支持的受管理传递性的依赖集合。


&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;<b>名字叫什么</b><br>
所有官方入门者都遵循类似的命名方式。spring-boot-starter-*，其中*是特定类型的应用程序。这种命名结构旨在在您需要寻找入门者时提供帮助。许多IDE中的Maven集成使您可以按名称搜索依赖项。例如，在安装了适当的Eclipse或STS插件的情况下，您可以按ctrl-spacePOM编辑器，然后键入“ spring-boot-starter”以获取完整列表。

如“ 创建自己的入门者 ”部分中所述，第三方入门者不应以开头spring-boot，因为它是为官方Spring Boot构件保留的。而是，第三方启动程序通常以项目名称开头。例如，thirdpartyproject通常将名为的第三方启动程序项目命名为thirdpartyproject-spring-boot-starter。


Spring Boot在该org.springframework.boot组下提供了以下应用程序启动器：

表1. Spring Boot应用程序启动器
名称