--- 
layout: post
title: "闲话彩票的误区"
tags: 
- Statistics
- loterry
status: publish
type: post
published: true
category:
  - Statistics
---
前段时间应朋友之邀请，在新华社某个栏目做了一期小节目，主题是`彩票可不可以作为投资手段？` 正好，借着这个机会说说大家对彩票的误区。

# 先说说公正性

在国际上彩票的各期投注结果是需要进行随机性验证的，一般的验证由高校的研究所主导，一般来说
大概会有上百种统计方法来验证彩票开奖的随机性，并随时发布在官方网站上供民众查询。
比如09年我曾写过一篇博文，说明为什么[福彩双色球是随机开奖的](http://bjt.name/2009/07/welfare-lottery-justice)，也是利用了
一种证明随机性的方法。


同国际相比，国内福彩和体彩就明显有中国特色了，是采用一种叫做`公证员公正`的方式来保证彩票的公正性，而不是用更为科学的概率论。
虽说北大和北师大都有传说中的彩票研究所，但同两大彩票发行机构却并不同步，略有遗憾。


# 关于赌徒谬误


彩民在投注的时采用的策略有很多，比如奇偶法、大小法、质数法、和值偏差追踪法、重复号、连号法、旋转矩阵等。大部分都是按照开彩的号码实际发生概率来
指导投注行为。我们拿36选7乐透型彩票来举例，开奖号码出现3奇数4偶数的概率是0.30，而出现1奇数6偶数的概率则是0.04（同样对于大小法也是如此）

    奇,偶    	  小,大   	出现概率
    0,7 		0,7 		0.00
    1,6 		1,6 		0.04
    2,5 		2,5 		0.16
    3,4 		3,4 		0.30
    4,3 		4,3 		0.30
    5,2 		5,2 		0.16
    6,1 		6,1 		0.04
    7,0 		7,0 		0.00

对于和值也有类似的概率表，但稍稍复杂一点：

![](http://i.imgur.com/gBO8T.png)

彩民一旦通过观察，发现近期的开奖数字同理论概率有不一致，即根据自己约定的规则进行投注。比如根据和值去投注，
前若干期开奖号码和值小于130，则彩民在当次投注时，会尽量要求自己的号码的和值大于130，
但实际上彩民忽略了一个概率，即任意组合的号码都是以等概率出现才满足如上图所示和值的表征，号码和为多少其实并无所谓。


以上的认识误区正式一点的说法是`赌徒谬误`，用掷币游戏来说明说明一下：投掷硬币过程中，如果大量的正面被观测到，那么硬币的反面即将出现。
这种误解归于对方差概念的误解--`机会被认为是自我修正的过程，一个方向上的偏差会引起向反方向的偏差，这样才能恢复均衡`。对于乐透游戏来说，大家普遍
认为如果一个数字先前出现的频率低，那么随后这个数字出现的概率就会变高。结果大家都来选择先前出现次数最少的数字。
同时，还有其他彩民选择出现最频繁的数字。对这种行为，一种解释为，这些数字比较容易被留心；或者，玩家可能认为这些出现最频繁的数字比较幸运。
这些误解被别有用心的报纸和网络过分地渲染，或者被一些软件制造商用来搜索特定式样的前期中奖号码。


# 为什么彩票不是投资途径

很多人觉得只要买一注彩票就是买到了一夜暴富的希望，但那其实是一个彻彻底底的悲剧，大家猜猜看下面那个比率是什么意思？

    > (100000/1400000000/365)/(1/(choose(33,6)*16))*2
    [1] 6.935847

大致的数字解释如下：
> 我国每年车祸死亡大概为10万人（05年官方数字），今年全国人口约为14亿，计算日死亡率。双色球的一等奖概率为1700万分之一，两天开一次奖。
> 大致计算一下，彩民出门去买一注双色球彩票，`路上被撞死的概率是双色球一等奖概率的7倍`。如果加上其他意外死亡，基本上这个比率还需要翻番，大概是
> 10几倍的样子。噢，出门被撞死10次，才会中奖一次。您说稍具理性的人应该不应该去购彩呢。

> 附带广告一则：双色球京东商城有售，可以让你不出家门无风险购彩~~

# 小盘玩法的黑洞

上面说的是大盘玩法，那小盘玩法呢？

以前在出差走访各地，时常会遇到号称是3D玩法的常胜将军。但随着深入的了解发现：这些常胜将军确实有一段时间接连中奖（这从概率上是可解释的），但
慢慢的随着投注次数的增加则开始了亏损（频率收敛于概率）。私下和这些`长胜将军`聊天，他们自己也明确表示：曾经认为能够提高中奖概率的技巧的实际作用其实有限。
但可惜的是，虽然他们已经退出彩坛，但更多的不明真相群众的记忆依旧是这些常胜将军呼风唤雨的假象。显然，这是一个趋利的心理暗示效应！

曾几何时，彩市流行一种投注策略，号称稳赚不赔。具体操作是这样的：

> 买1注彩票，如果中了，重新开始；如果未中，则第二次买2注彩票投注，中了，重新开始；如果未中，则开始第三次投注，买4注彩票，中则重新开始，不中则
> 购买8注彩票（翻番）投注，然后按照这个原则继续、继续……直到中奖为止。一旦中奖，不管累计投注多少次，本策略不但能够返还所有累计的投资，且仍有不菲的盈利。

看，多么天衣无缝的策略，但他忽视了这可是`指数函数`！且不说发行机构是否能够赔付，先看看需要动用的资本。下面是投注15次所需要的资金量：

    > x <- 1:15
    > 2*2^x
     [1]4  8  16  32  64  128  256 512 1024 2048 4096 8192 16384 32768 65536

再计算一下如果要确保以90%的概率最终中奖，需要多少期投注？考虑3D玩法的一注中奖概率为0.001，累计的未中奖概率为：

> (1 - 0.001)^N = 1 - 0.9

求得投注期数N等于2301期。即投注2301期才能保证90%的概率中奖。

2301这个数字稍稍有点大，我们换个说法：到第25次投注的时候需要的资金已经达到1亿3千万，即便是这么大的资金量也只能保证2.5%的概率让你全身而退。
如果到2301期，累加一下所需要的资金量，那可是一个全宇宙的原子总量加和的`正无穷!`



