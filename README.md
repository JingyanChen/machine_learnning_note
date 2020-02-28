#**<center>机器学习，线性回归模型与梯度下降法笔记（一）</center>**

##1 前言

笔者通过 [吴恩达·机器学习公开课](https://study.163.com/course/courseLearn.htm?courseId=1004570029#/learn/video?lessonId=1049052745&courseId=1004570029"吴恩达·机器学习公开课")学习到了一些机器学习的基础知识，笔者希望通过这篇文章，分享一些学习思考。为了验证自己是否掌握了其核心的知识，会使用Python语言，克服一切困难，实现机器学习的理论算法在python上运行。

##2 对机器学习的粗浅理解

###2.1 语言定义上的理解
"A computer program is said to learn from experience E with respect to some task T and some performance measure P,if its performance on T , as measured by P,improves with experience E." from Tom Mitchell.

里面谈到机器学习的作用和特点。就是程序在做任务T的时候，因为有先前的经验E，所以性能P直线上升。

所以理解每一个机器学习问题，都应该从这三个方面去考虑。

从最简单的线性回归问题来看，预测新的、原本并没有被记录的新输入x对应的h(x)值，就是它需要去做的任务T。

之前输入确定且正确的数据集set就是经验E。

预测的准确性，给出的答案是否令人满意，就是代价函数(cost function)是否是最小就是性能P。

### 2.2 从图来看

<center>
![GitHub set up](http://a1.qpic.cn/psc?/V11YQ5uU0HzVFs/ENmuKd2PHQoigBx2P9ktWVzR2ogGF9FCV3trwPix6qH77x4wsZc00jgeWzRriinT6wJOolMU2sC7GkC3IBM49Q!!/c&ek=1&kp=1&pt=0&bo=1gFGAQAAAAADF6I!&tl=1&vuin=599083727&tm=1582858800&sce=60-2-2&rf=viewer_4"机器学习图")
</center>
 


从数据集合Tranning set 通过Learning Algorithm学习模型，得到一个假设函数hypothesis，笔者认为这就是一个典型的学习过程，类似人类在学校里面接受教育，在学习完毕之后，给定一个input给到受过学习的系统，系统给出应答output，也就是运用学习成果的时刻。

从最简单的线性回归问题来看，一连串(x,y)的数据就是Training set 。

利用一个经典的模型获得了一个假设函数。

> y = a0 + a1 * x

显然，上面这个函数很模糊，具体的a0 a1的值没有给出来，还是没有解决实际问题，因为做出上面的假设，根本不需要数据集合的输入。

笔者认为机器自己通过一个数据集合的输入，自己找到最佳的参数a0 a1的过程，这才是学习算法产生作用的地方。不需要人工的去判断a0 a1的值，而是让机器自己整定，通过一系列数据的输入。

笔者认为，机器学习的过程就是试错的过程，不停的试验各种a0 a1的取值，观察这样的取值是否是最好的。

这里就出现两个问题

 **1 怎么试a0 a1 的值，初始值是多少，每次变化多少？--梯度下降**

 **2 怎么才算对，怎么才算好？机器没有感受，只能用数值做判断。--代价函数**


针对这个问题，吴教授提出了 “batch梯度下降法”的学习算法，完全解决了上面两个问题。使得机器有目标、有效率的试参数，得到最佳的参数整定效果。

当通过机器学习的方式，获得了合适的a0 a1参数，那么h函数就确定了，机器也就“毕业”可以工作了，我们大可重新考验他，把过去已经教给他的知识再问他一遍，她一定会“尽可能的” 告诉你之前你交给他的知识。




##3 简单的机器学习算法 -- linear regression 机器学习中的“HELLO WORLD”





##4 梯度下降法对数据集进行线性回归预测，使用python语言练习
