<h2>1.2.1 继承 Starter Parent</h2>

要将您的项目配置为继承自```spring-boot-starter-parent```，请设置```parent```如下：

```XML
<!-- Inherit defaults from Spring Boot -->
<parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>2.2.1.RELEASE</version>
</parent>
```

<b>注：</b>您只需要为此依赖项指定Spring Boot版本号。如果导入其他starters，则可以安全地省略版本号。

使用该设置，您还可以通过覆盖自己项目中的属性来覆盖各个依赖项。例如，要升级到另一个Spring Data的发布版本，您可以将以下内容添加到您的```pom.xml```：

```XML
<properties>
    <spring-data-releasetrain.version>Fowler-SR2</spring-data-releasetrain.version>
</properties>
```

<b>注：</b>查看```[spring-boot-dependencies pom](https://github.com/spring-projects/spring-boot/tree/v2.2.1.RELEASE/spring-boot-project/spring-boot-dependencies/pom.xml)```以获取受支持属性的列表。