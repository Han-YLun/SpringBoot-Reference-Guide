<h2>8.2.2 排除资源</h2>

某些资源在更改时不一定需要触发重新启动。例如，Thymeleaf模板可以就地编辑。默认情况下，改变资源```/META-INF/maven```，```/META-INF/resources```，```/resources```，```/static```，```/public```，或```/templates```不触发重新启动，但确会触发[实时加载(live reload)](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-devtools-livereload)。如果要自定义这些排除项，则可以使用该```spring.devtools.restart.exclude```属性。例如，仅排除```/static```，```/public```您将设置以下属性：

```
spring.devtools.restart.exclude=static/**,public/**
```

<b>注：</b>如果要保留这些默认值并添加其他排除项，请改用该spring.devtools.restart.additional-exclude属性。
