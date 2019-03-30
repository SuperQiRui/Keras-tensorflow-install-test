# Keras-test
本项目为个人学习记录


 # Step1 安装Anaconda
首先安装 Anaconda 然后打开 Anaconda prompt
原地址下载太慢，要添加清华镜像，加快下载速度

 conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
 
 conda config --set show_channel_urls yes

官网提供的只有python 3.7版本，而keras目前（2019.3.30）只支持最新到3.6版本，所以需要新建一个虚拟环境

conda create -n py36 python=3.6

activate py36 #（linux下+source， windows下无需+source）

# Step2 安装tensorflow-gpu 和 keras-gpu 
通过Anaconda安装极大的方便初学者学习。

在Anaconda prompt输入

conda install tensorflow-gpu

conda install keras-gpu

# Step3 安装vscode 或者 pycharm 

vscode 需要在设置中输入Anaconda虚拟环境的python地址
 
pycharm在create project 时选择已存在的Anaconda环境

上述两部可自行搜索参考

ps:我的vscode在import keras 时会返回不存在该modeul,而在终端中又能正确导入。

但是实际上tensorflow里面有keras  

可直接通过

from tensorflow import keras 导入keras 

（所以理论上应该不需要另外安装keras，只安装tensorflow-gpu 即可）

# Step4  验证是tensorflow-gpu是否正确安装
官方链接 https://www.tensorflow.org/guide/using_gpu?hl=zh_cn
在python中运行

import tensorflow as tf

#Creates a graph.

a = tf.constant([1.0, 2.0, 3.0, 4.0, 5.0, 6.0], shape=[2, 3], name='a')

b = tf.constant([1.0, 2.0, 3.0, 4.0, 5.0, 6.0], shape=[3, 2], name='b')

c = tf.matmul(a, b)

#Creates a session with log_device_placement set to True.

sess = tf.Session(config=tf.ConfigProto(log_device_placement=True))

#Runs the op.

print(sess.run(c))

可通过返回的信息确定是否是启用了gpu

# Step5 跑   Keras-test /helloWorld.py 中的文件测试

进一步学习、理解该代码可访问

https://blog.csdn.net/HHTNAN/article/details/80403146

https://keras-cn.readthedocs.io/en/latest/

https://blog.csdn.net/HHTNAN/article/details/82588372
		
      
      



