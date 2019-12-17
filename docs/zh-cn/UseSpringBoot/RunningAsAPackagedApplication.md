<h2>7.2 作为打包的应用程序运行</h2>

如果您使用Spring Boot Maven或Gradle插件来创建可执行jar，则可以使用如下命令来运行您的应用程序，如以下示例所示：

```bash
$ java -jar target/myapplication-0.0.1-SNAPSHOT.jar
```


也可以在启用了远程调试支持的情况下运行打包的应用程序。这样做使您可以将调试器附加到打包的应用程序，如以下示例所示：

```bash
$ java -Xdebug -Xrunjdwp:server=y,transport=dt_socket,address=8000,suspend=n \
       -jar target/myapplication-0.0.1-SNAPSHOT.jar
```
