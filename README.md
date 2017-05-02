
#Phabricator使用说明

##基本功能


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





