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
## zanata

#### 简介

Zanata是一个基于网络的系统，供翻译人员使用网络浏览器在线翻译文档和软件。zanata使用Java编写，利用了现代Web技术，如JBoss EAP，CDI，GWT，Hibernate和REST API。 它目前支持通过PO文件和许多其他格式翻译DocBook / Publican文档。可以使用Maven插件或命令行客户端将项目上传到Zanata服务器并从Zanata服务器下载。

（Docbook：是一种用于技术文件的语义标记语言。它本来是设计来编写有关计算机硬件和软件的技术文件，但它可以用于任何其它类型的文件。).

**对于开发者和写作者**: 使用zanata,可以打开项目进行翻译，而无需在版本控制中打开整个项目。它是一个集成工具，提供集中的本地化存储库以及节省时间和资源的翻译工具。

**对于翻译者**：无需使用po文件，下载文档或版本控制软件。只需登录网页，加入语言团队开始翻译，可以使用翻译记忆，可以随时看到其他译者的更新。它是一个基于Web浏览器的翻译环境，以前的翻译为他们的工作提供了背景。

Zanata是一个用Java编写的开源翻译平台，提供翻译记忆库，在线翻译编辑器以及与REST API和命令行工具的工作流程集成。

来源： https://opensource.com/life/12/11/zanata-new-open-source-translation-platform

#### 设计背景

由于Red hat长期参与开源软件翻译社区。在red hat内部用于将软件产品翻译成多种不同语言。

Redhat：是一家开源解决方案供应商。开源领导者。实践证明，开源是一种有利于实现技术创新的协作过程。开源意味着可以自由地查看代码、探索学习、提问以及提供改进方案。开源社区汇集了成千上万名贡献者，正是他们智慧的凝聚，才迸发出了最佳创意。

“如果我们能为最佳创意提供萌发的土壤，多方共赢就不再遥远。”

来源：https://www.redhat.com/zh

#### 设计动机

提供一个具有丰富功能的统一翻译平台，并消除了必须学习其他工具的麻烦。技术翻译由于涉及新的内容和技术，可能需要翻译人员进行大量研究。 在这些情况下，翻译人员通常不喜欢注意力被工具所分散。

适用对象：开源文档和软件项目的编写者，翻译者和开发者

#### 技术特点

对于文档，zanata通过Publican的Gettext支持DocBook项目，对于软件，zanata原生支持Gettext和Java Properties文件。zanata还通过Okapi项目对OpenOffice / LibreOffice ODF文件进行了实验性支持。任何可以将其资源转换为Gettext或Properties并与Zanata集成的项目。如果将文本保存在数据库中，则可以绕过文件并直接与zanata的REST API交谈。

它基于Seam，Hibernate和JBoss Enterprise Web Platform等开源技术，并具有开放式API，允许应用程序和工具开发人员编写自己的集成。

随着更多的使用，zanata会得到非常频繁的反馈，了解哪些是有效的，哪些是无效的以及需要改进的是什么。所有这些反馈都记录在公共错误跟踪系统上，这有助于zanata管理人员和对项目感兴趣的其他人跟踪事情。

Zanata旨在集成到内容工作流程中，提供自动命令，可以将可翻译文本推送到Zanata或从Zanata中提取。 这意味着翻译人员不必担心像git和SVN这样的源控制系统，他们可以继续在Zanata的翻译编辑器中进行翻译。

编辑器提供集成的翻译记忆库（查看翻译时的类似翻译），翻译统计的即时反馈以及其他用户输入的翻译。 还有许多工具可以轻松地自动重复使用翻译记忆库中的翻译（TM merge，CopyTrans）

zanata致力于更广泛的社区联系，并为希望引入他们的想法并开展工作的新贡献者建立一个生态系统。

来源：2012  opensource.com

#### zanata 的一些优势（对比gitnub）

**github**

每一个新用户需要建立一个文件夹，里面内容冗杂。反斜杠之类容易误删除，导致整个功能受到影响

翻译内容校正不方便，不支持多种语言翻译

需要一定的技术背景

**zanata**

流畅、效率高

<https://www.youtube.com/watch?v=zTaIg_jGQVc>

zanata不用下载任何工具  通过python上传和下载翻译文档

<https://www.youtube.com/watch?v=ZxqrTkT2XOI>

除了翻译作用外,还可以给开发者管理本地项目文件

**翻译管理项目相关：**

在公开场合完成本地化是最有效和最有效的。Zanata的这些工具应该使用户及其社区能够将项目本地化为尽可能多的语言。

TMS工具是基于Web的平台，允许用户管理本地化项目，并使翻译人员和审阅人员能够执行他们最擅长的工作。大多数TMS工具旨在通过包括版本控制系统（VCS）集成，云服务集成，项目报告以及标准翻译记忆和术语回忆功能来自动化本地化过程的许多手动部分。这些工具最适合社区本地化或翻译项目，因为它们允许大量翻译和审阅者为项目做出贡献。有些人还使用WYSIWYG编辑器为翻译提供翻译上下文。 这种增加的上下文提高了翻译的准确性，并减少了翻译人员在翻译和审查用户界面内的翻译之间必须等待的时间。

<https://opensource.com/article/17/6/open-source-localization-tools>

#### 知名项目

Fedora 本地化工作.(与zanata都是red hat Inc.)

**Fedora**：Fedora 是一个Linux发行版，是一款由全球社区爱好者构建的面向日常应用的快速、稳定、强大的操作系统。它允许任何人自由地使用、修改和重发布，无论现在还是将来。它由一个强大的社群开发，这个社群的成员以自己的不懈努力，提供并维护自由、开放源码的软件和开放的标准。

译者可以随时加入Fedora的本地化工作，选择自己喜欢的项目进行贡献。  

**FUEL project术语模块的贡献**

FUEL是一项开源工作，旨在解决计算机软件本地化不一致和缺乏标准化的问题。为翻译语言的计算机用户提供标准和一致的指导。 FUEL致力于创建语言和技术资源，如标准化术语资源，计算机翻译风格和会议指南以及评估方法。此项目是在zanata平台上进行的。
#### 特点：

使用Zanata翻译平台的好处之一是，它能够从永久链接中提取翻译，用户可以使用少量命令将其安装到自己的系统上。

来源 <https://fedoraproject.org/wiki/L10N/Translate_on_Zanata/zh-cn#Fedora_.E6.9C.AC.E5.9C.B0.E5.8C.96.E5.B7.A5.E4.BD.9C.E6.8C.87.E5.8D.97.EF.BC.88.E6.96.B0.E7.9A.84.EF.BC.89>

它基于Seam，Hibernate和JBoss Enterprise Web Platform等开源技术，并具有开放式API，允许应用程序和工具开发人员编写自己的集成。

zanata最酷的地方：主要功能由用户决定 。作为一个开源的翻译平台，用户可以自行修改使其符合自己的要求。

zanata 的代码资源在github上：https://github.com/zanata

每个人都可以选择自己的语言对一个文档进行翻译。

#### 译员沟通：

论坛等。如Fedora本地化项目在hyperkitty上。

游戏的本地化一般为翻译爱好者自发组织，将项目放在zanata上，译者之间在论坛相互交流

#### 项目管理

以Fedora的本地化为例

Fedora社区：只有三分之一是红帽员工，一个健康有序的社区，肯定是能够让所有人都参与进来的社区。

**组成：**Fedora 的理事会，它提供高层的指导，这些理事会成员是由社区内部选举产生的，理事会提供 Fedora 社区发展的方向；

在理事会之下，有各个不同的工作组，这些工作组有不同的关注点；

工程指导委员会，它会指导下一版发布中应该放哪些工程和技术方面的更新内容；

基础架构的工作组，负责内部的这些服务包括网站或者是其他一些涉及到内部服务的内容；

版本发布工程组及其他各种各样的工作组，他们都有各自的关注领域和关注点。

重要的一点就是这些工作组、委员会，这些机构，他们的会议是公开的，他们进行的讨论也是公开的，就是全世界都可以看到，因此，红帽不可能过度影响这样一个社区的运作，其他的竞争公司也没办法过度影响它的运作，因为全世界都在看着。无论红帽公司还是其他公司都没有办法在大家已经达成一致的时候跳出来反对。

社区回报：所有贡献者都能够从为开源社区所做的贡献中得到自己想要的东西，比如说有的贡献者有机会通过开源社区的贡献提升了自己在一个新的技术领域的技能，这个有可能能够促进他得到升职，或者是促进他得到新工作，而这种晋升或换工作可能是在红帽，也可能是在其他公司，对于另外一些个人的贡献者来说，他做的贡献可能就是解决了自己所面临的一个具体的问题，这样他就从中得到了获得感，得到了回报。

#### 工作流程

以**Hyperledger国际化工作组**为例

Hyperledger中国工作组(TWGC)下属的一个小组，主要负责相关文档的中文编写和翻译，以及组织讨论、教育培训活动等。

使用zanata进行国际化工作：

1. 注册用户并登陆

   注册新用户，并将的Zanata ID添加至项目组wiki页面

2. 申请加入Zanata中文团队

   通过`Launguage`->`Chinese (Simplified, China)`->`Request to Join`，申请加入Zanata中文翻译团队。通常这个申请只需要一两天就可以被通过。若两天后申请仍处于`pending`状态，请联系管理人员

3. 进入项目
4. 选择版本号

5. 选择语言 

6. 单击选择要翻译的文件

7. 在右侧编辑翻译

   在右侧输入译文，编辑完后会自动保存；下侧是翻译提示内容，可直接`copy`；也可以点击`使用新版`体验新版翻译页面。

   **注意：翻译中的固定术语尽量按照翻译提示统一命名，以免混乱！！！**

   **注意：翻译中的原文特有的格式符号（如---、====等）一定要保留！！！**


8. 译文显示

   **译文设置为20分钟自动编译更新一次**

9. 原文更新

   fabric官方源文档更新后，会有专人跟新Zanata上的原文。原文更新后，变化的地方如果被翻译过则译文会被删除掉，同时文档完成度会降低。

 Zanata + Github + Read the Docs

目前使用Jenkins实现了Zanata+github+Read the docs的集成。Jenkins20分钟自动编译一次



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



