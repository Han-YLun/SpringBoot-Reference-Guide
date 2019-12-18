<h2>8.2 自动重启</h2>

```spring-boot-devtools```只要类路径上的文件发生更改，应用程序就会自动重启。在IDE中工作时，这可能是一个有用的功能，因为它为代码更改提供了非常快速的反馈循环。默认情况下，将监视类路径上指向文件夹的任何条目的更改。请注意，某些资源（例如静态资产和视图模板）不需要重新启动应用程序。


<b>触发重启</b>
当DevTools监视类路径资源时，触发重启的唯一方法是更新类路径。导致类路径更新的方式取决于所使用的IDE。在Eclipse中，保存修改后的文件将导致类路径被更新并触发重新启动。在IntelliJ IDEA中，构建项目（```Build → Build Project```）具有相同的效果。


<b>注：</b>只要启用了forking，您还可以使用受支持的构建插件（Maven和Gradle）启动应用程序，因为DevTools需要隔离的应用程序类加载器才能正常运行。默认情况下，Gradle和Maven插件会forking应用程序进程。


<b>注：</b>与LiveReload一起使用时，自动重新启动效果很好。 [有关详细信息](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-devtools-livereload)，[请参见LiveReload部分](https://docs.spring.io/spring-boot/docs/current/reference/html/using-spring-boot.html#using-boot-devtools-livereload)。如果使用JRebel，则禁用自动重新启动，而支持动态重新加载。其他devtools功能（例如LiveReload和属性替代）仍可以使用。


<b>注：</b>DevTools依靠应用程序上下文的关闭挂钩在重新启动期间将其关闭。如果您禁用了关机挂钩（```SpringApplication.setRegisterShutdownHook(false)```），它将无法正常工作。


<b>注：</b>当决定是否在类路径中的条目应该触发重新启动时，DevTools自动忽略以下工程```spring-boot```，```spring-boot-devtools```，```spring-boot-autoconfigure```，```spring-boot-actuator```，和```spring-boot-starter```。


<b>注：</b>DevTools需要自定义```ApplicationContext```使用的```ResourceLoader```。如果您的应用程序已经提供了一个，它将被包装。不支持直接重写```ApplicationContext```上的```getResource```方法。



<b>Restart vs Reload</b>
Spring Boot提供的重启技术通过使用两个类加载器来工作。不变的类（例如，来自第三方jar的类）将被加载到基类加载器中。您正在开发的类将加载到重启类加载器中。重新启动应用程序时，将丢弃重新启动类加载器，并创建一个新的类加载器。这种方法意味着应用程序的重启通常比“cold starts”要快得多，因为基本类加载器已经可用并已填充。

如果发现重新启动对于您的应用程序来说不够快，或者遇到类加载问题，则可以考虑从ZeroTurnaround 重新加载技术，例如[JRebel](https://jrebel.com/software/jrebel/)。这些方法通过在加载类时重写类来使其更易于重新加载。








	