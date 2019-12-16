<h2>2.2 找到应用程序的主程序入口——Main</h2><br>

我们通常建议您将主应用程序入口类放在其他类之上的顶层。[```@SpringBootApplication```注解](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-using-springbootapplication-annotation)往往放在你的主类，它隐含地定义为某些项目基础的包搜索路径。例如，如果您正在编写JPA应用程序，带注释的类```@SpringBootApplication```则搜索带```@Entity```的类所在的包。使用在根package还允许组件扫描仅应用于您的项目。

<b>注：</b>如果您不想使用```@SpringBootApplication```，可以使用```@EnableAutoConfiguration```和```@ComponentScan```来替代它。

以下清单显示了典型的结构：

```bash
com
 +- example
     +- myapplication
         +- Application.java
         |
         +- customer
         |   +- Customer.java
         |   +- CustomerController.java
         |   +- CustomerService.java
         |   +- CustomerRepository.java
         |
         +- order
             +- Order.java
             +- OrderController.java
             +- OrderService.java
             +- OrderRepository.java
```

该```Application.java```文件将声明```main```方法以及基本的```@SpringBootApplication```使用方法，如下所示：

```java
package com.example.myapplication;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Application {

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }

}
```



