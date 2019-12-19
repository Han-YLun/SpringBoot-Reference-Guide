<h2>8.2.5 使用触发文件</h2>

如果使用IDE连续不断地编译变化的文件，您则可能更喜欢仅在特定时间触发重新启动。为此，您可以使用“触发文件”，这是一个特殊文件，只有修改它才能实际触发一个重启检测。


对文件的任何更新都将触发检查，但是只有在Devtools检测到有事情要做的情况下，重启才真正发生。


要使用触发文件，请将```spring.devtools.restart.trigger-file```属性设置为触发文件的名称（不包括任何路径）。触发文件必须出现在classpath上的某个位置。

例如，如果您的项目具有以下结构：

```bash
src
+- main
   +- resources
      +- .reloadtrigger
```

那么您的```trigger-file```属性将是：
```bash
spring.devtools.restart.trigger-file=.reloadtrigger
```

现在，仅在```src/main/resources/.reloadtrigger```更新时才会重新启动。

您可能希望将其```spring.devtools.restart.trigger-file```设置为[全局设置](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-devtools-globalsettings)，以便所有项目以相同的方式运行。


某些IDE具有使您不必手动更新触发器文件的功能。 [Eclipse的Spring Tools](https://spring.io/tools)和[IntelliJ IDEA (Ultimate Edition)](https://www.jetbrains.com/idea/)都具有这种支持。使用Spring Tools，您可以从控制台视图中使用“reload”按钮（只要您```trigger-file```名为```.reloadtrigger```）。对于IntelliJ，您可以按照其[文档](https://www.jetbrains.com/help/idea/spring-boot.html#configure-application-update-policies-with-devtools)中的说明进行操作。


