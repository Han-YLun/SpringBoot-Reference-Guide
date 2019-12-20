<h2>4.开发您的第一个Spring Boot应用程序</h2>

本节描述如何开发一个简单的“ Hello World！” Web应用程序，该应用程序重点介绍了Spring Boot的一些关键功能。我们使用Maven来构建该项目，因为大多数IDE都支持它。

<b>注：</b>该[spring.io](https://spring.io/)网站包含了许多“入门” [指南](https://spring.io/guides)。

通过转到[start.spring.io](https://start.spring.io/)并从依赖项搜索器中选择“ Web”启动器，可以简化以下步骤。这样做会生成一个新的项目结构，以便您可以[立即开始编码](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html#getting-started-first-application-code)。可以查看[Spring Initializr](https://docs.spring.io/initializr/docs/current/reference/html//#user-guide)文档以获取更多详细信息。

在开始之前，请打开终端并运行以下命令，以确保安装了有效的Java和Maven版本：

```java
$ java -version
java version "1.8.0_102"
Java(TM) SE Runtime Environment (build 1.8.0_102-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.102-b14, mixed mode)
```

```java
$ mvn -v
Apache Maven 3.5.4 (1edded0938998edf8bf061f1ceb3cfdeccf443fe; 2018-06-17T14:33:14-04:00)
Maven home: /usr/local/Cellar/maven/3.3.9/libexec
Java version: 1.8.0_102, vendor: Oracle Corporation
```

<b>注：</b>该示例需要在其自己的文件夹中创建。随后的说明假定您已经创建了一个合适的文件夹，并且它是当前目录。