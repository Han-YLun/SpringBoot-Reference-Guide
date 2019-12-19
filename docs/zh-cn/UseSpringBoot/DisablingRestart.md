<h2>8.2.4 禁用重启</h2>

如果您不想使用自动重启功能，则可以使用该```spring.devtools.restart.enabled```属性将其禁用。在大多数情况下，您可以在自己的属性配置文件```application.properties```中设置此属性（这样做仍会初始化重新启动类加载器，但它不会监视文件更改）。


如果您需要完全禁用重启支持（例如，因为它不适用于特定的库），则需要在调用```SpringApplication.run(…​)```之前将```spring.devtools.restart.enabled``` ```System```属性设置为```false```，如以下示例所示： 


```java
public static void main(String[] args) {
    System.setProperty("spring.devtools.restart.enabled", "false");
    SpringApplication.run(MyApp.class, args);
}
```