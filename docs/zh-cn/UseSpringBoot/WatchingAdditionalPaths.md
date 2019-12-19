<h2>8.2.3 查看其他路径</h2>

当您对不在classpath上的文件进行更改时，您可能希望重新启动或重新加载应用程序。为此，请使用该```spring.devtools.restart.additional-paths```属性配置其他路径以监视更改。您可以使用[前面描述](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-devtools-restart-exclude)的```spring.devtools.restart.exclude```属性来控制其他路径下的更改是触发完全重启还是[实时重载](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-devtools-livereload)。
