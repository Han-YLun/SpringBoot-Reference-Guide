<h2>6.使用@SpringBootApplication注释</h2>

许多Spring Boot开发人员喜欢他们的应用程序使用自动配置，组件扫描，并能够在其“application class”上定义额外的配置。单个```@SpringBootApplication```注释可用于启用这三个功能，即：

* ```@EnableAutoConfiguration```：启用[Spring Boot的自动配置机制](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-auto-configuration)
* ```@ComponentScan```：启用```@Component```对应用程序所在的软件包的扫描（请参阅[最佳实践](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-structuring-your-code)）
* ```@Configuration```：允许在上下文中注册额外的bean或导入其他配置类



```java
package com.example.myapplication;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication // same as @Configuration @EnableAutoConfiguration @ComponentScan
public class Application {

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }

}
```


<b>注：</b>```@SpringBootApplication```还提供了用于自定义```@EnableAutoConfiguration```和```@ComponentScan```属性的别名(aliases)。

<b>注：</b>这些功能都不是强制性的，您可以选择用它启用的任何功能替换此单个注释。例如，您可能不想在应用程序中使用组件扫描或配置属性扫描:
```java
package com.example.myapplication;

import org.springframework.boot.SpringApplication;
import org.springframework.context.annotation.ComponentScan
import org.springframework.context.annotation.Configuration;
import org.springframework.context.annotation.Import;

@Configuration(proxyBeanMethods = false)
@EnableAutoConfiguration
@Import({ MyConfig.class, MyAnotherConfig.class })
public class Application {

    public static void main(String[] args) {
            SpringApplication.run(Application.class, args);
    }

}
```

在此示例中，```Application```与其他任何Spring Boot应用程序一样，除了不会自动检测```@Component```-annotated类和```@ConfigurationProperties```-annotated类，并且显式导入用户定义的Bean（请参阅参考资料```@Import```）。
