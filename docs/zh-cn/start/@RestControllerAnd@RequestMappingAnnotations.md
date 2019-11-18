<h2>4.3.1. @RestController和@RequestMapping注释</h2><br>

我们```Example```类的第一个注释是```@RestController```。这被称为构造型注释。它为人们阅读代码提供了提示，对于Spring来说，类扮演了特定角色。在这种情况下，我们的类是一个web ```@Controller```，因此Spring在处理传入的Web请求时会考虑使用它。

```@RequestMapping```注释提供“路由”的信息。它告诉Spring任何具有```/```路径的HTTP请求都应映射到该```home```方法。```@RestController```注解告诉Spring以字符串的形式渲染结果，并直接返回给调用者。

<b>注：</b>在```@RestController```与```@RequestMapping```注解是Spring MVC的注解（他们并不是专门针对Spring Boot的）。有关更多详细信息，请参见Spring参考文档中的[MVC部分](https://docs.spring.io/spring/docs/5.2.1.RELEASE/spring-framework-reference/web.html#mvc)。