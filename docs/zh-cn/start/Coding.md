<h2>4.3 编写代码</h2>

要完成我们的应用程序，我们需要创建一个Java文件。默认情况下，Maven默认会编译```src/main/java```下的源码，因此您需要创建该文件夹结构，然后添加一个名为的文件```src/main/java/Example.java```，其中包含以下代码：

```java
import org.springframework.boot.*;
import org.springframework.boot.autoconfigure.*;
import org.springframework.web.bind.annotation.*;

@RestController
@EnableAutoConfiguration
public class Example {

    @RequestMapping("/")
    String home() {
        return "Hello World!";
    }

    public static void main(String[] args) {
        SpringApplication.run(Example.class, args);
    }

}
```

尽管这里没有太多代码，但是已经发生了很多事情。我们将在接下来的几节中逐步介绍重要部分。