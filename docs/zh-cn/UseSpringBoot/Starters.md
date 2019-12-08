<h2>1.5. Starters</h2><br>

Starters是一组便捷的依赖项描述符的集合，您可以在应用程序中包括它们。您可以一站式获取所需的所有Spring和相关技术，而不必复制粘贴大量的示例代码和依赖描述符。例如，如果要开始使用Spring和JPA进行数据库访问，请在项目中包含```spring-boot-starter-data-jpa```依赖项。

Starters包含许多启动项目并快速运行所需的依赖项，并且提供一组受支持的受管理传递性的依赖集合。


<b>名字叫什么:</b><br>
&emsp;&emsp;所有官方Starters都遵循类似的命名方式:```spring-boot-starter-*```，其中*是特定类型的应用程序。这种命名结构旨在在您需要寻找Starters时提供帮助。许多IDE中的Maven集成使您可以按名称搜索依赖项。例如，在安装了适当的Eclipse或STS插件的情况下，您可以按```ctrl-space```，然后键入“ spring-boot-starter”以获取完整列表。


如“[Creating Your Own Starter](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-custom-starter)”部分中所述，第三方starters不应以```spring-boot```开头，因为它跟Spring Boot官方artifacts冲突。一个acme的第三方starter通常命名为```acme-spring-boot-starter```。



Spring Boot在该```org.springframework.boot```下提供了以下应用程序启动器：


<b>表1. Spring Boot application starters</b>
		
|Name|Description|Pom|
|-------------------------------------------------|------------------------------------------------------------   |------------------------------------------------------------|
| ```spring-boot-starter```                         | 核心入门工具，包括自动配置支持，日志记录和YAML               | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter/pom.xml) |
| ```spring-boot-starter-activemq```                | 使用 Apache ActiveMQ 的 JMS 消息入门                         | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-activemq/pom.xml) |
| ```spring-boot-starter-amqp```                    | 使用 Spring AMQP 和 Rabbit MQ 的入门                         | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-amqp/pom.xml) |
| ```spring-boot-starter-aop```                     | 使用 Spring AOP 和 AspectJ 进行面向切面编程的入门            | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-aop/pom.xml) |
| ```spring-boot-starter-artemis```                 | 使用 Apache Artemis 的 JMS 消息入门                          | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-artemis/pom.xml) |
| ```spring-boot-starter-batch```                   | 使用 Spring Batch 的入门                                     | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-batch/pom.xml) |
| ```spring-boot-starter-cache```                   | 使用 Spring Framework 的缓存支持                             | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-cache/pom.xml) |
| ```spring-boot-starter-cloud-connectors```        | 使用 Spring Cloud Connectors 的入门程序，可简化与 Cloud Foundry 和 Heroku 等云平台中服务的连接。 不赞成使用 Java CFEnv | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-cloud-connectors/pom.xml) |
| ```spring-boot-starter-data-cassandra```          | 使用 Cassandra 分布式数据库和 Spring Data Cassandra 的入门   | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-cassandra/pom.xml) |
| ```spring-boot-starter-data-cassandra-reactive``` | 使用 Cassandra 分布式数据库和 Spring Data Cassandra Reactive 的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-cassandra-reactive/pom.xml) |
| ```spring-boot-starter-data-couchbase```          | 使用 Couchbase 面向文档的数据库和 Spring Data Couchbase 的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-couchbase/pom.xml) |
| ```spring-boot-starter-data-couchbase-reactive``` | 使用 Couchbase 面向文档的数据库和 Spring Data Couchbase Reactive 的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-couchbase-reactive/pom.xml) |
| ```spring-boot-starter-data-elasticsearch```      | 使用 Elasticsearch 搜索和分析引擎以及 Spring Data Elasticsearch 的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-elasticsearch/pom.xml) |
| ```spring-boot-starter-data-jdbc```               | 使用 Spring Data JDBC 的入门                                 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-jdbc/pom.xml) |
| ```spring-boot-starter-data-jpa```                | 将 Spring Data JPA 与 Hibernate 结合使用的入门               | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-jpa/pom.xml) |
| ```spring-boot-starter-data-ldap```               | 使用Spring Data LDAP的入门                                   | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-ldap/pom.xml) |
| ```spring-boot-starter-data-mongodb```            | 使用 MongoDB 面向文档的数据库和 Spring Data MongoDB 的入门   | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-mongodb/pom.xml) |
| ```spring-boot-starter-data-mongodb-reactive```   | 使用 MongoDB 面向文档的数据库和 Spring Data MongoDB Reactive 的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-mongodb-reactive/pom.xml) |
| ```spring-boot-starter-data-neo4j```              | 使用 Neo4j 图形数据库和 Spring Data Neo4j 的入门             | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-neo4j/pom.xml) |
| ```spring-boot-starter-data-redis```              | 将 Redis 键值数据存储与 Spring Data Redis 和 Lettuce 客户端一起使用的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-redis/pom.xml) |
| ```spring-boot-starter-data-redis-reactive```     | 将 Redis 键值数据存储与 Spring Data Redis Reacting 和 Lettuce 客户端一起使用的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-redis-reactive/pom.xml) |
| ```spring-boot-starter-data-rest```               | 使用 Spring Data REST 在 REST 上公开 Spring Data 存储库的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-rest/pom.xml) |
| ```spring-boot-starter-data-solr```               | 结合使用 Apache Solr 搜索平台和 Spring Data Solr 的入门者    | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-data-solr/pom.xml) |
| ```spring-boot-starter-freemarker```              | 使用 FreeMarker 视图构建 MVC Web 应用程序的入门              | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-freemarker/pom.xml) |
| ```spring-boot-starter-groovy-templates```        | 使用 Groovy 模板视图构建 MVC Web 应用程序的入门              | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-groovy-templates/pom.xml) |
| ```spring-boot-starter-hateoas```                 | 使用 Spring MVC 和 Spring HATEOAS 构建基于超媒体的 RESTful Web 应用程序的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-hateoas/pom.xml) |
| ```spring-boot-starter-integration```             | 使用 Spring Integration 的入门                               | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-integration/pom.xml) |
| ```spring-boot-starter-jdbc```                    | 通过 HikariCP 连接池使用 JDBC 的入门                         | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-jdbc/pom.xml) |
| ```spring-boot-starter-jersey```                  | 使用 JAX-RS 和 Jersey 构建 RESTful Web 应用程序的入门。spring-```boot-starter-web```的替代品 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-jersey/pom.xml) |
| ```spring-boot-starter-jooq```                    | 使用 jooq 访问 SQL 数据库的入门。替代 ```spring-boot-starter-data-jpa``` 或 ```spring-bootstarter-jdbc``` | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-jooq/pom.xml) |
| ```spring-boot-starter-json```                    | 读写 JSON 入门                                               | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-json/pom.xml) |
| ```spring-boot-starter-jta-atomikos```            | 使用 Atomikos 的 JTA 交易入门                                | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-jta-atomikos/pom.xml) |
| ```spring-boot-starter-jta-bitronix```            | 使用 Bitronix 的 JTA 交易入门                                | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-jta-bitronix/pom.xml) |
| ```spring-boot-starter-mail```                    | 使用 Java Mail 和 Spring Framework 的电子邮件发送支持的入门  | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-mail/pom.xml) |
| ```spring-boot-starter-mustache```                | 使用 Mustache 视图构建 Web 应用程序的入门                    | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-mustache/pom.xml) |
| ```spring-boot-starter-oauth2-client```           | 使用 Spring Security 的 OAuth2 / OpenID Connect 客户端功能的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-quartz/pom.xml) |
| ```spring-boot-starter-oauth2-resource-server```  | 使用Spring Security的OAuth2资源服务器功能的入门              | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-oauth2-resource-server/pom.xml) |
| ```spring-boot-starter-quartz```                  | 入门使用 Quartz Scheduler                                    | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-oauth2-resource-server/pom.xml) |
| ```spring-boot-starter-rsocket```                 | 用于构建 RSocket 客户端和服务器的入门程序。                  | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-rsocket/pom.xml) |
| ```spring-boot-starter-security```                | 使用 Spring Security 的入门                                  | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-security/pom.xml) |
| ```spring-boot-starter-test```                    | 用于使用包括 JUnit，Hamcrest 和 Mockito 在内的库测试 Spring Boot 应用程序的入门程序 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-test/pom.xml) |
| ```spring-boot-starter-thymeleaf```               | 使用 Thymeleaf 视图构建 MVC Web 应用程序的入门               | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-thymeleaf/pom.xml) |
| ```spring-boot-starter-validation```              | 通过 Hibernate Validator 使用 Java Bean 验证的入门           | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-validation/pom.xml) |
| ```spring-boot-starter-web```                     | 使用 Spring MVC 构建 Web（包括 RESTful）应用程序的入门程序。使用 Tomcat 作为默认的嵌入式容器 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-web/pom.xml) |
| ```spring-boot-starter-web-services```            | 使用 Spring Web Services 的入门                              | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-web-services/pom.xml) |
| ```spring-boot-starter-webflux```                 | 使用 Spring Framework 的反应式 Web 支持构建 WebFlux 应用程序的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-webflux/pom.xml) |
| ```spring-boot-starter-websocket```               | 使用 Spring Framework 的 WebSocket 支持构建 WebSocket 应用程序的入门 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-websocket/pom.xml) |

除了application starters，以下starters可用于添加[production ready](https://docs.spring.io/spring-boot/docs/current/reference/html/production-ready-features.html#production-ready)功能：

<b>表2. Spring Boot production starters</b>

| Name                                        | Description                                                                                                            | Pom |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | --- |
| ```spring-boot-starter-actuator``` | 使用Spring Boot的Actuator的入门程序，它提供了production ready功能，可帮助您监视和管理应用程序 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-actuator/pom.xml) |

最后，Spring Boot还包括以下启动程序，如果您想排除或交换特定的技术方面，可以使用这些starters：

<b>表3. Spring Boot technical starters</b>

| Name                                    |                         Description                          | Pom                                                          |
| --------------------------------------- | :----------------------------------------------------------: | ------------------------------------------------------------ |
| ```spring-boot-starter-jetty```         | 使用Jetty作为内嵌servlet容器的starter。[```spring-boot-starter-tomcat```](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#spring-boot-starter-tomcat)的替代品 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-jetty/pom.xml) |
| ```spring-boot-starter-log4j2```        | 使用Log4j2进行日志记录。[```spring-boot-starter-logging```](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#spring-boot-starter-logging)的替代品 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-log4j2/pom.xml) |
| ```spring-boot-starter-logging```       |       使用Logback进行日志记录。默认记录日志的starter。       | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-logging/pom.xml) |
| ```spring-boot-starter-reactor-netty``` |        使用Reactor Netty作为内嵌HTTP服务器的starter。        | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-reactor-netty/pom.xml) |
| ```spring-boot-starter-tomcat```        | 用于将Tomcat用作内嵌Servlet容器。默认使用的servlet容器starter是[```spring-boot-starter-web```](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#spring-boot-starter-web) | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-tomcat/pom.xml) |
| ```spring-boot-starter-undertow```      | 使用Undertow作为内嵌servlet容器的starter。[```spring-boot-starter-tomcat```](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#spring-boot-starter-tomcat)的替代品 | [Pom](https://github.com/spring-projects/spring-boot/tree/v2.2.2.RELEASE/spring-boot-project/spring-boot-starters/spring-boot-starter-undertow/pom.xml) |

<b>注：</b>有关社区贡献的其他starters的列表，请参见GitHub 中```spring-boot-starters```模块中的[README文件](https://github.com/spring-projects/spring-boot/tree/master/spring-boot-project/spring-boot-starters/README.adoc)。