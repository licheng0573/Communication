## （一）翻译项目中的沟通

### 1、XXX

### 2、XXX



## （二）翻译人员与技术人员的沟通

### 1、XXX

### 2、XXX



## （三）源语言和目标语言差异

### 1、XXX

### 2、XXX



## （四）翻译平台

### 1、腾讯



### 2、Zanata



### 3、Pootle

名称：基于**PO**的**O**nline **T**ranslation / **L**ocalization **E**ngine的首字母缩写

执照：GLP

#### 背景

- 2004	Translate.org.za开发和发布、免费**

  最早是由CATIA项目（非洲本地化网络）资助的项目中开发。

  使用[Django框架](https://en.wikipedia.org/wiki/Django_(web_framework))以[Python编程语言](https://en.wikipedia.org/wiki/Python_(programming_language))编写。

  **Catalysing Access to ICT in Africa**

  https://web.archive.org/web/20070117142810/http://www.catia.ws/

- **2006	作为WordForge项目进一步开发**



#### 设计理念

- 免费、鼓励项目托管自己的Pootle服务器以进行本地化。
- 使用Translate Toolkit的API和Django framework。作为翻译管理系统 ，把翻译文件视为文档进行管理。
- 能够同上游的版本控制系统交互，直接在项目内提交变更，而不是维护一个平行的系统。



**Notes：**

​	**PO文件：**

​	提取于源代码的一种资源文件，可使用Gettext获取。可以在一定程序上使翻译成果得到继承。

​	**Translate Toolkit：**

​	http://docs.translatehouse.org/projects/translate-toolkit/en/latest/features.html

​	目的是提高本地化和翻译质量。使用PO和XLIFF格式。

​	首先把文件转换为这两种基本格式。

​	其次提供工具来提取术语和检查术语一致性，能够检查各种技术错误，例如正确使用变量。

​	最后提供了一个功能强大的本地化API，可以作为其他工具的基础。



#### 使用Pootle的项目

##### **(1) OpenOffice.org**

https://en.wikipedia.org/wiki/OpenOffice.org#Apache_OpenOffice

OpenOffice是一个办公套件，2000年由Sun公司收购并发布商业版本，2011年Oracle公司将其捐赠给Apache软件基金会。

The Apache Software Foundation 使用了Pootle的服务，以简单、合作的方式完成产品的本地化工作。

OpenOffice 支持了120+种语言，目前有40+种是在Pootle上维护的，并且这个数量也正逐渐增加。

https://wiki.openoffice.org/wiki/Pootle_User_Guide

**Official Pootle Translate server used by ASF projects:**

![ASF Translate service](pic/ASFTranslateservice-1.jpg)



##### **(2) Verbatim**（**mozootle**）

https://wiki.mozilla.org/Verbatim

Verbatim是Mozilla的Pootle服务器的产品代号，也称为Mozootle。

Pootle的使用介绍（Mozilla Demo）

​	https://www.youtube.com/watch?reload=9&v=u6tDUQv3huU

​	translation

​	make a suggestion

​	review suggestion mode

​	checks



##### **(3) Sugar (software)**

Sugar是一个免费开源的桌面环境，为儿童的互动学习而设计。Sugar labs旗下开发。跨平台。

https://translate.sugarlabs.org/

![Sugar Labs translation platform-1](pic/SugarLabstranslationplatform-1.jpg)



#### Features

http://docs.translatehouse.org/projects/pootle/en/latest/features/index.html

##### 1、Pootle FS

- 可以与各种版本控制系统（VCS）集成。Pootle FS通过插件为不同的VCS系统提供支持。为VCS安装Pootle的插件，在VCS中为Pootle提供同步访问权限（SSH密钥）即可。

##### 2、Backends and storage

- 通过Translate Toolkit API支持多种文件格式。

- 提供翻译进展的统计信息。

- Translate Toolkit的pofilter提供的质量检查。

  http://docs.translatehouse.org/projects/translate-toolkit/en/latest/commands/pofilter.html#pofilter

##### 3、Online translation editor

- Alternative source language

  翻译时可以查看其他语言的翻译以消除歧义。用户可以在帐户设置中设置希望显示的语言。

  ![Features-其他语言](pic/Features-其他语言.jpg)

- Special characters

  对于各种语言中，键盘上不方便输入的字符，在编辑区提供选择。用户可以直接点击使用。

  ![1544798303333](pic/edit.png)

- Quality checks

  质量问题会明显地显示在页面上方。

  ![critical_errors](pic/critical_errors.png)

  对于重要错误，会显示在提交按钮前。用户需要修改或者Mute。

  ![failing-checks](pic/failing-checks.png)

- Translation Memory

  用户可以使用远程的/本地的/外部的翻译记忆库

- Machine Translation

  可以配置文件中启用机器翻译服务。

  支持：Google Translate 和 Yandex.Translate

- Searching in Pootle

  提供高级搜索，将搜索内容限定在特定字段，词组匹配，大小写限制等。

- Keyboard shortcuts

  提供键盘快捷键操作。

  ![shortcuts-edit](pic/shortcuts-edit.jpg)

  ![shortcuts-navi](pic/shortcuts-navi.jpg)

- Translation suggestions

  提出建议：有权提出建议的用户将看到“提交”旁边的“建议”按钮。

  查看建议：具有翻译权限的用户才可以查看建议。在翻译时可以查看建议，或者可以浏览所有建议。

  审核建议：批准或者拒绝建议。

- Terminology

- Offline Translation

  用户可以将待翻译的文本导出进行离线翻译。完成后再上传。

##### 4、Administrative features

- 管理团队成员：

  添加和删除成员，并设定其角色。不同角色具有不同权限。

  4种角色：Member、Submitter、Reviewer、Administrator

- 设置验证码

- 权限

  可为不同的用户组设定不同的权限。

  访问权限（对项目的访问）、动作权限（建议、审查、翻译、管理等）





#### **其他Pootle Servers**

http://translate.sourceforge.net/wiki/pootle/live_servers

​	Public Pootle Servers

​	Non-Public Pootle Servers





### 4、Translation5



#### 4.1 简介

​         translate5是由Marc Mittag在德国开发和维护的基于Web的开源翻译系统。

​	它的主要组成部分是一个完善的基于网络的翻译工作台。它支持可视化编辑，审阅，自动QA，后期编辑和质量评估。translate5没有自己的翻译记忆库，而是在后台依赖IBM的OpenTM2服务器。此外，还有一个在线管理套件，支持项目管理，工作流程，术语，用户和客户端。

​	该系统可由支持公司Mittag QI托管，或部署在用户自己的服务器上。

​	开源平台，系统核心代码和核心插件代码都遵守AGPL3许可证。用户免费使用和可以修改translate5，但是所有的修改代码必须公开发布。开发团队是MittagQI（一家德国翻译行业软件使用及翻译流程咨询公司）

#### 4.2 设计背景

​	translate5的开发者在平台网站上这样说：对于很多小型公司，或者大型公司的语言服务部门而言，在构建实际需要的流程并保持独立于语言行业的大型参与者的过程中，是与其他开发人员联合开发他们需要的软件的重要因素。

​	对于MT-研究人员来说，与商业中使用翻译软件的公司密切合作以及从事共同的软件开发是非常有帮助的。翻译专业人士则受益于翻译研究在开发和翻译过程中的投入。

​         这些需求的概念基础是基于开放源码的联合开发。

​         translate5项目会尽量与其他开源项目合作。作为web服务器环境，translate5作为许多不同工具(开源和私有)的基于api的集成中心，旨在帮助用户在一个简单上手的GUI中享受不同工具的组合能力。

​         开源软件是免费的，在“无成本使用”的意义上，但它的主要思想是“自由”。用户可以自由地对软件做他们想做的事情——集成它、扩展它、开发它——只要他们尊重开源许可。

在自由软件的意义上，translate5遵循了开源的概念。它的目标是服务和支持它的用户，并且以这种方式被它的用户所拥有，这样用户可以以他们想要和需要的任何方式影响和贡献开发。

​         这样的软件还有一个好处，为用户的工作提供了可靠性。他们不必要依赖于一个公司开发的软件，这样就算一个开发团队无法工作了，也可以找到其他人员来支持开发这个软件。

​	translate5的设计思路是将他们使用的软件的控制权交给用户。

#### 4.3 基本用法

​	添加任务支持压缩包，单个文件（tbx）。压缩包（zip）中必须包含proofRead目录， SDLXLIFF、openTM2 XLIFF和csv文件可以任意混合在proofRead文件夹中。Translate5支持导入4中双语文件格式，CSV，openTM2 XLIFF，SDLXLIFF，STAT Transit NXT language paris。

​         页面分为文件查看区，编辑区，工具区，片段信息显示区，翻译记忆区。

​         文件查看区包括工作文件和参考文件。工作文件中可以按照树结构分类查看文件。参考文件可以下载阅读。

​	编辑区中，可以选择编辑器模式，分为details，details(read only)，normal，normal(readonly)。其中details和normal的界面区别不大，仅是前者会将文件查看区展开，字体显示现对于后者变小一些。编辑区也设有翻译文件字号方大和缩小功能。设有reset grid功能，可以重新划分单元格，但划分过程是后台自动完成的。包含的列有Nr.，autostatus，Matchrate，Source text，Target text(at time of import)，Target text，comments，status，QM，Last editor。所有列都可以被过滤和排序，可以组合来自多个列的筛选器。对术语库，或翻译记忆库中有的内容进行不同颜色下划线标识。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\bianjiqu01.png)

![bianjiqu02](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\bianjiqu02.png)

![bianjiqu03](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\bianjiqu03.png)

![bianjiqu04](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\bianjiqu04.png)

​	片段内容显示区包括术语查询、译文评级评分。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\pianduanneirong.png)

​	工具区大致包含了确认，向上，向下，标注，退出操作等简单操作命令。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\toolarea.png)

​	翻译记忆区包括matches和concordance search，支持API调用机器翻译，采用Moses standard connector和Lucy LT connector。

通过快捷键ctrl+f/ctrl+h可以弹出查找与替换选项卡，支持通配符匹配和正则表达式。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\chazhao.png)

#### 4.4 特色功能

##### 4.4.1 翻译流程中的插件功能

- VisualReview: Review in perfect layout — for most file formats

- Inline MS-Word style Track Changes

- The integration of Translation Memory and MT systems

  上述插件都已经融入了整个平台之中。

​	用户还可以自己写插件。以插件的形式扩展功能有三个好处：保证系统稳定性，用户不需要修改系统核心代码；用户可以有自己的功能需求隐私；用户可以售卖开发的功能。系统核心代码由专门的代码开发团队维护。用户自己写的插件，可以在开源GPL3许可证和开源AGPL3许可证之间自由选择。GPL3允许用户在云服务器上运行软件，而无需将服务器端代码传递给云的用户。

​	有一些插件是需要付费的。例如读取多种文件格式的VisualReview插件，以及跟踪文章修改痕迹的Inline Ms-Word Style Track Changes插件等，这些插件都仅对支持了translate5开发的公司免费。

##### 4.4.2 译员沟通中的网站

​	创建了一个单独的网站（confluence.translate5.net），在这个网站上，用户和开发者都可以讨论发布信息。同时这也是一个技术文档的发布点，所有的使用信息都在这个网站上。不过这个网站暂时不是为了译员沟通而设置的，基本都是针对产品本身存在的问题等提出讨论或改进想法。但是译员作为用户可以在平台上反应自己的需求等，以便更好的改进产品。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\translate5website.png)

##### 4.4.3 知识管理中的文件参考

​	有参考文件功能，译员登录后下载参考文件可以了解翻译项目。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\cankao.png)

##### 4.4.4 质量控制中的账户类型控制

​	不同项目登录账户类型（manager，proofheader，editor，visitor，translator），如项目经理账户可以上传管理术语库，并决定可以使用的译员账户权限。

![](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\translate5manager.png)

![translate5proofhead](F:\桌面文件夹汇总\研究生课程\翻译技术原理与实践\讨论题\第四次\Communication\pic\translate5proofhead.png)