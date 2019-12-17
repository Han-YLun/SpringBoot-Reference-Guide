<h2>7.3 使用Gradle插件运行</h2>

Spring Boot Gradle插件还包含一个```bootRun```任务，可用于以热启动方式运行您的应用程序。```bootRun```每当您应用```org.springframework.boot```和```java```插件时，都会添加该任务：

```bash
$ gradle bootRun
```

您可能还想使用```JAVA_OPTS```操作系统环境变量，如以下示例所示：

```bash
$ export JAVA_OPTS=-Xmx1024m
```
