<h2>8.1 属性默认值</h2>

Spring Boot支持的一些库使用缓存来提高性能。例如，	[模板引擎](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-spring-mvc-template-engines)缓存已编译的模板，以避免重复解析模板文件。另外，Spring MVC可以在提供静态资源时向响应添加HTTP缓存头。

尽管缓存在生产中非常有益，但在开发过程中可能适得其反，从而使您无法看到刚刚在应用程序中所做的更改。因此，默认情况下，spring-boot-devtools禁用缓存选项。

缓存选项通常由```application.properties```文件中的设置配置。例如，Thymeleaf提供了该```spring.thymeleaf.cache```属性。该```spring-boot-devtools```模块无需手动设置这些属性，而是自动应用合理的开发时配置。

由于在开发Spring MVC和Spring WebFlux应用程序时需要有关Web请求的更多信息，因此开发人员工具将启用```DEBUG```日志```web```记录。这将为您提供有关传入请求，正在处理的处理程序，响应结果等的信息。如果您希望记录所有请求的详细信息（包括潜在的敏感信息），则可以打开```spring.http.log-request-details```配置属性。

<b>注：</b>如果你不想被应用属性默认可以设置```spring.devtools.add-properties```为```false```在你的```application.properties```。

<b>注：</b>有关devtools应用的属性的完整列表，请参见[DevToolsPropertyDefaultsPostProcessor](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-devtools/src/main/java/org/springframework/boot/devtools/env/DevToolsPropertyDefaultsPostProcessor.java)。