## Mac OS下配置Scala环境

下载scala，进入scala下载目录`cd Downloads` 

将scala-2.12.3.tar改名为scala`mv scala-2.12.3.tar scala`，

将其移动到/Documents/MyApp下`mv /Downloads/scala  /Documents/MyApp`下，

解压`tar -zxvf scala-2.12.3.tar`，进入解压文件，输出当前路径`pwd`，

进入用户环境`sudo vim ~/.bash_profile` 输入密码，在环境变量中加上配置如下

```shell
JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_144.jdk/Contents/Home
`SCALA_HOME=/Users/zhangjiachen/Documents/MyApp/Scala`
PATH=$JAVA_HOME/bin:`$SCALA_HOME/bin:`$PATH
CLASSPATH=.:$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar
export JAVA_HOME `SCALA_HOME` PATH CLASSPATH
```

使更改生效`souce ~/.bash_profile`

在终端输入`scala -version` 弹出版本信息则配置成功