<h2>7.3 使用Maven插件运行</h2>

Spring Boot Maven插件包含一个```run```目标，可用于快速编译和运行您的应用程序。应用程序以热启动方式运行，就像在IDE中一样。以下示例显示了运行Spring Boot应用程序的典型Maven命令：

```bash
$ mvn spring-boot:run
```

您可能还想使用```MAVEN_OPTS```操作系统环境变量，如以下示例所示：


```bash
$ export MAVEN_OPTS=-Xmx1024m
```
