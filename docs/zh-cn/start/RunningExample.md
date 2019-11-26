<h2>4.4. 运行示例</h2><br>

此时，您的应用程序应该可以工作了。由于使用了```spring-boot-starter-parent```下的POM，因此有一个有用的```run```目标，可以用来启动应用程序。从项目根目录中输入```mvn spring-boot:run```以启动应用程序。您应该看到类似于以下内容的输出：

```XML
$ mvn spring-boot:run

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::  (v2.2.1.RELEASE)
....... . . .
....... . . . (log output here)
....... . . .
........ Started Example in 2.222 seconds (JVM running for 6.514)
```

如果使用浏览器打开localhost:8080，则应该看到以下输出：

```JAVA
Hello World!
```

要正常退出该应用程序，请按```ctrl-c```。