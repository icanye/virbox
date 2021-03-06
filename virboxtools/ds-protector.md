# DS Protector

## DS 产品化\_支持各种解决方案文档 {#ds-产品化_支持各种解决方案文档}

## 实现原理

> 文件读取方式

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds1.png)

> 我们如果要对文件内容进行过滤和处理必须要加入一层

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds2.png)

> 这个过滤层就是我们的插件实现的功能，它是一个动态链接库，在加壳的时候会被插入到加壳的文件（ exe 或者 dll \)中。在运行的时候会被加载到内存，然后执行初始化函数，就将文件的操作挂钩，然后文件的操作都将被这个插件进行过滤。对于加密的文件进行解密，对于未加密的文件还是按照原流程处理。
>
> 具体的文件操作和处理：

* &gt;文件的操作：打开，读取，写入，移动指针，获得属性，关闭
* &gt;使用钩子截获文件的打开，读取，移动指针，获得文件大小，关闭的事件。
* &gt;在文件打开的时候，判断文件是否被加密，并登记到列表中
* &gt;在文件读取的时候, 读取并解密文档，返回
* &gt; 在文件移动指针的时候，确保指针不要移动到原文件大小之外
* &gt;在获得文件大小的时候，要返回文件原来大小
* &gt; 在关闭的时候从登记列表中删除

> 在应用层实现的缺陷

windows 的文件读取的层次

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds3.png)

> 各层之间的内容可能不同，我们现在只是在文件-内存之间实现挂钩

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds4.png)

> **那么当应用读取文件的方式采用缓存的方式的时候，我们就不能拦截文件的读写就不能进行解密**

**应用层实现资源加密解密依赖于应用的实现**

## 测试的范围

| 序号 | 软件名称 | 类型 | 支持or不支持 |
| :--- | :--- | :--- | :--- |
| 1 | python | 语言类 | Y |
| 2 | lua | 语言类 | Y |
| 3 | perl | 语言类 | Y |
| 4 | erlang | 语言类 | Y |
| 5 | ruby | 语言类 | Y |
| 6 | go | 语言类 | N |
| 7 | php | 语言类 | N |
| 8 | R | 语言类 | N |
| 9 | Unity游戏 | 游戏类 | Y |
| 10 | UE4游戏 | 游戏类 | 部分支持 |
| 11 | Potplayer | 播放软件 | Y |
| 12 | 暴风影音\(安装版\) | 播放软件 | Y |
| 13 | 暴风影音绿色版 | 播放软件 | N |
| 14 | jar,war web or 客户端 | 开发环境 | Y |

## 分类说明以上支持的软件的资源保护方法

### 语言类的使用方法

####  **python 语言**

```text
安装版本：
2.7.6
1.添加环境变量：添加环境变量：在我的电脑->属性->高级->环境变量
2.变量名：path 变量值：C:\Python27(python的安装目录)
3.打开命令行，输入python回车，显示版本号则配置成功
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/python1.jpg)

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/python2.jpg)

```text
4.对安装目录下如C:\Python27
中python.exe进行加壳
5.打开DS，导入刚加壳生成的配置工具，添加所需要保护的demo，点击保护
6.进入demo所在的目录下，运行如python_demo.py
```

####  **lua 语言**

```text
安装版本：5.3.4
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/lua1.jpg)

```text
1.安装完成之后命令行中输入lua，若出现版本号则表示安装成功
2.若提示不是内部命令，需要在我的电脑->属性->高级->环境变量，变量名path 变量值：lua的安装目录
3.再次在命令行中输入lua，出现版本号则表示配置成功
4.对安装目录下的lua.exe进行加壳。
6.进入demo所在的目录下，运行如lua demo.lua
```

#### **perl 语言**

```text
安装版本：5.26.1
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/perl1.jpg)

```text
1.安装完成之后命令行输入perl --version，若出现版本号则表示安装成功
2.若提示不是内部命令，需要在我的电脑->属性->高级->环境变量，变量名path 变量值：perl的安装目录
3.再次在命令行中输入perl --version，出现版本号则表示配置成功
4.对安装目录(如：C:\Strawberry\perl\bin)下的perl.exe进行加壳。
5.打开DS，导入刚加壳生成的配置工具，添加所需要保护的demo，点击保护
6.进入demo所在的目录下，运行如perl demo.pl
```

####  **erlang 语言**

```text
安装版本：9.1
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/erlang1.jpg)

```text
1.安装完成之后命令行输入erl，若出现版本号则表示安装成功
2.若提示不是内部命令，需要在我的电脑->属性->高级->环境变量，变量名path 变量值：erlang的安装目录
3.再次在命令行中输入erl，出现版本号则表示配置成功
4.对安装目录(如：C:\Program Files\erl9.1\bin)下的erl.exe进行加壳。
5.打开DS，导入刚加壳生成的配置工具，添加所需要保护的demo，点击保护
6.进入demo所在的目录下，运行如erl demo.erl
```

#### **ruby 语言**

```text
安装版本：2.4.2
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ruby1.jpg)

```text
1.安装完成之后命令行输入ruby --version，若出现版本号则表示安装成功
2.若提示不是内部命令，需要在我的电脑->属性->高级->环境变量，变量名path 变量值：ruby的安装目录
3.再次在命令行中输入ruby --version，出现版本号则表示配置成功
4.对安装目录(如：C:\Ruby24-x64\bin)下的ruby.exe进行加壳。
5.打开DS，导入刚加壳生成的配置工具，添加所需要保护的demo，点击保护
6.进入demo所在的目录下，运行如ruby demo.rb
```

### 游戏类的使用方法

#### Unity 游戏 {#游戏类的使用方法}

```text
文件目录如下
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/unity1.jpg)

```text
对上面目录中的exe进行加壳处理
```

```text
脚本目录，可以对Assembly-CSharp.dll进行保护
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/unity2.jpg)

```text
打开DS，导入刚加壳生成的配置工具，添加所需要保护的Assembly-CSharp.dll，点击保护
```

```text
数据目录，可以对*.resS进行保护
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/unity3.jpg)

```text
打开DS，导入刚加壳生成的配置工具，添加所需要保护的数据文件，点击保护
```

### 播放类软件的使用方法

#### **PotPlayer**

```text
选择了一个绿色免安装的视频播放器，运行程序PotPlayerMini.exe
对此程序进行加壳，打开DS，导入刚加壳生成的配置工具，添加所需要保护的视频，点击保护，运行加壳过后的程序。
```

#### **暴风影音\(安装版\)**

```text
安装的是5.72.921.1111，运行程序 StormPlayer.exe
对此程序进行加壳，打开DS，导入刚加壳生成的配置工具，添加所需要保护的视频，点击保护，运行加壳过后的程序。
```

### 开发环境

####  **java 的 war 和 jar 包的加密**

```text
1.对war包进行加壳
1.1、可以先启动程序然后在资源管理器中找到对应程序，打开所在位置，找到对应的程序可以再次进行加壳。
我的安装目录如下：D:\apache-tomcat-9.0.0.M21\webapps
先启动tomcat服务确认能正常启动，启动过后该War包会自动解压出一个同名的文件夹。
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/war1.jpg)

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/war2.jpg)

```text
对java.exe进行加壳，对war包文件夹里的class进行资源保护（可根据自己情况选择），然后重启tomcat，
输入http://localhost:8080/myhome.ssp(根据自己的war包名)进行验证。
1.2、若在控制面板-管理工具-服务中启动Tomcat，需要对tomcat9.exe程序进行加壳(需按照自己查看自己电脑上对应的哪个程序)。
方法：可以先启动程序然后在资源管理器中找到对应程序，打开所在位置。
```

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/war3.jpg)![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/war4.jpg)![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/war5.jpg)

```text
注：若服务中没有找到tomcat，需要切换到tomcat\bin目录下，执行命令service install 服务名
（我得是9，service install tomcat9），若没有也没必要加入到服务中。
2、jar包进行加壳
执行程序一般都是对java里jre目录下的java.exe进行加壳
对javaw.exe或java.exe进行加壳，打开DS，导入刚加壳生成的配置工具，添加所需要保护的jar，点击保护,
然后运行jar包，命令为javaw –jar bounce.jar或java -jar bounce.jar
```

