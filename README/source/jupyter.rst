.. jupyter.rst --- 
.. 
.. Description: 
.. Author: Hongyi Wu(吴鸿毅)
.. Email: wuhongyi@qq.com 
.. Created: 二 9月  8 21:17:48 2020 (+0800)
.. Last-Updated: 五 9月 25 19:28:13 2020 (+0800)
..           By: Hongyi Wu(吴鸿毅)
..     Update #: 6
.. URL: http://wuhongyi.cn 

##################################################
jupyter
##################################################

============================================================
环境配置
============================================================

下载配置文件 http://gofile.me/42AHM/jdVBx7GMs

复制参考配置文件 *jupyter_notebook_config.py* 到个人的某个文件夹。该文件夹为您 jupyter 的根目录。

.. code-block:: bash
		
  #将 8888 改成您的端口号
  c.NotebookApp.port = 8888

如果需要设置访问密码

.. code-block:: bash
		
  #设置访问密码 本设置的密码为 wuhongyi ，需要修改成您自己的密码
  c.NotebookApp.password = u'sha1:b4312c4fb8b5:e239f220fa9fc697668ec3dc71b4180ee8854dac'


.. image:: /_static/img/jupyter_config.png
  
如果没有设置密码（将该行设置注释掉），那么在访问网页的时候，会要求输入 token ，token 在终端的输出信息中有。

建议配置个人密码，方便访问。生成密码的方式如下：

打开ipython, 创建一个密文密码

.. code-block:: bash
		
  In [1]: from notebook.auth import passwd
   
  In [2]: passwd()
  Enter password: 
  Verify password: 
  Out[2]: 'sha1:ecff44b879cd:35b5b64072d286b66f0d8f84a41dbf7515d21755'

把生成的密文 *sha1:ec…* 复制下来替换成以上配置文件中的密码。

.. image:: /_static/img/jupyter_ipython.png

完成以上配置之后，即可启动 jupyter。将终端进入到放置 *jupyter_notebook_config.py* 文件的目录。然后执行以下命令：


.. code-block:: bash

  root --notebook

之后，您可在任意电脑中通过 *127.0.0.1:8888* 来本地访问。（其中 8888 替换成您的端口号）


============================================================
示例程序
============================================================

这里演示使用示例。


   
.. 
.. jupyter.rst ends here
