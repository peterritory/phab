
#Phabricator使用说明
Phabricator(以下可以成为Phabricator)是[Phacility公司](https://www.phacility.com/)的专门用于工程项目管理的综合产品，产品中包含的应用功能非常丰富，其有力竞品即Atlassian公司的各类产品，Phabricator与Atlassian公司产品的对比表格如下（来源<https://rekinyz.wordpress.com/2015/01/18/phabricator/>）：

| 比较项目       | Phabricator  | Github |  Atlassian| 
|:------------- |:-------------| :-------------| :-------------|
| 代码托管 | SVN, Git, Mercurial|SVN, Git|Git, Mercurial
| 提交前代码审查| Yes (Differential)|Partial (Pull Request|Yes (Crucible)|
| 提交后代码审查 | Yes (Audit)|	Basic |Yes (Crucible)|
|基于规则代码审查| Yes (Herald)|	No|No|
|集成事件跟踪|Yes (Maniphest)|Yes (Issues)|Yes (JIRA)|
|组织与项目管理|Yes (Projects)|Yes	|Yes|
|访问管理|Yes|Yes|Yes|
|代码浏览查看|Yes(Diffusion)|Yes|Yes (FishEye)|
|文档管理|Yes (Phriction)|Yes|Yes (Confluence)|
|设计审查|Yes(Pholio)|No|No|




##功能简介
1. 

##基本功能

1. 菜单定制功能。Phabricator的左边菜单默认情况下，最低端有Edit Menu选项，点开之后，发现现有的左边菜单都是根据右边的若干个分类逐步添加管理的，默认情况下，没有博客编辑系统Pham（Phabricator中的博客工具），可以通过操作逐步添加Pham实现博客系统的定制，首先Pham是一款Application，那么在右边的Add New Menu Item下选择Application，之后在Application中填写Pham，此时会自动出现可以选择的候选，其中就出现了Pham，之后命名为Pham(Blog)作为菜单的显示名，点击保存后即可添加全新的Pham(Blog)作为Pham的这一个Phabricator的Application的链接。
2. 

##详细使用步骤

###代码版本管理（Diffusion + git）

1. 新建Repository，选择git作为版本控制工具，给项目取名并初始化；
2. 激活（Active）Repository；
3. 初次使用需要新建ssh-key，将其中的id_rsa.pub内容通过Upload Pubic Key操作提交到Phabricator的Settings/SSH Public Keys中；
4. 新建的Repo会生成一个自动的Phabricator的repo，例如：ssh://test-fiw332m2cmuj@vault.phacility.com/source/sor.git，此时可以通过客户端的git命令，将代码拉下来：

```
git clone ssh://test-fiw332m2cmuj@vault.phacility.com/source/sor.git
```

5. 在操作的文件夹中即可看到sor作为代码编辑更新目录。





