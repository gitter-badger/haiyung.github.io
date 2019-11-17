---
layout: cnpost
title: 做软件开发的第一年，最少用到哪些技能（最少篇）
date: 2019-11-14 23:59:00
categories: cn
tags: 程序员入门指南
--- 

__Contents__

* content
{:toc}

## 前言

你好，这是“做软件开发的第一年”系列，预计两集，这是第一集。

很多东西刚刚入门的时候你看着挺简单，比如象棋、围棋，规则非常简单，也很容易学，可真的要下好，需要付出巨大心血。

软件研发行业，对你我来说，很可能入门都不容易。

- 首先，入门规则不像马走日、象走田那样直观、有趣、像顺口溜；
- 其次，无法用生活经验去解释。比如经济学，因为大家都处在经济生活中，所以一些基本的理论几乎是看得见、摸得着的，一说就明白，但要硬把软件的运行原理拎出来，就有点儿难为人的意思了。

这与计算机在我国普及的时间有关系，也跟计算机本身就是一门独立的、带有自然科学性质的学科有关。做软件开发，尽管他没有想象中的那么难，但知识的积累是少不了的，除此之外，还需要时间，需要你的耐心，有时甚至需要你忍一忍。

在本文中，我会分享作为职业开发者（初级）的一年多来，我，用到了什么技术上的硬技能。我是做 Go 语言方向的，那么 Go 初级开发者又会用到哪些基础知识，本文也会有提及。

不过，仍需要额外做说明的是：局限于自己的水平、眼界，我只能就我自己的开发经验对所谓的“软件开发的第一年”进行定义。当然，每个人都有每个人的成长曲线，我将我自己的成长轨迹分享出来的目的,

1. 这段岁月很快就成为历史，如果不用文字加以记录，我怕十年、二十年以后，我便忘了。明明经历了，却若有若无、没有印象，是件挺可怕的事。
2. 如果你是个零基础的同学，不要怕，一步一步来；
   
   如果你是个有些许基础却没实战经验的学生，尤其不是根正苗红、计算机科班出身的朋友们，出校门后，要面临找工作，很多技能已经成为事实上的标配了，希望你能警觉；
   
   如果你是个高材生或者是工作 N 年的大佬，希望这篇文章能让你看到自己当年的模样。

## Hello-World

酷壳网作者陈皓老师写过一篇文章《[HELLO WORLD 集中营](https://coolshell.cn/articles/169.html)》,读完以后你就知道，“Hello-World”在我们软件开发者中的地位了。

“Hello-World”是什么呢？就像我们小时候学习英语从“Hello.How are you.I'm fine,thank you.”开始学起的一样。

你首先需要明白的是，计算机编程语言跟汉语、英语、俄语、法语差不太多，本质上都是“交流”的工具，刚才说的几种语言要解决的是“**人与人的交流**”，而编程语言要解决的是“**人与机器的交流**”。

“Hello-World”是你通过某种编程语言向计算机说的第一句话：你好，世界。跟“Hey,guys”差不多。

“Hello-World”很简单，也非常关键。

- 首先，它是你入门计算机编程的第一课，是发端，是启蒙；
- 其次，它是你编程路上的一个里程碑似的存在，即便 N 年过后，我坚信你依然无法忘记你初试牛刀时的新奇与激动；

下面我们就来看看不同的编程语言是如何跟计算机“打招呼”的吧。

_（以下仅列出常用的编程语言 Java、Python 和 Go 的 “Hello-World”，更多请参见陈皓老师推荐的 [The Hello World Collection](http://helloworldcollection.de/)）_

```java
// Hello World in Java
class HelloWorld {
  static public void main( String[] args ) {
    System.out.println( "Hello World!" );
  }
}
```

```python
# Hello world in Python 3
print("Hello World")
```

```go
// Hello world in Go
package main
import "fmt"
func main() {
 fmt.Println("Hello World")
}
```

我们不考虑你安装环境的问题，也不考虑这些代码怎么运行，我们仅从“语法”的角度看看它，你猜，它在干什么？

你看到每门语言的语法都不一样。没错！中文跟英文的语法也不一样，发音还不一样嘞，但你知道“你好啊”和“Hello”都是表达相同的意思。上面三段代码虽然表现的形式不太一样，但意思是一样的，你注意到每段代码都有一个用双引号包裹着的“Hello World”了吗？

一个字（包括汉字和英文字母），被用双引号包裹，这在计算机编程里是有特殊的含义的。我们想个场景：

> 你是如何跟别人说话的？

这个问题乍一听很奇怪，怎么说话的，当然是张嘴说话啊。没错，但还不够。最起码，张嘴说之前，你应该知道要说什么吧。

说话的过程：

1. 思考要说什么- -组织词汇
2. 怎么说- -选择语言
3. 说- -张嘴说话

人跟人之间的交流你当然熟悉了，不用费一丁点力，不假思索的就可以把话说出来，轻松的走完上面三步，用时有时都超不过 1 秒钟。

跟计算机交流，过程是一样的，但毕竟对方是机器，同样的三步，做起来就免不了有些繁琐。

> 第一步：你要用双引号把你要说的话存储起来，跟人说话的时候你会存到人的大脑里，跟计算机对话，你就把话用双引号引起来，它代表你组织好的词汇。
>
> 第二步：跟计算机交流可以用很多种语言，你要把对应的语言捋顺了。
>
> 第三步：张嘴说话环节需要你用对应的语法“说”出来，中文叫“说”，英语叫“say”，Java 叫“println”，Python 叫 “print”，Go 叫“Println”。

通过一个 Hello-World 你可以一窥编程的究竟。

有人会说：平常一句随随便便打个招呼，放到计算机编程里，就要搞的如此复杂？

不是编程把事情搞复杂了，而是这件事本身就这么复杂，只是你身在其中，这么多年习惯了，没把它当回事。

编程对人有几个非常显著的好处：

- **_编程语言的语法全程英文。_**这是一个很好的沉浸式学习英语的机会；
- **_编程会强迫你进行深入思考。_**就好比刚才讲的“说话的流程”，即便是说话这么简单的事情，其实细想起来，也不简单。任何一件事情都是这样，如果你对这件事情没有足够深刻的认知，你是无法动手编写相应的程序的。
- **_编程会让一个人做事的方式更加科学化。_**思考是后续编写程序的基石，很多时候，思考花费的时间比写程序的时间要多得多，程序写完之后还需要做测试，及时回收问题，修正问题，这是一个非常科学的做事习惯的问题，从长远角度，这种习惯会节省大量的资源，包括时间、人力、物力和财力。
- **_编程会训练抽象思维。_**编程工作面对的往往是比较复杂的问题，比如把全班人按姓名排个序，你手动排序试一下。你会把姓名列出来，一个名字一个名字的比较。这时候给你 10 个班、100 个班，每个班的姓名都不一样，你还吭吭哧哧一个姓名一个姓名的比较吗？有没有一个通用的、普遍适用的方法？就像公式一样，不管什么名字，多少名字，我都能给你排序，这就需要动动脑筋了。

**总的来说，编程有清理大脑垃圾的功效，并训练大脑相关肌肉群，让大脑变得更加健壮、更加性感。每当面对复杂的事物，你那经过编程训练过的大脑，会更有目标性、针对性，通过分析，更能把握住事情的重点、关键。最起码，能有理有据的分析出事情的原因、经过以及可能的结果，有哪些突破点、潜在的风险点等等。到现在，我找不到更好的工具了。**

Hello，world。你跟计算机世界打过招呼了吗？

## 流程语句的控制

说完 Hello-World,我希望你有了对编程基本的认知：**用规定的语法来操作计算机。**

我们还需要逐渐掌握更多的语法。编程语言的语法不难，如果英语的语法难度系数是 100，那编程语言基础的语法就相当于 5 这个高度。因为编程语言的基础语法就来自于生活。

我们生活中有类似的场景：

- 如果你拿了钥匙，就可以开锁；
- 交作业忘了写名字，被罚写名字 1000 遍；

这两个场景背后代表的逻辑非常典型。

第一个场景是如果...那么...句型，是因果联系，即只有满足了某个条件，才可以完成下面某个动作；反之，不满足条件，则后面的动作无法执行；

第二个场景是来来回回、反反复复、翻来覆去句型，即同样的动作，被重复执行。

编程语言也是语言，编程语言来自于生活，任何编程语言，基本都具备这两个语法。

用编程语言来说，第一个场景是if...else...，第二个场景是 for 循环，他们代表着程序的**运行流程**：

```go
var a = 10
if a == 0 {
    fmt.Println("a = 0")
} else {
    fmt.Println("a ≠ 0")
}
```

上面这段代码是什么意思？有一个 a,这个 a 的值为 10，接下来有一个“流程语句”，说：

> 问 a = 0 吗？（两个等号就是在发问，问是否相等）
>
> 如果等于 0，那么就输出 “a = 0”
>
> else 是“其他”的意思，放在这里意思是说，除了 a = 0 外其他的情况，就输出“a ≠ 0”

你明白if...else...了吗？还有一个 for 循环，我就不打算举例子了。

希望这两个“流程语句”能引发你思考。其实，我们的世界里充满了类似的逻辑，有很多“只有这样...才能那样...”的例子，有很多来来回回、反反复复的例子，希望你能思考一下，如果没有了因果联系，这个世界将会怎样。

这两个逻辑在现实生活中至关重要，在编程工作中同样。

## 遍历数组和字典类型数据

你需要明白什么是数组、字典。

这两个东西在编程中简直太常见了。

不过，对于初学者来说，这两个数据类型仍然非常让人费解，很可能不能理解它存在的意义。这很正常。

形象点来说，数组是一列车厢，里面工工整整的坐满了人，1 号 2 号 3 号，各就各位，互不干扰。

字典是你期末成绩单。语文：59分；数学：89分；英语：76分；一个科目，对应一个值，科目和值像是搞对象似的“绑定”到一起。

车厢（数组）、成绩单（字典），他们有一个共同点，你感受到了吗？

> 他们都像容器一样能够存储数据。

请问，数据如何存进去？数据如何取出来？

因为数组、字典在编程过程中用的实在太频繁了，那么里面数据的存、取，用的次数就太多了，你一定要弄熟练。

## 字符串处理

又是数组又是字典的，怎么这么多事儿啊？别急，还有字符串、布尔值等类型呢？

如果你是初学者，我相信你在学了两个数据类型后就开始不舒服了，那是一种脱离舒适区的不快，我曾经就真切的感受到过，并且还放弃过。

有这个感觉很正常，希望你能理解一下计算机，毕竟这么大的玩意儿，要解决的东西这么多，规矩嘛，还是应该有的。

其实呢，每一种数据类型都有它自己的特点，什么时候用这个，什么时候用那个，是非常明确的。你应该坚信，每一种数据类型都将是你未来的得力助手。

编程语言是工具，那么编程语言的流程语法、N 多种类型就是**让工具成为工具的工具**。

你说，现实生活中：

> 如何把名字倒过来写？
>
> 名字中的姓氏是？
>
> 名字中的名为？

你看，上面的问题不过分吧。

你的名字在程序中就是一个字符串，如何把字符串反过来写？如何得到字符串中的第一个值？如何得到字符串中第一个以后的所有值？

这些，就是字符串的处理。

## 正则表达式

推荐你去看余晟老师所著的《正则指引》。

我的第一份工作、第一份工作要处理的第一件问题，就是写**正则表达式**。

<p>
    <img src="/images/my_first_programming.png" width="68%">
</p>

正则表达式是对字符串的另一种处理方式，它像一把筛子，而字符串就好像筛子上面的大大小小的粮食，通过这把筛子，就可以把合你心意的字符串收入囊中了。

举个简单的例子，有很多文件名，我希望从这些文件名里挑选出以 golang 开头并且以 pdf 结尾的名字，这时候有两种办法：

1. 不用正则；遍历每个文件名，对每个文件名进行判断，是否以 golang 开头，是否以 pdf 结尾；

2. 使用正则；写出正则表达式，再遍历每个文件名，利用正则直接就可以判断该文件名是否符合要求；

简单来说，正则表达式是对字符串进行“筛选”的工具。

## 排序和分页

排序和分页这一节，讲的就不是关于某门编程语言的基础知识，它是一个功能。

下面我出个题目，你来想一想：

> 全班有 60 个人，要求你能按照名字将同学们顺序排列，并将排序后的结果打印在 A4 纸上，每张纸 10 个人；

不难对吗？思路是先把这些人按照顺序排好，再 10 个人一组即可。

这里面有难度的地方在于使用什么样的方式把这些名字排序？

使用的“方式”、“方法”在计算机科学里有个酷酷的名字：**算法**。

常用的排序算法有：冒泡排序、选择排序、快速排序。希望你能掌握它们，它们是解决排序问题的**王**！

## 函数

啥是函数？你学过的第一个函数应该是 y = x + 1。

啥意思呢？用初中数学的解释就是：

> x 是自变量，y 是因变量，因变量 y 随着自变量 x 的变化而变化。

我们把 x 称作输入，y 称作输出，那么从这个函数来看，只要输入给定，那么输出也必然是固定的；比如 x 为 4，y 肯定得 5。

函数体现出了某种抽象的对应关系。还是拿 y = x + 1 来说，无论你给到什么数值，它都会输出比这个值大 1 的数，它不是仅仅对某个数字有效，而是无差别的对任何数字有效。函数的抽象就体现在不局限于某一个个体，它阐述的是一个普遍适用的关系。

拿上一节的排序来说，如果你的方法仅仅支持对本班 60 个人的名字排序，那这就算不上一个函数；如果你的方法可以扩展到任意班、任意数量的人，那就是函数了。

函数是具有普遍意义的方法。

## 对象和对象中的方法

程序员世界有很多黑话，比如：面向过程编程、面向对象编程、函数式编程，以及难以启齿的面向搜索引擎编程。

其实，我认为，就只有两种编程思想：

1. 面向热爱编程
2. 面向人民币/消费者编程

哈哈哈哈，开个玩笑。

言归正传。我们在编程过程中，若仅仅使用函数的方式，不足以支撑起现在逻辑如此复杂、量级如此庞大的软件，这就用到了对象（object）。

函数是什么？函数是一个个具有普遍适用性功能的工具，就像炒锅、剪刀、锯子这些工具一样，那么对象是什么呢？对象就是使用这些工具的人。人是一个对象，这个对象拥有诸多独特的技能，比如会用炒锅炒菜，会用锯子砍树，这些技能是其他的“对象”所不能掌握的，比如狗，狗也是个对象，狗会汪汪叫，这个技能也是其他的对象所不能掌握的。

那么什么是对象？对象是一个具备某些技能的个体。这些技能的表现形式是“对象中的方法”（简称“方法”），方法与函数相比没有大的区别，但因为对象中的方法隶属于某个对象，而函数则是独立的，所以在名字上做了区分。

当然，以上的观点不能代替你的学习，我只是希望在这里能够抛砖引玉，希望你能通过更多的学习渠道把“面向对象”搞清楚，要学，请深学。

## Linux 操作系统基础

你非常熟悉操作系统，比如 Windows 或者 Mac OS，你甚至经常帮周边的朋友们重装系统、解决各种使用上的疑难杂症。

但这不够，作为一个软件工程师，Linux 操作系统是你必须掌握的操作系统。因为你的软件很大的可能性是运行在 Linux 服务器中的。

Linux 操作系统就是你代码的“生存环境”，想一想假如人类不了解四季的更替、天气的变化，那会是怎样的灾难。不了解操作系统的软件研发人员，最终的成品也很有可能像台风过境一样糟糕。

作为新手，了解 Linux 操作系统，到底需要了解什么？

1. 我们与 Linux 进行交互的方式跟在 Windows 上用鼠标单机、双击不太一样，那是一个黑压压的窗口，一种类似于一问一答的交互模式，你要适应它，这个适应的时间跟你使用它时间长度成反比，即你越强迫自己尽可能多次的使用它，你适应它的时间就会越快。
2. 目录管理；就相当于 Windows 上的“新建文件夹”、“删除文件夹”。
3. 文件管理；比如文件的创建、删除、复制、移动。
4. 软件管理；即如何在 Linux 操作系统之上实现安装、查询、卸载软件包的。
5. 用户管理；比如添加、删除用户、用户密码、用户权限等等。

## Vim 的基本使用

就像 Windows 操作系统下人尽皆知的“记事本”功能一样，Linux 操作系统下也有一个著名的、功能极其强大的、入门曲线极其陡峭的文本编辑工具- -Vim。

若你使用 Linux 操作系统，那么像打开并查看文本文件这样的操作应该是家常便饭，Vim 这个工具值得你探索一下：

- 模式转换
- 光标跳转
- 编辑命令
- 撤销命令
- 翻屏操作

说起来，真的不少呢。

##  SQL 语句

你需要了解什么是数据库。因为在工作中，写一些 SQL 语句是一件寻常的事情。

流行的数据库 Mysql 是个不错的选择，有机会深入的学习 Mysql 数据库的运作机制对你和我来说很可能是个挑战，不过也是个不错的机会。

## 代码管理工具- -Git

假如你是老板或者软件中心的总负责人，你一定特别希望做成一件事：知道每个人都做了哪些工作。

放到软件研发工作上来说，这就是 Git。

一个项目由多人维护，哪行代码是由谁写的，又是由谁在哪一天哪个时间点因为什么事情做更改了，这些事情我们必须要知道。如果没有一个完整的记录，会造成以下问题：

- 无法追踪文件变动的历史
- 多人合作开发代码统一的问题
- 对代码有疑问寻找作者以及出了故障如何追责

Git 是个性能强大的、分布式的版本管控系统，非常适合团队形式的项目开发。Git，你值得拥有。

## 其他可选

- redis
- nginx
- 代码重构
- 同步、异步
- 并发控制

## Go 语言技术栈

beego/RESTful/kubernetes/docker/grpc/cobra/consul/prometheus

<br>

本文完

请看下集：《做软件开发的第一年，还需要用到哪些技能（还需要篇）》