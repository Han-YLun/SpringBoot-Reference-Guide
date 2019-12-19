<h2>8.2.6 自定义重启类加载器</h2>

如前面的“[重新启动与重新加载](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-spring-boot-restart-vs-reload)”部分所述，重新启动功能是通过使用两个类加载器实现的。对于大多数应用程序，此方法效果很好。但是，有时可能会导致类加载问题。

默认情况下，IDE中任何打开的项目都使用“重新启动”类加载器加载，而任何常规```.jar```文件都使用“base”类加载器加载。如果您在多模块项目上工作，并且并非每个模块都导入到IDE中，则可能需要自定义内容。为此，您可以创建一个```META-INF/spring-devtools.properties```文件。

该```spring-devtools.properties```文件可以包含以```restart.exclude```和```restart.include```为前缀的属性。```include```元素定义了那些需要加载进'restart'类加载器中的实体，```exclude```元素定义了那些需要加载进'base'类加载器中的实体。这些属性的值是应用于类路径的正则表达式模式，如以下示例所示：

```bash
restart.exclude.companycommonlibs=/mycorp-common-[\\w\\d-\.]+\.jar
restart.include.projectcommon=/mycorp-myproj-[\\w\\d-\.]+\.jar
```

<b>注：</b>所有属性键都必须是唯一的。只要属性以```restart.include.```或```restart.exclude.```开始就可以考虑。

<b>注：</b>	所有```META-INF/spring-devtools.properties```从classpath加载，您可以将文件打包到项目内部，也可以打包到项目使用的库中。
