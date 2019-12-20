<h2>3.3 从较早版本的Spring Boot升级</h2>

如果要从```1.x```Spring Boot发行版进行升级，请查看项目[Wiki上的“迁移指南”](https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-2.0-Migration-Guide)，其中提供了详细的升级说明。还请检查[“发行说明”](https://github.com/spring-projects/spring-boot/wiki)以获取每个发行版的“新功能和值得注意的功能”列表。


升级到新功能版本时，某些属性可能已被重命名或删除。Spring Boot提供了一种在启动时分析应用程序环境并打印诊断的方法，而且还可以在运行时为您临时迁移属性。要启用该功能，请将以下依赖项添加到您的项目中：

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-properties-migrator</artifactId>
    <scope>runtime</scope>
</dependency>
```
<br>

<b>注：</b>较晚添加到环境的属性（例如使用时```@PropertySource```）将不被考虑。迁移完成后，请确保从项目的依赖项中删除此模块。


要升级现有的CLI安装，请使用适当的程序包管理器命令（例如，```brew upgrade```）。如果您手动安装了CLI，请遵循[标准说明](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html#getting-started-manual-cli-installation)，记住要更新您的PATH环境变量以删除所有较旧的引用。