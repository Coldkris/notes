###1）上传安装文件并解压缩

将jdk-8u151-linux-x64.tar.gz上传至服务器/home/soft目录，如果没有该目录，请使用mkdir 进行创建。
解压缩：tar -zxvf jdk-8u151-linux-x64.tar.gz

###2）修改配置文件

**sudo vim /etc/profile**
<p>将以下配置增加至profile文件末尾</p>
```java
JAVA_HOME=/home/ewallet/soft/jdk1.8.0_151
JRE_HOME=/home/ewallet/soft/jdk1.8.0_151/jre 
PATH=$PATH:$JAVA_HOME/bin:$JRE_HOME/bin  
CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib  
export JAVA_HOME JRE_HOME PATH CLASSPATH

```

使用命令使得配置立刻生效：source /etc/profile
