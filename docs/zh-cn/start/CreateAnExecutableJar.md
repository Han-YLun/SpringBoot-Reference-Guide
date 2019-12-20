<h2>4.5 创建一个可执行的jar</h2>

让我们通过创建可以在生产环境中运行的完全独立的可执行jar文件来结束示例。可执行jar（有时称为“fat jars”）是包含您的已编译类以及代码需要运行的所有jar依赖项的存档。

<b>可执行jars和Java:</b><br>
Java没有提供加载内嵌jar文件（jar中本身包含的jar文件）的标准方法。如果您要分发独立的应用程序，则可能会出现问题。

为了解决这个问题，许多开发人员使用“uber” jars。uber jar将来自应用程序所有jars的所有类打包到单个存档中。这种方法的问题在于，很难查看应用程序中包含哪些库。如果在多个jars中使用相同的文件名（但具有不同的内容），也可能会产生问题。

Spring Boot采用了[另一种方法](https://docs.spring.io/spring-boot/docs/current/reference/html/appendix-executable-jar-format.html#executable-jar)，实际上允许您直接嵌套jar。

要创建可执行jar，我们需要将添加```spring-boot-maven-plugin```添到```pom.xml```。为此，请在该```dependencies```节点后面插入以下行：

```XML
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```

<b>注：</b>```spring-boot-starter-parent```POM包括<executions>配置以结合repackage目标。如果不使用父POM，则需要自己声明此配置。有关详细信息，请参见[插件文档](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/maven-plugin//usage.html)。

保存```pom.xml```,并从命令行运行```mvn package```，如下所示：

```java
$ mvn package

[INFO] Scanning for projects...
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building myproject 0.0.1-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] .... ..
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ myproject ---
[INFO] Building jar: /Users/developer/example/spring-boot-example/target/myproject-0.0.1-SNAPSHOT.jar
[INFO]
[INFO] --- spring-boot-maven-plugin:2.2.1.RELEASE:repackage (default) @ myproject ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
```

如果查看target目录，则应该看到```myproject-0.0.1-SNAPSHOT.jar```。该文件的大小应为10 MB左右。如果您想查看内部结构，可以使用```jar tvf```，如下所示：

```
$ jar tvf target / myproject-0.0.1-SNAPSHOT.jar
```

您还应该在```target```目录中看到一个更小的文件```myproject-0.0.1-SNAPSHOT.jar.original```。这是Maven在Spring Boot重新打包之前创建的原始jar文件。

要运行该应用程序，请使用以下```java -jar```命令：

```java
$ java -jar target/myproject-0.0.1-SNAPSHOT.jar

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
........ Started Example in 2.536 seconds (JVM running for 2.864)
```

和以前一样，要退出该应用程序，请按```ctrl-c```。