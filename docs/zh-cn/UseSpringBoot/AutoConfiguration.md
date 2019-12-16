<h2>4.自动配置</h2>

Spring Boot自动配置会尝试根据添加的jar依赖项自动配置Spring应用程序。例如，如果```HSQLDB```位于classpath下，并且尚未手动配置任何数据库连接bean，那么Spring Boot会自动配置内存型(in-memory)数据库。

您需要通过将```@EnableAutoConfiguration```或```@SpringBootApplication```注释添加到一个```@Configuration```类中来进行自动配置。

<b>注：</b>您只能添加一个```@SpringBootApplication```或```@EnableAutoConfiguration```注释。我们通常建议您仅将一个或另一个添加到您的主要```@Configuration```类中。


