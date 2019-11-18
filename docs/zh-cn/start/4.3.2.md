<h2>4.3.2. @EnableAutoConfiguration注解</h2><br>

第二个类级别的注释是```@EnableAutoConfiguration```。这个注释告诉Spring Boot根据所添加的jar依赖“猜测”您想如何配置Spring。由于```spring-boot-starter-web```添加了Tomcat和Spring MVC，因此```auto-configuration```假定您正在开发Web应用程序并对Spring相应地设置。

<b>Starters and Auto-configuration:</b><br>
Auto-configuratio旨在与“Starters”配合使用，但是这两个概念并没有直接的联系。您可以在starters之外自由选择jars依赖项。Spring Boot仍会尽其所能自动配置您的应用程序。