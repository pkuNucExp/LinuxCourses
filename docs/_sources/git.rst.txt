.. git.rst --- 
.. 
.. Description: 
.. Author: Hongyi Wu(吴鸿毅)
.. Email: wuhongyi@qq.com 
.. Created: 四 8月 13 20:21:20 2020 (+0800)
.. Last-Updated: 五 8月 14 21:40:37 2020 (+0800)
..           By: Hongyi Wu(吴鸿毅)
..     Update #: 4
.. URL: http://wuhongyi.cn 

##################################################
git 与 GitHub
##################################################


============================================================
git 的使用
============================================================

LINUX 下配置文件位置

.. code:: txt
	  
   ~/.gitconfig


**初始化配置**
   
.. code:: bash

   #配置使用git仓库的人员姓名
   git config --global user.name <youname>
    
   #配置使用git仓库的人员email
   git config --global user.email <youemail>
    
   #让Git显示颜色
   git config --global color.ui true
    
   #设置编辑器
   git config --global core.editor emacs
    
   #别名
   git config --global alias.co checkout
   git config --global alias.ci commit
   git config --global alias.st status
   git config --global alias.br branch






   

。。。


**git 提交空目录**

需要在目录下创建 .gitkeep 文件，然后在项目的 .gitignore 中设置不忽略 .gitkeep。

.gitkeep 是一个约定俗成的文件名并不会带有特殊规则。




============================================================
GitHub 帐号配置
============================================================

。。。



**创建仓库**

首先先上网站点击新建一个仓库，例如我要新建一个名为“test”的仓库，输入仓库名字，点击创建即可创建，然后就进入快速设置引导界面。如果你选择了 Initialize this repository with a README、Add .gitignore、Add a license，则会在仓库中生成相应的 README 、.gitignore 、 LICENSE 文件，跳过快速指导页面直接进入项目。如果选了以上，第一次上传之前还需要 pull 一下。

创建项目之后会进入一个快速设置指导页面。上面提示 HTTPS、SSH 两种方式可以上传、下载。如下所示。

.. code:: bash

   # HTTPS
   https://github.com/wuhongyi/test.git
   # SSH
   git@github.com:wuhongyi/test.git

如果说本地本人使用两个没什么差别，SSH 可能还方便点。但是如果远程电脑或者公共服务器账户上还是 HTTPS 好，远程 SSH 输入密码框无法显示，意味着没法上传。SSH 可以配置免密上传，公共服务器上还会泄漏账户信息或者被人误操作。综合以上建议采用 HTTPS 方式上传。

本地对应仓库的创建：

终端指向该文件夹执行以下命令初始化仓库（每个仓库只需要一次）

.. code:: bash

   #初始化 该目录下将生成. git 文件夹
   git init
   #设置远程仓库地址 第一个为 HTTPS 第二个为 SSH，两个选一个即可。
   #设置完之后该信息将被写入到 .git/config 文件中，可修改该文件切换上传方式
   git remote add origin https://github.com/wuhongyi/test.git
   git remote add origin git@github.com:wuhongyi/test.git
	  
仓库内容的修改和发布：

.. code:: bash
   
   git add [XXX]    #添加文件到暂存区
   git commit -m "commit message"    #提交修改
   git push -u origin master    #上传到网站

项目下创建文件 .gitignore，在里面添加需要忽略的文件夹及文件

.. code:: txt

   /projectNCURSES/build/
   /projectROOT/build/
   /SimulationPMT/build/
   /projectG4/build/
   /projectWU/build/
   /projectWU/bin/
   /projectG4MT/build/
   /projectG4MTNeutron/build/
   /projectG4MTPhoton/build/
   /GammaSpectroscopy/build/
   /GammaSpectroscopy/source/build/
   /projectG4Visualization/build/
   *.root
   *.m4b
   *.mca
   *.spe
   /G4_lib/
   /lib/
   Authorize/Log/   

其中目录以 “/” 开头的为绝对路径，如前几个。不以 “/” 开头的将会忽略整个仓库中该名字的文件夹，例如最后一个。文件也同理，不指定目录将忽略所有匹配的文件。

   

**github 创建个人主页**

每个用户下只能有一个 [username].github.io 的仓库

发布在该仓库的 master 分支的内容即个人静态网页， 可通过 [username].github.io 访问。


============================================================
GitHub 客户端
============================================================

。。。






   
.. 
.. git.rst ends here
