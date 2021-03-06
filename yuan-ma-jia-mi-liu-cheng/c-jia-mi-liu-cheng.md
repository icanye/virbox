# C\# 加密流程

## 使用 Virbox Protector 加壳工具

从 Virbox 开发者工具盒打开加壳工具，将待加密软件拖入到加壳工具中

注：使用加壳工具的前提是点击“下载” SDK，并安装

![](https://github.com/virboxzhou/virbox/blob/master/assets/import100.png?raw=true)

![](https://github.com/virboxzhou/virbox/blob/master/assets/import102.png?raw=true)

加壳工具目前支持对可执行 exe 和 dll 加壳，支持的开发语言以及开发框架：

C、C++、.Net、VB6.0、Deliph、Java、ARX插件、Revit\(插件\)、Unity3D、UE4、PHP、Labview、Mathlib、Python、Lua、VF、go、Perl、Revit 软件中所有格式得资源文件、视频、音频PPT、游戏资源

本示例主要以.net 语言开发的贪吃蛇为例：

![](https://github.com/virboxzhou/virbox/blob/master/assets/import122.png?raw=true)

## 设置加壳工具

![](https://github.com/virboxzhou/virbox/blob/master/assets/import101.png?raw=true)

**登录云锁**：

即登录 Virbox LM 平台开发者账号

**许可形式：**

勾选相应许可形式 ![](https://github.com/virboxzhou/virbox/blob/master/assets/import106.png?raw=true)

此处勾选的许可形式需要与发布给用户的许可类型一致，[四种许可类型简介](https://github.com/virboxzhou/virbox/blob/master/Virbox/si-zhong-xu-ke-jian-jie.md)

**许可 ID：**

许可 ID 需要自定义，是 1-42 亿数字范围。

许可 ID 是加密过程中需要使用的一个重要概念，是加密后软件和授权唯一的标识，也可以代表软件开发商的一个产品或者一个模块，许可 ID 在下一步的发布许可中会直接用到。

**API 密码：**

进入 Virbox LM 开发者平台，页面顶部点击“查看”，将 API 密码输入至此![](https://github.com/virboxzhou/virbox/blob/master/assets/import107.png?raw=true)

**锁序列号：**

如果输入锁序列号，则加壳后的程序只有此锁可用。\(此功能只针对硬件锁\)

**被保护函数列表:**

 ****点击 “+” 按钮： ![](https://github.com/virboxzhou/virbox/blob/master/assets/import110.png?raw=true)对加壳前的软件进行预分析，建议对比较重要的函数选择碎片代码的保护方式，开发者需要在软件性能与安全之间平衡，如果对调用次数过多的函数选择碎片化保护，可能会影响软件的运行速率，调用次数过多的函数建议使用不保护的方式（仅支持 exe 文件）。

![](https://github.com/virboxzhou/virbox/blob/master/assets/import132.png?raw=true)

**加密选项：**

建议对 exe 文件勾选压缩和导入表保护选项：勾选压缩后软件更安全，此压缩为带密码的压缩。

DS 插件在此处默认关闭即可

![](https://github.com/virboxzhou/virbox/blob/master/assets/import115.png?raw=true)

**消息选项：**

设置许可失效时提示的形式、设置提示标题、软件剩余时间、剩余次数以及其他提示消息

![](https://github.com/virboxzhou/virbox/blob/master/assets/import113.png?raw=true)

**软件加壳：**

设置好相应的选项后，点击加壳按钮，对软件进行加壳保护

![](https://github.com/virboxzhou/virbox/blob/master/assets/import116.png?raw=true)

## 加密后文件

加密前的软件（以一个 .net 开发的贪吃蛇 .Net\_RetroSnaker.exe 为例）

![](https://github.com/virboxzhou/virbox/blob/master/assets/import133.png?raw=true)

加密后的软件

![](https://github.com/virboxzhou/virbox/blob/master/assets/import134.png?raw=true)

①加壳前的软件原文件 xxx.exe，将此文件剪切备份至其他文件夹

②加壳后的配置文件xxx.exe.ssp，此配置文件主要记录API密码和一些配置信息，可删除。

③加壳后的软件xxx.ssp.exe，建议将加壳后的软件名称修改为原文件名称。

至此使用加壳工具加密的过程已经完成，下一步根据不同用户的不同需求发布不同的许可内容到用户的账号中,详见[发布许可流程（授权）](https://github.com/virboxzhou/virbox/blob/master/xu-ke-liu-cheng.md)

