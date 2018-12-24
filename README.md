# 18年912真题回忆

说在前面：912 的试题在一个A4 纸一半大小的牛皮纸信封里，试卷是雪白A4竖版印刷，有好多页，在左上角钉，是对折了之后放在里面的。

## DSA:70'  
### 判断题(12*2'):  

1. $n^{log(log(log(n)))}$ 等于 $O(\biggl\lfloor log(n) \biggr\rfloor)$

- Huffman 编码树中，如果交换深度不同的两个树结点，那么一定会增大整体编码成本

- 基数排序的底层算法如果不稳定，排序的结果有可能是错的。

- 有2019个叶节点的真二叉树数量比2018对括号的合法数量要多

- 如果访问不具有局部性，伸展树不能保证O(log(n)) 的访问时间

【还有几个忘了】

### 简答题(8*4'):

要求每题小于80字。

- 把常规表达式转换成 RPN（逆波兰表达式）已经相当于是一次常规表达式的求值，那为什么还要把他转换成RPN？RPN有啥好处？

- DFS（广度优先搜索）中， 什么时候标记前向边，什么时候标记后向边？
- Dijkstra 算法在稠密图上运行时，为什么用多叉堆而不用完全二叉堆？以及堆的分叉数怎么确定？

【中间还有几个忘了】



- 相对于开放散列，闭散列的优点？请举出两点。
- 锦标赛树和败者树（loser tree） 的一道题【具体忘了】
- 相对选择排序，插入排序有哪些好处，举出两个并解释

- 红黑树有的时候比AVL书要好【后面忘了】
- KMP 算法什么情况下比蛮力搜索更高效？

【还有几个忘了】





### 二叉树(7'+3'+4'):

给出了二叉树的结点链式实现，实现里每个节点有size（以自己为根的树的总结点个数）和左右孩子。

还有一个类似层次遍历的函数，即给出根节点和秩，返回指定序号元素（0开始编号，按后序遍历顺序编号），中间有一大段代码空出来了。【这里我描述的不清楚，请补充完整】要求是时间复杂度控制在` O(depth(x)) ` 内， 提示了不可以直接后序遍历，因为那样复杂度搞不得分。

1. 填空实现相关功能（少于12行，按有效代码记）。
2. 解释相关算法（少于200字，可以配一张图）。
3. 证明时间和空间复杂度。















## 计算机原理:30'

### 选择：

【待补充，完全忘了】

1. 第一题
2. 第二题
3. …

### 填空（1',2'的都有）：

- 一个十进制正数的32位补码，用十六进制表示，小端机器。

- 一个负的小数（好像是 -27.625），转32位ieee754浮点数表示
- 写出三种解决数据冲突的方法
- 写出三种Cache缺失的原因

【好像是4道题？还有没有了？求确认】

### 流水线(好像是5'?)：

【彻底忘了，求补充】

bla

bla





## 操作系统:30'

### 填空(15*1'):

*填空题大概是10道题，但是每道题有至少一个空 *

- （>=3个空）Stride调度算法的溢出相关问题，溢出之后可以巧妙的回避溢出，用了8位的无符号整数【后面忘了】
- （2个空）CPL，DPL，门和段的特权级判断问题
- （3个空）信号量的实现，PV操作的函数里面挖掉了3行
- （2个空）父进程退出，子进程没退出，子进程变成啥？子进程退出，父进程还没 wait，子进程变成啥？
- 【中间有好几个题】



- （2个空）inode，硬链接，软连接和链接数量

### 判断(5*1'):

- …
- …
- …
- …
- …

### ucore(6'):

给出了好多代码有 `switch.S` ，进程上下文的定义，进程切换的代码。

要求读玩代码之后，写出实现功能的位置：

-  切换页表的代码
-  切换堆栈的代码
- switch 函数中读取两个参数的代码

### 页表(4'):

【彻底忘了，求补充】

bla

bla

## 计算机网络（20'）:

### 选择(6*1'):  

1. 电话网，电路交换，IP电话，分组交换，报文路径

- 【题号记不清】源与目的的距离越_远_，传输速率越_大_，发送的数据位数越少 ，停等协议效率越低。

- 【题号记不清】计算传输速率【1Gbps 2Gbps 200Mbps 100Mbps】

- 【题号记不清】给了传输速率，计算延迟【1.5s 1.6s 2.1s 3.1s】


5. CSMA/CD 计算速率
6. TCP 窗口 加性增，乘性减，MSS，W


### URL大题(4'):  

给一个 URL:http://info.tsinghua.edu.cn:80/index.jsp，服务器 IP 是 `166.111.4.98` 。

1. 说出这个 URL 各个组成部分
2. 一般来说，在浏览器里输入 http://info.tsinghua.edu.cn:80/index.jsp 跟输入 http://166.111.4.98:80/index.jsp 看到的是一样的。
   1.  如果输前者能打开，后者打不开，这可能是什么原因?
   2.  如果输前者打不开，后者能打开，这可能是什么原因?



### IP、路由器大题（10')：


给了一个 /24  的IP地址，还有一张拓扑图，让分配主机和路由器的网段。

1. 分配 IP
2. 解释在这里 ARP 在子网内 和 跨越子网 分别怎么工作。
3. 写出每一跳的 源IP 目的IP 源MAC 目的MAC。