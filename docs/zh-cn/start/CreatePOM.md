<h2>4.1. 创建POM</h2>

我们需要先创建一个Maven pom.xml文件。pom.xml是用来构建项目的。打开您喜欢的文本编辑器并添加以下内容：


```XML
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>myproject</artifactId>
    <version>0.0.1-SNAPSHOT</version>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.2.1.RELEASE</version>
    </parent>

    <description/>
    <developers>
        <developer/>
    </developers>
    <licenses>
        <license/>
    </licenses>
    <scm>
        <url/>
    </scm>
    <url/>

    <!-- Additional lines to be added here... -->

</project>
```
<br>






上面的清单应为您提供有效的构建。您可以通过运行```mvn package```进行测试（目前，您可以忽略```jar will be empty - no content was marked for inclusion!```警告）。

<b>注：</b>此时，您可以将项目导入IDE（大多数现代Java IDE包括对Maven的内置支持）。为简单起见，我们在此示例中继续使用纯文本编辑器。