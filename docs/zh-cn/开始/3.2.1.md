<h2>3.2.1. 手动安装</h2><br>

您可以从Spring软件仓库下载Spring CLI发行版：

* [spring-boot-cli-2.2.1.RELEASE-bin.zip](https://repo.spring.io/release/org/springframework/boot/spring-boot-cli/2.2.1.RELEASE/spring-boot-cli-2.2.1.RELEASE-bin.zip)

* [spring-boot-cli-2.2.1.RELEASE-bin.tar.gz](https://repo.spring.io/release/org/springframework/boot/spring-boot-cli/2.2.1.RELEASE/spring-boot-cli-2.2.1.RELEASE-bin.tar.gz)

也提供最先进的[snapshot distributions](https://repo.spring.io/snapshot/org/springframework/boot/spring-boot-cli/) 。

下载完成后，请按照解压缩后的归档文件中的[INSTALL.txt](https://raw.githubusercontent.com/spring-projects/spring-boot/v2.2.1.RELEASE/spring-boot-project/spring-boot-cli/src/main/content/INSTALL.txt)
说明进行操作。总而言之，在```.zip```文件的```bin/```目录中有一个```spring```脚本（Windows下是```spring.bat```）。或使用```java -jar```运行```lib/```目录下的```.jar```文件（该脚本会帮你确保classpath被正确设置）。