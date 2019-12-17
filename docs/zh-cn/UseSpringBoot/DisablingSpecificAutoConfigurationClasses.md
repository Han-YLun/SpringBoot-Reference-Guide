<h2>4.2 禁用特定的自动配置类</h2>

如果发现正在应用不需要的自动配置类，则可以使用```@EnableAutoConfiguration```的exclude属性来禁用它们，如以下示例所示：

```java
import org.springframework.boot.autoconfigure.*;
import org.springframework.boot.autoconfigure.jdbc.*;
import org.springframework.context.annotation.*;

@Configuration(proxyBeanMethods = false)
@EnableAutoConfiguration(exclude={DataSourceAutoConfiguration.class})
public class MyConfiguration {
}
```


如果该类不在classpath中，则可以使用```excludeName```注释的属性，并指定全限定名来达到相同效果。最后，您还可以使用```spring.autoconfigure.exclude```属性来控制要排除的自动配置类的列表。

<b>注：</b>您可以在注释级别和使用属性来定义排除项。


<b>注：</b>尽管自动配置类是```public```，但该类唯一被视为公共API的方面是可用于禁用自动配置的类的名称。这些类的实际内容（如嵌套配置类或bean方法）仅供内部使用，我们不建议直接使用它们。


