<h2>2.1 使用“default”包</h2><br>

当一个类不包含```package```声明时，它被认为是在“default package”中。通常不建议使用“default package”，应避免使用。因为使用了```@ComponentScan```，```@ConfigurationPropertiesScan```，```@EntityScan```，或```@SpringBootApplication```的Spring Boot注解启动应用程序，它会扫描每个jar中的类，这会造成一定的问题。

<b>注：</b>我们建议您遵循Java建议的包命名规范，并使用反向域名（例如```com.example.project```）。
