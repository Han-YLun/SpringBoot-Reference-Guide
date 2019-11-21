<h2>1.2.2. 在没有父POM的情况下使用Spring Boot</h2><br>

并非每个人都喜欢从```spring-boot-starter-parent POM``` 继承。您可能需要使用自己公司的标准parent，或者可能希望显式声明所有Maven配置。

如果您不想使用```spring-boot-starter-parent```，则仍然可以通过使用```scope=import```依赖项来保留依赖项管理（而不是插件管理）的好处，如下所示：

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <!-- Import dependency management from Spring Boot -->
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-dependencies</artifactId>
            <version>2.2.1.RELEASE</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

如上所述，前面的示例设置不允许您使用属性来覆盖各个依赖项。为了达到同样的效果，你需要在项目的```dependencyManagement```节点中，在```spring-boot-dependencies```实体<b>前</b>插入一个节点。例如，要升级到另一个Spring Data发布系列，可以将以下元素添加到pom.xml：

```xml
<dependencyManagement>
    <dependencies>
        <!-- Override Spring Data release train provided by Spring Boot -->
        <dependency>
            <groupId>org.springframework.data</groupId>
            <artifactId>spring-data-releasetrain</artifactId>
            <version>Fowler-SR2</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-dependencies</artifactId>
            <version>2.2.1.RELEASE</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

<b>注：</b>在前面的示例中，我们指定了BOM，但是可以以相同的方式覆盖任何依赖项类型。