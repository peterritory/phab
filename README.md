
# Phabricator使用说明

## 概述

Phabricator(以下可以称为Phab)是[Phacility公司](https://www.phacility.com/)的专门用于工程项目管理的综合产品，产品中包含的应用功能非常丰富，其有力竞品即Atlassian公司的对应产品。

## 对比

Phabricator与Github以及Atlassian公司产品的对比表格如下（来源<https://rekinyz.wordpress.com/2015/01/18/phabricator/>）：

| 应用/特性       | Phabricator  | Github |  Atlassian| 
|:------------- |:-------------| :-------------| :-------------|
| 提交前代码审查| Yes ([Differential](https://www.phacility.com/phabricator/differential/))|Partial (Pull Request|Yes (Crucible)|
| 提交后代码审查 | Yes ([Audit]())|	Basic |Yes (Crucible)|
|基于规则代码审查| Yes ([Herald](https://www.phacility.com/phabricator/herald/))|	No|No|
|集成事件跟踪|Yes ([Maniphest](https://www.phacility.com/phabricator/maniphest/))|Yes (Issues)|Yes (JIRA)|
|组织与项目管理|Yes ([Projects](https://www.phacility.com/phabricator/projects/))|Yes	|Yes|
|代码浏览查看|Yes([Diffusion](https://www.phacility.com/phabricator/diffusion/))|Yes|Yes (FishEye)|
|文档管理|Yes ([Phriction](https://www.phacility.com/phabricator/phriction/))|Yes|Yes (Confluence)|
|设计审查|Yes([Pholio](https://www.phacility.com/phabricator/pholio/))|No|No|
|团队沟通|Yes([Conpherence](https://www.phacility.com/phabricator/conpherence/))|No|Yes(Hipchat)|
|持续集成|Basic(Harbomaster)|第三方|Yes(Bamboo)|
|可视化任务管理|Yes([Workboards](https://www.phacility.com/phabricator/projects/))|第三方|Yes(JIRA Agile)|
|命令行工具|支持大部分应用([Arcanist](https://www.phacility.com/phabricator/arcanist/))|桌面应用和第三方工具|某些应用|
|API支持|Yes([Conduit](https://secure.phabricator.com/conduit/))|Some Application|Some Application|
|移动端/平板设备支持|Yes|Yes|支持某些应用|
|多合一开箱即用|Yes|Yes|No|
|富文本条目格式|Yes (Remarkup)|Yes (Markdown)|Yes (Markup)|
|付费第三方托管|Yes|Yes|Yes|
|本地私有安装|Yes|Yes(企业版)|Yes|
|开放源代码|Yes (Open, Apache 2.0)|No|Yes(Closed,Enterprise License)|
| 代码托管 | SVN, Git, Mercurial|SVN, Git|Git, Mercurial|
|访问管理|Yes|Yes|Yes|


## 使用基本逻辑

Phabricator本质上是开发与项目管理软件，大部分与开发和项目管理相关的功能都集成在了Phab的各种Application中。

对于普通项目（相对于代码项目而言），可以通过Projects应用逐步描述项目的基本属性，
对于代码项目，首先就可以使用Diffusion开启git代码仓库（Repository），通过通过给定的*.git的URL路径（例如：ssh://test-fiw332m2cmuj@vault.phacility.com/source/sor.git）与本地客户端交互。




## 基本功能

1. 菜单定制功能。Phabricator的左边菜单默认情况下，最低端有Edit Menu选项，点开之后，发现现有的左边菜单都是根据右边的若干个分类逐步添加管理的，默认情况下，没有博客编辑系统Pham（Phabricator中的博客工具），可以通过操作逐步添加Pham实现博客系统的定制，首先Pham是一款Application，那么在右边的Add New Menu Item下选择Application，之后在Application中填写Pham，此时会自动出现可以选择的候选，其中就出现了Pham，之后命名为Pham(Blog)作为菜单的显示名，点击保存后即可添加全新的Pham(Blog)作为Pham的这一个Phabricator的Application的链接。
2. 


## 详细使用步骤


### 代码版本管理（Diffusion + git）


1. 新建Repository，选择git作为版本控制工具，给项目取名并初始化；
2. 激活（Active）Repository；
3. 初次使用需要新建ssh-key，将其中的id_rsa.pub内容通过Upload Pubic Key操作提交到Phabricator的Settings/SSH Public Keys中；
4. 新建的Repo会生成一个自动的Phabricator的repo，例如：ssh://test-fiw332m2cmuj@vault.phacility.com/source/sor.git，此时可以通过客户端的git命令，将代码拉下来：

```
git clone ssh://test-fiw332m2cmuj@vault.phacility.com/source/sor.git
```

5. 在操作的文件夹中即可看到sor作为代码编辑更新目录。


### 提交前代码审查

1. Arcanist是Phabricator下的命令行工具，Phabricator基本上所有的功能，Arcanist都可以触发并使用。提交前代码审查最为方便的实现方式还是使用arcanist完成。代码提交前审查的必要性，为什么要做代码提交前审查？有如下几个理性的原因：

  - 顾忌监督的力量：如果执行代码提交前审查，写代码的人就会在写代码的时候时刻提醒自己注意：“我的代码是会有人认真看的，所以我必须对我的代码负责，三思再提交”；
  - 结对编程的需要：高质量的代码包含着可以维护性的概念，每一个提交至少需要掌握在两个人手里，才会让代码具有较强的生命力，一个人维护一份代码会让这个人的不可替代性加强导致组织对于这一单一人员的依赖性过强；
  - 代码变更跟踪变动的需要；

2. 



### 项目管理功能

项目计划
计划开始时间
计划持续时间
负责人
工作量
工作任务
工作记录
任务交付
交付物审批
交付物发布
工作量统计
成本核算










