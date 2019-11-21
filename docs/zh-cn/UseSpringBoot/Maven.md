<h2>1.2. Maven</h2><br>

Maven用户可以从```spring-boot-starter-parent```项目继承以获得合适的默认值。父项目提供以下功能：

* Java 1.8是默认的编译级别。

* 源编码为UTF-8。

* 一个[依赖管理部分](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-dependency-management)，从spring启动依赖性POM，管理公共依赖的版本继承。当在自己的pom中使用这些依赖关系时，可以为这些依赖关系省略<version>标记。

* 具有重新打包执行ID的[目标](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/maven-plugin//repackage-mojo.html)执行。

* 具有恰到好处的[资源过滤](https://maven.apache.org/plugins/maven-resources-plugin/examples/filter.html)。

* 恰到好处的插件配置（[exec插件](https://www.mojohaus.org/exec-maven-plugin/)，[Git commit ID](https://github.com/ktoso/maven-git-commit-id-plugin),[shade](https://maven.apache.org/plugins/maven-shade-plugin/)）。

* 恰到好处的针对```application.properties```和```application.yml```包括特定于配置文件的文件的资源过滤（例如```application-dev.properties```和```application-dev.yml```）

<b>注：</b>请注意，由于```application.properties```和```application.yml```文件都接受Spring样式的占位符（```${…​}```），因此Maven filtering已更改为使用```@..@```占位符。（您可以通过设置名为```resource.delimiter```的Maven属性来覆盖它。）