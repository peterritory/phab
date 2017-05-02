
#Phabricator使用说明

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





