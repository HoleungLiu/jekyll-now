
> 在此就不介绍机器学习的概念了，请自行google，在此直接看Learning Map。


# ***Learning Map（学习导图）***
| [PDF](http://speech.ee.ntu.edu.tw/~tlkagk/courses/ML_2016/Lecture/Learning%20Map%20%28v2%29.pdf) | [VIDEO](http://speech.ee.ntu.edu.tw/~tlkagk/courses/ML_2016/Lecture/Learning%20Map%20%28v2%29.ecm.mp4/index.html) | 
|-|-|-|

----
先来看一张李大大的总图↓

![先来看一张李大大的总图](http://img.blog.csdn.net/20170520185249205?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

鉴于看起来不是很直观，我“照虎画猫”做了一个思维导图如下：

![这里写图片描述](http://img.blog.csdn.net/20170521003122947?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

理论上Supervised Learning分支下的内容都可以放在其他Learning Map大类下。


----------
# 1. ***Supervised Learning***
所谓监督学习，就是我们告诉机器说，当这个function看到某种input则输出a，看到另一种input输出b，看到……
### ***Supervised Learning-> Regression*** 
Regresion： **The output of the target founction f is ‘scalar’**. 如果我们在机器学习中要找的function输出是数值，

 举个例子：
 预测PM2.5进行天气预报。
![这里写图片描述](http://img.blog.csdn.net/20170520204609319?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

核心思想就是：**连续函数下进行预测**。
### ***Supervised Learning-> Classification***
分类问题有两种可能，Binary Classification 输出是或否，Multi-class Classification输出多个类型。

 ![这里写图片描述](http://img.blog.csdn.net/20170520205210389?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

**举个例子：**

Binary Classification： Spam filtering（垃圾邮件过滤），判断是垃圾邮件，不是垃圾邮件。

Multi-classification： Document Classification（文件分类），将文件分为政治、经济、体育等多个大类。


----------


      
#### ***Classification->   Linear Model 与 Non-Linear Model*** 

**Linear Model :** 能做的事有限，一些简单的模型可以用它来做，但遇到复杂问题就力不从心了。

**Non-linear Model :** For example，现在的深度学习就是一个Non-linear Model，能完成一些很复杂的工作，比如图像分类等。
     

 - Classification-Image Recognition：输入一个图片，通过一个很复杂的卷积神经网络（CNN）的Function判断是猫是狗还是猴子，每个可能的物种是class。
 
   ![这里写图片描述](http://img.blog.csdn.net/20170520210849049?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
   
 - Classification-Playing Go：输入棋盘上的局势，判断下一个落子的位置，每一个可能的落子位置就是一个class。
 
 ![这里写图片描述](http://img.blog.csdn.net/20170520211419277?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 


----------


 
### ***Structuerd Learning***
在实际运用中，常常会遇到Beyond Classification的情况，比如语音识别，人脸识别，语言翻译等，是结构化输出。此类问题常配合Reinforcement Learning 解决。

![这里写图片描述](http://img.blog.csdn.net/20170521003604856?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

----------
# ***2. Semi-supervised Learning***
 
 **example：**要建立一个辨识猫与狗的系统，手上有一部分Labelled data（已经标记好的猫狗图片），和**一部分Unlabeled data（未做过标记的猫狗图片）**，那么Semi-supervised Learning做的就是利用Unlabeled data优化function，也常用于数据不足时进行学习。
 


----------


# ***3. Transfer Learning***
**example：**还是建立辨识猫与狗的系统，手上有一部分Labelled data（已经标记好的猫狗图片），和**另一部分与猫狗没有关系的图片（比如狮子老虎，标未标记都可）**，那么Transfer Learning就是利用这些data优化function。
![这里写图片描述](http://img.blog.csdn.net/20170520234607722?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

# ***4. Unsupervised Learning***


**example1：** 要让机器学会阅读，希望机器自己在网络上爬去很多文章，自己理解其中的意思，进而取得人类的一些理解，掌握阅读的技巧，这就是非监督学习要做的。

我们知道，做machine Learning就是要找一个function。比如在学会阅读这个系统里，我们给系统input一个“apple”词汇，然后让机器看懂。在Unsupervised Learning 中没有人告诉机器每个词汇表示什么意思，只有大量text喂给机器。

![这里写图片描述](http://img.blog.csdn.net/20170520235436710?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


**example2：**要让机器学会自主绘画，我们只给机器呈现显示世界中的景象并不做标识，机器要从中提炼绘画风格与内容，学会通过作画表达自己。

![这里写图片描述](http://img.blog.csdn.net/20170520235848895?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

# ***4. Reinforcement Learning*** 
在实际运用中，以上方法并不能解决全部问题，常常会遇到Beyond Classification的情况，比如语音识别，人脸识别，语言翻译等，那么就要通过增强学习来解决问题。

增强学习的一个非常知名的应用就是 google 阿法狗。


----------


### ***Reinforcement Learning VS Supervised***
增强学习与监督学习有什么区别呢？
**example1：**用一个语音识别的例子来解释：

Supervised 就像给了机器一个点读机，他听到一句话时可以看到其含义，每一句话都有标签，就像有一个**手把手教他的老师**。

而Reinforcement Learning 就像跟女朋友对话，反复讲来回讲很多句话，直到女朋友觉得你无言以对愤然离去，**机器唯一可以知道的就是他做的好还是不好**，除此之外没有任何information。而这更像人类现实生活中的学习过程，必须自己像哪里做得好做得不够好，怎么修正。

![这里写图片描述](http://img.blog.csdn.net/20170521001424423?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

另一个例子，下围棋。

**example2：**   

supervised： 给机器一堆棋谱，告诉机器，情况a则落子在“5-5”处，情况b则落子在......

Reinforcement Learning:  让机器自己下棋，下过几百手之后，机器只知道自己赢了还是输了，下的好还是不好，机器必须自己想办法做提高。

![这里写图片描述](http://img.blog.csdn.net/20170521002507085?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

Alpha Go is supervised learning + reinforcement learning.


----------
# 学习导图总结
**有一个非常重要的信息是每一个框的颜色。**

![这里写图片描述](http://img.blog.csdn.net/20170521003838295?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc291bG1lZXRsaWFuZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


----------


 - **蓝色部分代表scenario，意思是你现在有什么类型的 training data。**

| machine learning | scenario | 
| ------------- |-------------|
| Supervised Learning | 有标签data |
| Semi-supervised Learning | 部分有标签data | 
| Unsupervised Learning | 无标签data |
| Transfer Learning | 一堆不相干data | 
| Reinforcement Learning | 只有来自外界的评价 | 


----------


 - **红色部分代表task，意思是现在function的output是什么，只体现在supervised中，但其实可以插在以上五种Learning的每一种内。**
| machine learning | task(output) | 
| ------------- |-------------|
| Regression | scalar |
| Classification | class1、class2...之一 | 
| Structured Learning | 有结构的内容 |


----------


-  **绿色部分代表Method方法模型，比如在Classification中有Linear模型 or Non-linear模型，我们可以将绿色部分插入任何红色部分中。**


  
