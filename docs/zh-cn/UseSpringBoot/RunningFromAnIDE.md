<h2>7.1 从IDE运行</h2>

您可以将IDE中的Spring Boot应用程序作为简单的Java应用程序运行。但是，您首先需要导入您的项目。导入步骤因您的IDE和构建系统而异。大多数IDE可以直接导入Maven项目。例如，Eclipse用户可以从```File```菜单中选择```Import…​``` → ```Existing Maven ProjectsFile```导入。

如果您不能直接将项目导入IDE，则可以使用构建插件生成IDE元数据。Maven有包括[Eclipse](https://maven.apache.org/plugins/maven-eclipse-plugin/)和[IDEA](https://maven.apache.org/plugins/maven-idea-plugin/)的插件。Gradle提供了用于[各种IDE](https://docs.gradle.org/current/userguide/userguide.html)的插件。

<b>注：</b>如果不小心运行两次Web应用程序，则会看到“端口已在使用中”的错误。STS用户可以使用```Relaunch```按钮而不是```Run```按钮来确保关闭任何现有实例。


