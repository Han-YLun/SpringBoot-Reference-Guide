<h2>4.3.3 “main”方法</h2>

我们应用程序的最后一部分是```main```方法。这只是遵循Java约定的应用程序入口的标准方法。我们的main方法通过调用```run```，将业务委托给了Spring Boot的```SpringApplication```类。```SpringApplication```将引导我们的应用，启动Spring，相应地启动被自动配置的Tomcat web服务器。我们需要将```Example.class```作为参数传递给```run```方法，以判断```SpringApplication```哪个是主要的Spring组件，并传递```args```数组以暴露所有的命令行参数。