# Virbox Protector

## 概述

深思数盾自动保护工具 Virbox Protector ，是深思数盾科技股份有限公司经过多年技术深耕开发的一款高强度自动保护（加密）工具。Virbox Protector 与 Virbox 用户工具、Virbox 云许可或软许可或精锐 5 配套使用，集自动代码移植、混淆、外壳加密、数据加密于一身，无需编程就能达到极高的保护强度，是业界领先的软件保护工具。

## 联系我们

深思数盾加壳工具技术支持 QQ:2852513869

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/qrcode.png)

## 产品导航页

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/jiakedaohang.png)

通过三种途径开始您的软件保护之旅：

1. 将可需要保护的程序拖拽到窗口，进入加壳程序的主界面。
2. 点击【新建】目录下面的【打开】按钮，打开需要保护的程序，进入加壳程序的主界面。
3. 如果您已经在最近使用 Virbox Protector 保护过您的程序并保留该历史记录，您可以在【最近打开的工程】目录中找到您的程序并且单击打开程序，进入加壳程序的主界面。

## 产品主界面

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/jiakezhujiemian.png)

### 菜单栏

#### 打开

点击【打开】按钮，打开一个需要加壳的程序，用户可以选择 XXX.exe 或者是 XXX.dll ，进入加壳程序的主界面 。 \[ 注意：如果被加壳程序的相同目录下存在 XXX.map 文件，那么会自动加载 map 文件，将函数名称显示在界面当中，目前支持 vs 、 vc 、 bcb 、delphi 编译器生成的 map 文件 \]

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/jiakeopen.png)

#### 最近打开的文件

点击【最近打开的文件】按钮 ，系统罗列出 5 个最近保护过的程序，单击选择需要打开的程序，进入加壳程序的主界面。

#### 保存

点击【保存】按钮，保存当前工程信息到 \[ 需要保护程序名称 .ssp\] 文件中。

#### 立即加壳

点击【立即加壳】即可绑定授权并生成保护后的应用程序 . 如果工程信息有所改动，那么点击【立即加壳】也会保存工程文件；如果工程信息未被修改，那么点击【立即加壳】不会保存工程文件。注意： \[ 用户锁中必须存在和模块编号相同的许可 ID 才能够打开加壳之后的软件 \]

#### 登录云锁

点击【登录云锁】用户登录开发者账户，使用云控制锁进行加壳。如果不登录云控制锁，那么系统默认使用本地控制锁进行加壳，系统目前支持本地控制锁加壳和云控制锁加壳两种模式。 \[ 特别注意：此处的云控制锁，登录的是开发者账户，而非普通的用户 \]

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/jiakelogin.png)

### PIN 功能

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/pin_show.png)

#### 什么是 PIN 功能

PIN 功能提升开发锁使用安全性，使用前必须输入正确 PIN 码才能正常使用开发锁完成许可签发、软件加壳等操作。在加壳工具中加密锁存在以下几种 PIN 状态的显示。

#### 支持 PIN

开发锁支持 PIN 功能， 3.1.20 版本及后续版本的开发锁默认支持 PIN 功能。

#### 不支持 PIN

开发锁不支持 PIN 功能， 3.1.20 之前版本的开发锁不支持 PIN 功能，加壳工具截止至 2019-04-01 前，允许不支持 PIN 的开发锁进行软件加壳。

#### 已启用PIN {#已启用pin}

开发锁已启用PIN，启用状态下，每次使用开发锁前必须进行PIN验证，验证通过后才能正常使用

#### 未启用PIN {#未启用pin}

开发锁支持PIN但未启用，未启用状态下，使用开发锁不需要进行PIN验证即可使用。不启用PIN降低了开发锁的安全性，不建议主动禁用PIN验证功能。

#### 已验证PIN {#已验证pin}

开发锁支持PIN，并通过PIN验证，只有此状态下的开发锁能进行许可签发、软件加壳操作。

#### 未验证PIN {#未验证pin}

开发锁支持PIN，但未通过PIN验证，在未输入正确PIN码通过验证前，开发锁将不允许进行许可签发、软件加壳操作。

### 导航栏

#### 授权信息

许可形式，保护后的软件可以使用的许可所在的载体。包括本地加密锁中的许可，表示插在用户本机器上的硬件锁；网络加密锁，插在局域网内其他机器上的硬件锁中的许可；云锁，云端虚拟的加密锁中的许可；软锁中的许可，软锁是用纯软件实现的加密锁，不依赖任何硬件锁，跟 PC 机器硬件唯一指纹绑定。

**许可 ID**

开发者用于管理用户软件版权控制与发放凭证的一个序列号，开发者能够在开发者中心分发给普通的云账户，同时开发者也可以通过开发者管理工具为用户锁分发许可。

**开发者密码**

与开发者 ID 相对应的 32 个字符表示的序列号，保证了开发者的云授权平台的安全， 每个开发者有一个唯一的开发者密码。开发者登录 Virbox LM 平台获取。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/jiakekaifamima.png)

**锁序列号**

一串 32 个字符表示的，能够唯一确定加密锁的序号，如果软件保护使用了指定的锁序列号，那么保护后的程序只能使用指定序列号的用户锁才能打开。需要保护的具有重要价值的函数块，用户能够选择混淆和碎片化代码的保护方式。

**查看函数的详细信息**

鼠标点击函数保护列表中的函数，在右侧的工作区窗口中展示函数的详细信息，包括函数的保护方式、函数名、函数的地址和汇编代码的展示。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/jiakecode.png)

**函数的保护方式**

用户能够选择不保护、混淆、碎片化、虚拟化四种种保护方式。

#### 被保护的函数列表

需要保护的具有重要价值的函数块，用户能够选择混淆和碎片化代码的保护方式。

**查看函数的详细信息**

鼠标点击函数保护列表中的函数，在右侧的工作区窗口中展示函数的详细信息，包括函数的保护方式、函数名、函数的地址和汇编代码的展示。

**函数的保护方式**

用户能够选择不保护、混淆、碎片化、虚拟化四种种保护方式。

| 序号 | 保护方式 | 说明 | 存在的问题 |
| :--- | :--- | :--- | :--- |
| 1 | 不保护 | 对选中的指令不进行保护 | 无 |
| 2 | 混淆 | 将代码指令翻译为机器和人都无法识别的一串伪代码字节流，在具体执行时在对这些伪代码进行翻译解释，逐步还原为原始代码并执行 | 无 |
| 3 | 碎片化 | 将指令翻译成 arm 指令，并置于加密锁内执行 | 对指令有一定的格式要求，有的函数可能不能被保护 |
| 4 | 虚拟化 | 将指令编译为虚拟代码 , 放在指定虚拟机中运行 | 对指令有一定的格式要求，有的函数可能不能被保护 |

**添加保护函数的方法**

1 、使用 SDK 标签，编程方式添加需要保护的函数。

2 、点击【添加】按钮，可视化选择添加保护函数。

**删除保护函数的方法**

1 、右键单击【被保护函数列表】 -&gt; 【清空列表】，即可实现保护列表框的清空操作。

2 、将鼠标滑动至需要删除的函数名称上，点击【 X 】。

#### 加密选项

**输出文件**

输出文件，可以修改程序保护后生成文件的路径和名称。 \[ 注意： 1 、如果只有文件名称，那么路径为源程序的路径； 2 、如果输出文件名和源文件同名，生成的程序会将源程序覆盖 \]

**压缩**

压缩，对加壳后的后的程序进行压缩处理，减小体积，同时可以防止静态反编译。 \[ 特别说明： 1 、由于压缩模块需要一个固定大小的空间，如果被加壳的程序非常小压缩的效果并不明显还有可能出现体积更大的情况，对于体积较大的程序效果明显 2 、不支持 DotNet 动态库的压缩 3 、不支持 arx 类型程序的压缩 \]

**名称混淆**

名称混淆，对源程序中的函数名称进行混淆，静态反编译工具显示的函数名为乱码。 \[ 特别说明：名称混淆目前只能支持 DotNet 程序，并且不支持 IIS 类型程序的混淆 \]

**加密资源段**

加密资源段，对被保护程序的资源区段进行加密，运行的时候需要用户使用相应许可进行解密方可使用程序。 \[ 特别说明：加密资源段目前只能支持本地程序 \]

**生成日志**

生成 Virbox Protector 的工作日志，方便出错的时候排查问题。正常情况下您可不选，只有在加壳后的程序运行出现问题的时候，您需要选择并将生成的日志发给深思技术人员进行排查问题。

**后台检测时间间隔 \( 秒 \)**

后台检测时间间隔（秒），表示每隔多少秒对运行程序进行检测是否存在对应许可，如果没有那么就会提示错误，或者退出。如果后台检测时间设为 0s, 那么后台就不会进行检测许可的操作。

#### 消息选项

**提示语言**

设置弹出消息框文字的语言，包括简体中文、英文，繁体。

**许可失效提示形式**

许可失效提示形式，主要是用于设置，加壳后的程序找不到指定的许可的时候，如何进行提示。目前支持

1 、程序不提示消息，直接闪退；

2 、程序可继续运行，点击确定后退出；

3 、程序冻结，用户可选择重试连接许可或退出；

4 、允许可找不到时，弹出登陆框；

5 、远程桌面服务会话消息框（支持 vista 和 server2008 以上版本）等五种不同的提示形式。 注意：如果是对 autocad 的 arx 程序进行加壳，建议选择第五种许可会话失效提示形式。

**延迟退出时间 \(s\)**

当许可会话已经失效时，会弹出提示框，如果此时选择了 “ 取消 ” 那么您的程序会在设定的延迟退出时间到达的时候退出，这样做的目的是给客户提供了存档的时间。

**提示标题**

设置弹出消息框的标题信息。

**自定义信息**

对主要的许可状态信息进行显示，开发者按照一定的格式自定义编辑提醒消息，使保护后的程序更加的人性化的向用户展示许可状态

信息。

**云锁登陆错误信息**

主要是针对加壳后程序找不到许可的时候，许可失效提示形式选择了第四种，那么会弹出云账号登陆框，如果此时登录出错那么本程序会显示对应的错误消息。

**错误信息**

定义了对应的错误码显示的提示信息，错误信息的格式为【 8 位 16 进制错误码 - 错误信息】，可以添加错误消息也可以删除错误消息，如果没有自定义错误消息，那么加壳后的程序出现错误的时候会弹出系统错误信息。【详细的错误码介绍请参见 SDK 中的 ss\_error.h 文件】

### 状态栏

状态栏中从左到右分别显示了被保护程序的文件的全路径、程序的版本、程序的类型以及程序的硬件机器版本。

### 可视化添加函数模块

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ssprotect_select_fun.png)

**函数搜索**

在搜索框中输入关键字，程序会列出所有名称中包含关键字的函数块，并且彩色显示，支持模糊查询

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/addhanshu.png)

**性能分析**

点击性能分析按钮，运行需要保护的程序，执行正常的业务操作，然后关闭程序后，程序中各个函数模块调用的次数即可显示在列表中，参见上图。如果当前分析的程序位为 ll 程序，需要选择启动模块。

**可保护函数列表**

展示了需要保护程序的所有的函数模块，托管代码程序和非托管代码程序有细微的差别。 \[ 注意：并不是所有的函数模块都能展示出来。 1 、指令大小小于 15 个字节的函数模块不会展示； 2 、有的非常规函数模块不会展示（名称中存在 '.' 、 '&lt;' 、 '&gt;' 、 '@' 、 ':' 、 '?' 等）。 \]

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ssprotect_fun_tree.png)

**托管代码程序**

1 、函数名称为 “ 命名空间 + 类名称 + 函数名称 ” 。

2 、函数列表能够切换为列表的模式和树形模式，点击表头【已添加】右侧的按钮实现切换。

* **树形模式展示**
* **列表模式展示**

  ![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ssprotect_fun_list.png)

* 列表模式中，点击列表头能够实现排序。

3 、函数选择支持 【 Control + A 】、【 Control + 鼠标】和【 Shift + 鼠标】等。

4 、函数的保护方式支持右键选择

5 、选择了保护方式后【已添加】会表示为已选择。

**非托管代码程序**

1 、函数名称为函数的 va 的值

2 、展示列表只有列表一种模式

其余的功能和托管代码程序一致。

**信息展示**

可保护函数列表信息展示，显示了函数的总个数、已添加函数个数、混淆函数个数、碎片代码函数个数

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/xinxizhanshi.png)

**添加**

点击【添加】按钮，退出窗口，并将函数添加到主页面的被保护函数列表当中

**取消**

点击取消，退出窗口，不做任何修改。

### 如何使用 sdk 标签，添加需要保护的函数模块

sdk 工具包，包括头文件、静态库以及动态库，用户在编程的过程中将 sdk 标签静态载入到需要保护的函数当中，这样生成的可执行程序，在 Virbox Protector 加壳工具中就能够分析出 sdk 表示的函数，这样就能够找到用户的核心代码所在的位置。目前支持， VBProtectBegin （常规保护）， VBVirtualizeBegin （虚拟化保护）， VBMutateBegin （混淆化保护）， VBSnippetBegin （碎片化代码保护） ,VBProtectDecrypt\( 许可加解密 \) 。 \[ 注意： sdk 标签能方便用户找到关键代码 \]

sdk 标签使用需要注意以下几点：

sdk 标签使用

1 、 sdk 只能静态加载，不支持动态加载 dll （即 loadlibraryA 的方式）。

2 、 VBProtectBegin 、 VBVirtualizeBegin 、 VBSnippetBegin 以及 VBMutateBegin 等接口，传入的字符串参数，不能与其他函数共用。

3 、传入的字符串参数保证为 ANSII 码的形式，这样显示在界面上的函数名称才正确，否则就会显示为乱码。

4 、每个 Begin 对应一个 End ，总是成对出现，并且一个函数里面不要出现多对 begin+end 。

5 、如果 sdk 表示的保护方式和工程文件中保存的保护方式冲突了，以工程文件中的保护方式为准。

6 、 begin+end 锁定代码最好大于 3 行代码。（因为锁定的代码正汇编生成的指令小于 15 个字节，那么不会显示在加壳工具界面上）

7 、 sdk 动态库，分为 32 以及 64 位，在使用的时候要开发者根据要编译的程序位数进行加载对应的库。

8 、目前明确不支持的语言：易语言、 java 程序、 unity3d

9 、 begin/end 不支持嵌套使用

10 、 VBProtectDecrypt 被加密的字符串或者是缓冲区的长度必须是 16 的倍数，例如 char g\_test\_string\[16\] = {"test\_decrypt"};

11 、 VBProtectDecrypt 传入缓冲区和传出缓冲区不能是同一个缓冲区

12 、 VBProtectDecrypt 传入的缓冲区只能放在函数外，即全局变量。具体的使用参照 demo

13 、 .Net 程序暂时不支持 VBProtectDecrypt

### 如何使用自定义插件 {#如何使用自定义插件}

#### 自定义插件 {#自定义插件}

我们以外壳工具目录下面的demo为例进行介绍：

1、首先编写插件的dll，格式请查看demo工程中的文件demo.cpp

2、编写插件配置文件“XXX.xml”，书写规则如图

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/import1.png)

#### 插件使用 {#插件使用}

1、文件的格式

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/import2.png)

2、插件文件存放在 plugin 目录下

#### 界面显示 {#界面显示}

1、插件在加壳工具中显示

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/import3.png)

2、加壳后程序的插件显示

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/import4.png)

## 问题及解决方法 {#问题及解决方法}

### 什么是许可 {#什么是许可}

LM 本质就是「加密与管理」。 深思许可管理（Sense License Mangment）是一套深思数盾根据中国国情、多年用户深度定制的经验与市场独特理解的许可管理解决方案，其本质是控制软件能否使用，尤其在领先的【移植算法】的理念保证下，解决软件无锁情况下试用、加密锁丢失甄别等棘手问题提供技术支持，达到超安全性与软件许可灵活性的平衡。同时针对企业内部挑战如加密开发难度高、加密方案泄露风险\(加密人员离职\)、私自烧狗等，提供强有力的工具与平台。 许可是软件版权的控制与发放（sofeware license），本质就是允许让最终用户能否使用软件的技术控制。本文主要讲的是技术控制，其中分为许可技术和许可管理。 许可的技术控制：可以区分许可内容、 许可使用时间、 使用次数、 软件并发限制、同时登录软件系统的在线人数限制等功能限制。 许可管理： 对许可使用、许可生命周期（产品创建、许可的生成、许可的发放、许可的吊销）的管理和用户的管理，综合为许可管理。

### 许可获取以及许可的更新、删除操作 {#许可获取以及许可的更新删除操作}

#### 使用开发商工具签发许可 {#使用开发商工具签发许可}

#### 新建 {#新建}

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_product_add.png)

#### 编辑 {#编辑}

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_module_product_edit.png)

其中，锁定的意思是：选择后，新建模板及授权后，该数据区不可修改。

#### 删除 {#删除}

选中要删除的产品，点击“删除”按钮。**注意**：删除产品时，会同时删除通过该产品创建的所有许可模板。

### 授权管理 {#授权管理}

授权管理包括模板的新建、编辑、删除功能，以及许可发布和已签发记录查看功能。

不同类型许可具有近似特征，重复操作一类许可不仅浪费时间，还会出现操作失误，不利于产品的管理和许可签发。深思使用模板的方式固化常用的许可类型，一次设定、反复使用，来减少开发者的工作量，提高效率。

#### 新建模板 {#新建模板}

* 选择产品

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_module_product_select.png)

* 填写授权信息

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_new_module_set_lic.png)

#### 编辑模板 {#编辑模板}

选择已有的许可模板，编辑模板信息。

#### 删除模板 {#删除模板}

选中要删除模板，点击“删除模板”按钮。

#### 发布许可 {#发布许可}

* 选中要发布许可模板，点击“发布许可”。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_module_product_select.png)

* 编辑授权信息

发布前可以对许可进行临时修改，适应于少量的改动的情况。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_module_product_edit.png)

* 选择硬件锁

选择要签发许可的硬件锁，支持批量给多把锁签发许可。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_module_product_select_lock.png)

* 许可签发 点击“发布”，发布成功。

#### 查看已签发许可 {#查看已签发许可}

查看已经签发的许可信息，如下图：

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/LicMgr_look_lic.png)

#### 以 WEB 方式签发云许可 {#以-web-方式签发云许可}

第一步 登录[开发者网站](http://developer.senseshield.com/auth)的云账号

第二步 新建产品

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/UI_cloud_new.png)

第三步 新建正式模板

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/UI_cloud_module.png)

第四步 新建用户

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/UI_cloud_input_username.png)

第五步 许可分发

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/UI_cloud_license.png)

第五步 在许可管理工具中查看发布结果

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/UI_cloud_success.png)

### 加壳后的程序在哪里 {#加壳后的程序在哪里}

问题描述：有一部分用户，找不到加过壳的程序，错误的将自己原始的程序当成加壳保护过的的程序。 解决方法：我们以扫雷程序Mine.exe 为例，加壳保护后的程序为 Mine.ssp.exe，与 Mine.exe 为同一目录下。

### 加密后的软件 360 报毒 {#加密后的软件360报毒}

问题描述：使用加壳工具对开发者软件进行加壳，然而加密后的程序 360 认为是病毒软件。

解决方法：提交 360 认证

第一步：软件中可执行文件（不包含驱动程序 .sys ）及打包后的可执行文件使用沃通（Wosign）签名（使用沃通代码签名工具并且购买代码签名证书进行签名，沃通签名相关问题请咨询沃通官方网站客服人员，沃通签名在 360 认证过程有很大帮助）。

第二步：注册并登录 360 开放平台：[http://open.soft.360.cn/](http://open.soft.360.cn/)

第三步：在“我的软件”页面中选择提交我的软件，如下图：

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/UI_360_authentication.png)

第四步：选择“仅安全检测”，并填写软件名称，软件版本（主要为了后续记录查看），提交方式可以选择本地上传安装包，然后提交软件。

第五步：同时可以在“软件列表”中查看已经提交过的待检测软件和“通过检测”的软件。目前软件提交后通过检测的时间大约为1天。

### 加壳软件已知问题汇总 {#加壳软件已知问题汇总}

* 不支持二次加壳，无论是第三方还是本程序加壳后的文件，都不能再次进行加壳。
* .NET加壳不支持第三方运行时库，只支持微软标准运行时库。
* 使用命令行加壳时，其目标程序的配置文件必须存在。
* 在.NET程序中使用类似 GetField\("name", bindingAttr\)函数时，加壳后名称混淆可能出现异常，[如果.NET](http://xn--bvs014a.NET)程序加壳后运行失败，尝试去掉名称混淆。
* sdk 标签不支持含有本地代码的托管程序。
* 对函数块进行碎片化代码保护的时候，存在不能成功保护的情况，主要原因是，碎片代码对指令的长度过小，指令可能不可移植，存在跳转等情况。
* 有的软件加壳后需要把名称改为原来的名称才能运行。\(例如：程序 Mine.exe，加壳后的程序为 Mine.ssp.exe，假如程序Mine.ssp.exe 不能成功启动，有可能需要将 Mine.ssp.exe 改为 Mine.exe 才能正常使用\)。
* 如果程序中存在附加数据，加壳后的程序可能会出现未知的问题。
* AUTOCAD 的 arx 插件程序只能选择“远程桌面服务会话消息框”，并且目前只支持 win7 和 server2008 以上的版本。
* Unity3D 程序选择“程序冻结，用户可选择重试连接或退出”的许可失效提示形式，程序会崩溃。
* 如果是 spring 框架的 java 程序，请使用资源加密的方式保护。
* linux 程序和 mac 程序，不支持二次加壳，并且加壳工具无法检测被加壳的程序是否为二次加壳。
* 对 linux 和 mac 程序加壳，设置选项中生成日志若勾选之后无法生成日志。
* 对 linux 和 mac 程序加壳，不能同时勾选ds，否则可能会造成程序运行失败。
* 暂不支持加壳后的 so 用 gcc 链接到源码文件。
* 如果用户的机子上装有杀毒软件 AVAST，可能会出现加壳后的程序无法运行的情况。导致此问题的原因是，当加壳程序运行的时候 AVAST 会杀死加壳程序的进程。

### 加壳工具目前已经测试的可以支持的范围 {#加壳工具目前已经测试的可以支持的范围}

| 序号 | 名称 | 类型 | 备注 |
| :--- | :--- | :--- | :--- |
| 1 | .Net |  |  |
| 2 | PE |  |  |
| 3 | java |  |  |
| 4 | arx | 插件 |  |
| 5 | vb |  |  |
| 6 | pb |  |  |
| 7 | vc |  |  |
| 8 | delphi |  |  |
| 9 | Unity3d |  |  |
| 10 | c++ |  |  |
| 11 | bcb |  |  |
| 12 | .Dylib库 |  |  |
| 13 | maco可执行文件 |  |  |
| 14 | .so库 |  |  |
| 15 | elf可执行文件 | Exec、Dyn |  |

### 如何使用 VirboxProtector\_con.exe 命令行加壳工具 {#如何使用virboxprotector_conexe命令行加壳工具}

1、首先在运行输入框中输入"cmd.exe" 打开控制台命令窗口

2、输入 路径 +VirboxProtector\_con.exe /? 可以查看帮助信息

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/con_help.PNG)

**命令行加壳工具 help 信息**

```text
VirboxProtector_con <filename> [-c local|cloud] [-u username] [-p password] [-o output]
-c local|cloud|auto //login specific types of sense control lock.
-u username //login cloud's username.
-p password //login cloud's password.
-o output //specific output filename.
-?
```

3、使用本地控制锁加壳

VirboxProtector\_con.exe 全路径 + 需要被保护的程序的全路径 -c local -o 输出文件的全路径。如图：

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/con_use_locak.PNG)

4、使用云控制锁加壳

VirboxProtector\_con.exe 全路径 + 需要被保护的程序的全路径 -c cloud -u 开发者名称 -p 开发者密码 -o 输出文件的全路径。 如图：

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/con_use_cloud.PNG)

**注意**：1、命令行工具会自动从被加壳工具下面查找 XXX.exe.ssp 工程配置文件（该配置文件是 Virbox Protector 界面工具生成得到的）；2、如果路径中存在空格需要将路径使用双引号\("路径"\)括起来。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/con_project_file.PNG)

### 如何生成 map文件 {#如何生成map文件}

1、生成 BCB 程序 map，工程设置如下图

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/bcb_create_map_1.png)

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/bcb_create_map_2.png)

2、生成 vc 程序 map，工程设置如下图

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/vc_create_map_1.png)

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/vc_create_map_2.png)

3、生成 VS 程序 map，工程设置如下图

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/vs_create_map_1.png)

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/vs_create_map_2.png)

4、生成 Delphi 程序的 map，工程设置如下图

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/delphi_1.png)

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/delphi_2.png)

5、生成 VB6.0 程序的 map

在系统环境变量中增加一个名为“LINK”，值为"/MAP"项目,重新启动电脑，这样编译生成 exe 程序，map 文件就不会自动删除，而得以保留。

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/vb6_1.PNG)

## Linux 程序加壳保护 {#linux程序加壳保护}

1、解压 sdk 开发包，例如：senseshield-sdk-2.2.0.28909.tar.gz，解压该压缩包。

2、将解压后文件中的 lib 目录下面的 libslm\_runtime.so 和 libss\_user\_login.so 两个文件拷贝到加壳工具文件目录的 bin 目录下，并把这两个文件名称修改为 slm\_runtime\_linux32.so 和 ss\_user\_login\_linux32.so

3、将解压后文件中的 lib64 目录下面的 libslm\_runtime.so 和 libss\_user\_login.so 两个文件拷贝到加壳工具文件目录的 bin 目录下，并把这两个文件名称修改为 slm\_runtime\_linux64.so 和 ss\_user\_login\_linux64.so

文件结构如图所示

![linux&#x5F00;&#x53D1;&#x5E93;](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/linux_bin_dir.PNG)

3、将 linux上的被加壳程序，拷贝到 windows 中进行加壳，加壳方法同 windows 程序，然后将加壳后的程序拷贝到 linux 上运行

## Mac 程序加壳保护 {#mac程序加壳保护}

1、解压 sdk 开发包，例如：senseshield-sdk-2.2.0.28909-mac.tar.gz，解压该压缩包。

2、将解压后文件中的 lib64 目录下面的 libslm\_runtime.dylib 和 libss\_user\_login.dylib 两个文件拷贝到加壳工具文件目录的 bin 目录下，并把这两个文件名称修改为 slm\_runtime\_linux64.dylib 和 ss\_user\_login\_linux64.dylib

文件结构如图所示

![mac&#x5F00;&#x53D1;&#x5E93;](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/mac_bin_dir.PNG)

3、将 mac 上的被加壳程序，拷贝到 windows 中进行加壳，加壳方法同 windows 程序，然后将加壳后的程序拷贝到 mac 上运行

## 其它类型程序的加壳保护 {#其它类型程序的加壳保护}

### 加密的原理 {#加密的原理}

* 用加壳工具给执行的 exe 加壳，这个过程会将会将您设置的密码和解密插件注入到 exe 中。
* 用 DSProtector.exe 选择\*.ssp \(由加壳工具生成,里面存有秘钥\),然后选择要加密的数据文件,点击"保护它"按钮就可以了。步骤如下
* 执行加壳 ,勾选 插件-&gt;ds ，设置密码，就会用这个密码给你的数据文件加密

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds1.jpg)

* 选择 ssp 文件

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds2.jpg)

* 选择之后

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds2.jpg)

* 添加资源文件

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds3.jpg)

* 选择要保护的资源

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds4.jpg)

* 点击 "保护它",自动将原文件替换为加密文件；原文件被改名为 {xxxx}.bak ,xxxx 是你选择的文件名字

![](https://github.com/virboxzhou/virbox/tree/d12a4b0aefdf309f6422c723bf65ac059fb84ea4/assets/ds5.jpg)

### 如何使用 DSProtector.exe 程序进行资源保护 {#如何使用dsprotectorexe程序进行资源保护}

加壳工具对绝大部分的软件的二进制代码能够提供非常优质的保护，而对于软件使用的资源，我们提供了 DSProtector.exe 资源保护工具进行保护，目前资源保护工具（DSProtector.exe）支持的范围包括（已测试）

| 序号 | 软件名称 | 类型 | 支持or不支持 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| 1 | python | 语言类 | Y | 对pyc支持，对.py程序源码不支持 |
| 2 | lua | 语言类 | Y |  |
| 3 | perl | 语言类 | Y |  |
| 4 | erlang | 语言类 | N |  |
| 5 | ruby | 语言类 | Y | 命令执行脚本支持，web端不支持 |
| 6 | go | 语言类 | N |  |
| 7 | php | 语言类 | Y |  |
| 8 | R | 语言类 | Y |  |
| 9 | Unity游戏 | 游戏类 | Y | 对dll、res、resources、unity3d文件支持 |
| 10 | UE4 | 游戏类 | 部分支持 |  |
| 11 | Potplayer | 播放软件 | Y | Mp4、mkv |
| 12 | 暴风影音（安装版） | 播放软件 | Y | Mp4、mkv |
| 13 | 暴风影音（绿色版） | 播放软件 | N |  |
| 14 | jar、war web or 客户端 | 开发环境 | Y |  |
| 15 | 2345看图王\(安装版\) | 图片类 | Y | jpg、jpeg、png、bmp、gif支持 |
| 16 | foxitreader\_cnlv（绿色版） | pdf文档阅读器 | Y |  |

