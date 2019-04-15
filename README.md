# BNUSSS Toolkit

*这里是BNUSSS工具箱，这个工具箱存在的意义是为我们更好的实践科研范式提供一套工具。*


# 目录

<a href="#t1">梳理科研项目的思维链条：Xmind8</a>
<a href="#t2">实验协作文档/流程管理：石墨文档</a>
<a href="#t3">代码管理工具：Gitlab / Github</a>
<a href="#t4">建立你的个人网站：mobirise.co / html5up.net</a>
<a href="#t5">板项目管理工具：tower / trollow</a>
<a href="#t6">使用Anaconda</a>
<a href="#t7">使用conda管理环境</a>

## 梳理科研项目的思维链条：Xmind8 
<div id="t1"></div>

在我们做科研项目的时候，一个非常重要的点是（至少第一作者）必须要对自己的科研项目的整个思维链条非常熟悉。这包括，至少可以流畅的回答以下问题：

- 我的工作的实际背景是什么
- 实际意义是什么（小综述）
- 以往，前辈们在这个问题上有哪些进展
- 我的工作具体解决的科学问题是什么
- 解决问题的思路是什么
- 支撑我的工作，需要哪些背景知识
- 算法框架是什么
- 算法的各个模块是怎样工作的
- 未来有哪些方向

针对科研的实验设计，也应该清晰的了解

- 实验的对比模型是什么，为什么选择这个对比模型
- 应该设计哪些实验，目的是什么
- 实验的执行方法是什么
- 实验的结论是什么
- 实验结果反映了我的方法有怎样的特点，有怎样的不足

可以看到，要回答上述问题，需要对大量的想法、数据和结论进行整理，因此我们有必要选取一个记录整个逻辑思维链条各个环节的工具。xmind8 https://www.xmind.cn/xmind8-pro/ 是一个免费的思维导图软件，既可以用于记录新的想法、进展，也便于整理老的想法，从宏观的角度审视自己的工作。

例如（一个未展开的导图）：

<img src="./img/xmind.png" width="800px" alt="xmind">

详细展开版(内部同学可见)请见： http://210.31.72.204/f/489


## 实验协作文档/流程管理：石墨文档
<div id="t2"></div>

要发好的期刊，工作量都是非常大的，因此记录我们工作的阶段性结论就很重要。<br>
石墨文档是一个在线多人协作文档（https://shimo.im）<br>
针对实验流程的管理，尤其是涉及到多人协作的时候，我们可以整理如下表格<br>
每天大家可以把今日工作结果用两句话整理到石墨文档上（只记录重要结论，无需记录细节），也可以开会后定某件事情的DDL写在文档上。<br>

例如（一个示例管理表格）：

<img src="./img/shimo.png" width="500px" alt="xmind">


## 代码管理工具：Gitlab / Github
<div id="t3"></div>

感谢集智学园程序组友情协助<br>
git的使用已经成为了一项基本技能，相信大家都有必要学会熟练的使用git <br>
科研项目的代码量并不多，协作要求不高，但每个版本都十分重要，因此我们可以着重使用gitlab的

- 代码版本打tag功能
- code review功能
- 快速同步功能

## 建立你的个人网站：mobirise.co / html5up.net
<div id="t4"></div>

建立你的个人网站可以方便的向他人展示你自己<br>
Git Pages(https://pages.github.com) 是一个方便、免费、广受认可的静态网站托管平台，可以为我们所使用<br>
<br>

以下是简单的例子<br>

https://lingfeiwu.github.io/ <br>

以下是一些方便且美观的建站工具<br>
https://mobirise.co <br> 
https://html5up.net


## 看板项目管理工具：tower / trollow
<div id="t5"></div>

看板式项目管理是一种清晰，简洁的项目管理方式 <br>
具体而言，我们可以将任务分为 wish list / to do / doing / done / trash 这五类 <br>
因为一个科研项目往往需要关注很多因素， 看板式的项目管理可以帮助我们梳理那些事情正处于哪些状态 <br>
一个健康的任务会从todo 跑到 doing 再跑到 done <br>
当然，如果我们发现这个任务没有必要，可以把它扔到trash里面 <br>
一些奇奇怪怪的想法也可以记录到 wish list里面 <br>
一个典型的看板项目如下：

<img src="./img/board.png" alt="">

tower（https://tower.im）和 trollow （https://trello.com） 是两个免费的支持看板任务管理的web软件，值得一试


## 使用Anaconda
<div id="t6"></div>

Anaconda的下载，前往https://mirrors.tuna.tsinghua.edu.cn <br>
安装过程中，添加环境变量记得选yes。<br>
安装完成后，在命令行输入which python，显示的应该是 <br>

<img src="./img/anaconda.png" alt=""> <br>

这就说明你现在用的python是你目录下anaconda文件夹里的python，而不是系统默认的python。<br>

#### 手动添加环境变量：
vim ~/.bashrc 然后添加 <br> 
export PATH="/home/liujing/anaconda3/bin:$PATH" <br>
保存退出，再 source ~/.bashrc即可 <br>
<br>
安装完成后，可以修改镜像源。参考https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/
不然装包会很慢的。


## 使用conda管理环境
<div id="t7"></div>

##### 创建一个名为torch03的环境
```
conda create -n torch03 python=3.6 numpy scipy matplotlib jupyter notebook
```

##### 激活虚拟环境

```
conda activate torch03
```


#### 在虚拟环境中安装包
```
conda install pytorch=0.3 
```

#### 退出虚拟环境
```
conda deactivate
```

#### 删除虚拟环境

```
conda remove -n torch03 package/ --all
```

#### 查看虚拟环境列表

```
conda env list
```

#### 复制虚拟环境
复制功能常用作环境备份：为了避免环境崩溃，在对环境进行操作（如安装某个包）之前，进行环境备份是一个好习惯 <br>
否则，如果环境崩溃了，只能重头装，当环境很复杂的时候，这个过程是非常麻烦的
```
conda create -n env_backup_name --clone env_name
```

<br>
<hr>
<font size=2>如果你还有其他好用的工具，欢迎联系3riccczz@gmail.com（张章）</font>
<br>
<font size=2>Tools may help, but don't be trapped.</font>



