<h2>3.2.2 使用SDKMAN安装！</h2>

SDKMAN（软件开发工具包管理器）可用于管理各种二进制SDK的多个版本，包括Groovy和Spring Boot CLI。可以从[sdkman.io](https://sdkman.io/)获取SDKMAN,并使用以下命令安装Spring Boot：

```java
$ sdk install springboot 
$ spring --version 
Spring Boot v2.2.1.RELEASE
```

如果您正在为CLI开发功能并希望轻松访问所构建的版本，请使用以下命令：

```bash
$ sdk install springboot dev /path/to/spring-boot/spring-boot-cli/target/spring-boot-cli-2.2.1.RELEASE-bin/spring-2.2.1.RELEASE/
$ sdk default springboot dev
$ spring --version
Spring CLI v2.2.1.RELEASE
```

这将会安装一个名叫```dev```的本地```spring```实例。它指向您的目标构建位置，因此每次重建Spring Boot ```spring```都是最新的。

您可以通过运行以下命令来查看它：

```bash
$ sdk ls springboot

================================================================================
Available Springboot Versions
================================================================================
> + dev
* 2.2.1.RELEASE

================================================================================
+ - local version
* - installed
> - currently in use
================================================================================
```