---
layout: post
title: macOS arm64 配置 maven
date: 2023-10-16
categories: 学习偶得
---

# macOS arm64 配置 maven

# 一、jdk8安装

注意 jdk1.8 和 jdk8 是同一安装包在不同命名体系下的名字。下载链接：https://www.oracle.com/java/technologies/downloads/#java8-mac，需要oracle账号。

![image-20231016101738474](https://s2.loli.net/2023/10/16/7Ww3heYb4cqg9po.png)

进行默认安装即可。默认安装路径：`/Library/Java/JavaVirtualMachines/jdk-1.8.jdk/Contents/Home`。

接下来配置环境变量。编辑`~/.zshrc`（用vscode或vim），附加以下代码

```bash
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-1.8.jdk/Contents/Home
export PATH=$JAVA_HOME/bin:$PATH%
```

在terminal中输入以下指令

```bash
source ~/.zshrc
echo $JAVA_HOME
```

如果输出`/Library/Java/JavaVirtualMachines/jdk-1.8.jdk/Contents/Home`说明环境变量配置正确。

在terminal中输入`java -version`如果输出以下信息说明安装正确。

![image-20231016104300610](https://s2.loli.net/2023/10/16/JGL6sj3EYvRd4kV.png)

# 二、maven安装

Maven是一个用于构建和管理Java项目的工具。它提供了一种标准化的项目结构和构建过程，使得开发者能够更加方便地管理项目的依赖关系、编译、测试、打包和部署等任务。

Maven使用一个称为"Project Object Model"（POM）的XML文件来描述项目的配置信息和依赖关系。在POM文件中，你可以指定项目的元数据、依赖库、插件、构建目标等信息。Maven会根据POM文件来自动下载所需的依赖库，并根据配置执行相应的构建任务。

下载链接：https://maven.apache.org/download.cgi

![image-20231016102907302](https://s2.loli.net/2023/10/16/8Tx3krho7OSeVD9.png)

将二进制包放到安装路径（如`/usr/local`）后解压即完成安装。

接下来配置环境变量。编辑`~/.zshrc`（用vscode或vim），附加以下代码。

```bash
export MAVEN_HOME=/usr/local/apache-maven-3.8.8
export PATH=$MAVEN_HOME/bin:$PATH:.
```

在terminal中输入以下指令

```bash
source ~/.zshrc
mvn -v
```

如果输出以下信息说明安装正确。maven链接的runtime路径（下图红框选中的部分）应与`JAVA_HOME`保持一致。

![image-20231016104513113](https://s2.loli.net/2023/10/16/TMZqGgkxh7PwvRS.png)



# 三、maven部署

在terminal中进入项目文件夹（`pom.xml`所在的文件夹），输入`mvn clean install`进行依赖的安装。出现如下信息说明安装正确。

![image-20231016110650787](https://s2.loli.net/2023/10/16/oXLS1RIwDHf2WkY.png)

如果在第一步中 java 的环境变量配置不正确，maven链接的runtime路径（上图红框选中的部分）为`Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home`。输入`mvn clean install`后会出现如下错误。需要重新配置java的环境变量。

![在这里插入图片描述](https://s2.loli.net/2023/10/16/O7sKZB1imPxrFJj.png)

