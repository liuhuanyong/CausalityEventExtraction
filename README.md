# CausalityEventExtraction
self complement of templated based causality event extraction 基于因果关系知识库的因果事件图谱构建demo

# 项目介绍
现实社会是个逻辑社会，大量的逻辑即逻辑经验存在于我们的脑海中，而这些逻辑经验是无法穷举出来的，靠大量人工的总结，显然不切实际。然而，幸好人类将这种逻辑用文字表达出来了，这为我们利用自然语言处理技术实现这种因果逻辑的抽取提供了可能性。不过，受限于自己的技术水平，目前还无法将深度学习这套高端的打发应用于因果事件抽取当中，而以构造和总结因果模板，结合中文语言特点，构建因果语言知识库的方式代替。
本项目是对因果事件抽取以及因果知识图谱构建的一种尝试。

# 技术路线
因果事件图谱技术流程上遵循以下流程：    
![image](https://github.com/liuhuanyong/CausalityEventGraph/blob/master/image/schema.jpg)

主要包括以下几个步骤：  
1、因果知识库的构建。因果知识库的构建包括因果连词库，结果词库、因果模式库等。  
2、文本预处理。这个包括对文本进行噪声移除，非关键信息去除等。  
3、因果事件抽取。这个包括基于因果模式库的因果对抽取。  
4、事件表示。这是整个因果图谱构建的核心问题，因为事件图谱本质上是联通的，如何选择一种恰当（短语、短句、句子主干）等方式很重要。  
5、事件融合。事件融合跟知识图谱中的实体对齐任务很像  
6、事件存储。事件存储是最后步骤，基于业务需求，可以用相应的数据库进行存储，比如图数据库等。    

# 最终效果
经过以上几个流程之后，可以支持各类查询，比如已知原因找结果，已知结果找原因等，这都很有事情，总之，数据库有了，我们可以做的事情有很多，接下来就是我们脑洞的事情了。
接下来以以下几个事件在因果知识库中查询一把：
以上几个图展示了输入既定事件在数据库中相似的事件（一度），相似事件导致的结果（二度节点）。
# 范冰冰偷税漏税事件
![image](https://github.com/liuhuanyong/CausalityEventGraph/blob/master/image/fangbingbing.png)

# 美国攻打伊拉克事件
![image](https://github.com/liuhuanyong/CausalityEventGraph/blob/master/image/gongda.png)

# 寿光发生洪水事件
![image](https://github.com/liuhuanyong/CausalityEventGraph/blob/master/image/shouguang.png)

# 总结
1）基于规则这套，很实用，但问题不少，规则维护比较多  
2）事件表示这块一定要好好想想啊  
3）事件融合这块，利用各种相似度度量进行计算，都有一定缺陷  

# question?
send mail to lhy_in_blcu@126.com
