Ubutnu离线安装Typora

1.在Typora官网下载安装包https://www.typora.io/#linux

在根目录已下载安装包:

```
Typora-linux-x64.tar.gz
```

2.解压安装包

```bash
1  sudo tar -zxvf Typora-linux-x64.tar.gz
```

3.将解压出来的bin文件夹下的Typora-linux-x64文件夹移动到安装文件夹下，我这里将Typora安装在/usr/local/文件夹

```bash
1  cd bin
2  sudo mv Typora-linux-x64 /usr/local/
```

4.创建Typora的快捷启动

Ubuntu中的快捷启动都在/usr/share/applications目录中

```bash
1  cd /usr/share/applications
2  sudo gedit typora.desktop
```

在创建的typora.desktop文件中写入如下内容：

```bash
Encoding=UTF-8
Name=Typora
Exec=/usr/local/Typora-linux-x64/Typora
Icon=/usr/local/Typora-linux-x64/resources/app/asserts/icon/icon_256x256@2x.png
Categories=Application;Development;Java;IDE
Type=Application
#Terminal=1
```

5.创建Typora终端快捷启动

```bash
1.  gedit .bashrc
2.  alias typora="/usr/local/Typora-linux-x64/Typora"
3.  source .bashrc
```

安装配置完成后，以后就可以直接打开终端，输入typora命令启动Typora程序进行新建和文档编辑了