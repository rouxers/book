# 两桥的搭建

<!-- | ![](http://cube.rider.biz/visualcube.php?fmt=svg&bg=t&size=150&stage=f2b&alg=RUM%27UR%27U2) | (U2) R U M' U R' <br> (U2) R U' M U' R'|
|:--:|:--:| -->

本章介绍如何提升搭桥的能力。我们将逐个讲解以下话题：底色/桥色选择、左桥、右桥、和其他两桥搭建法。

## 块筑构(Blockbuilding)的大体策略

块筑构，英文blockbuilding,是指用直觉可以理解的方法去高效地构造魔方中的一些连在一起的块的方法，例如2x2x2,1x2x3,2x2x3等块。常见于一些速拧方法（包括桥式和petrus）以及最少步项目中。这份最少步教程的[“块筑构”章节](https://fmcsolves.cubing.net/fmc_tutorial_ENG.pdf#section.2.1)中有对于基本策略的实例和解释，桥式速拧尤其是左桥中，也可以作为参考。

## 左桥 vs 右桥 ：相同与不同

如果你从桥式入门法过来，你的左右桥做法应该是比较相似的：先做底下的棱，再做两组棱角对——先把棱块放到底下，再跟角块组到一起，最后插入。但是你要知道，进阶以后，左右桥在本质上的区别就会凸显出来：

- 左桥的规划是静态的
    - 你可以运用预观察时间来充分观察魔方，经过深思熟虑，得出一个高效（步数短）的解法。

- 右桥的还原是动态的
    - 你需要实时地跟踪魔方块，并且在一瞬间对于解法作出决定。你可能会为更好的连贯性（即不停顿）而牺牲解法的效率。


## 选择你的桥色

所谓桥色，指的是你会在几种不同的块上面做左桥。也就是说，左桥你能接受的底面颜色（底色）和左面颜色（侧边色）的颜色组合有哪些。

作为新手，你可能只有一到两个固定的桥色。那么，为了充分利用盘面的简单情况，你应该拓展自己的桥色，让左桥变得更好做。这个过程应该越早越好，对颜色形成惯性后就不容易改了。

我们先说叫法。中文里，桥色一般以“A底B色桥”来描述。例如，双底四色桥就是在某一组对面底色（例如白黄底）上，四个侧面色（以白黄为例，就是红橙蓝绿）的左桥都能做。加起来，就是八种选择。

高手中，最常见的桥色是”双底四色桥“。它提供了八种左桥的选择。如果你现在的桥色只有少于八种，例如你是”单底四色“或”双底双色“，那么高度建议你改到”双底四色桥“。

这是因为双底四色桥，是能让你利用所有盘面上现成的棱角对的最低要求。左桥选项如果更少的话，你能遇到现成棱角对的概率就会大大降低，你的平均情况就会更困难。如果实在无法拓展，那么四个选择也勉强可以接受，然而若桥色再少的话，就有自讨苦吃之嫌了。


<!-- (on a side note: x2y2 means that you're more sensitive to the L/R sides as their colors are fixed.  ) -->

关于六色桥（六底四色桥）: 六色桥能提供24种左桥的选择，在解法上显然比双底四色有优势。然而，与之相应的观察难度会更高。实践中，因为大多数玩家初学时没有刻意拓展底色，所以惯性使然，仍然是双底为主。六底乃至四底桥色的玩家存量不多，现在的代表人物只有四色四底桥的Fahmi Aulia Rachman。有人反对多色底，认为双底再往上意义不大，因为太多左桥观察不过来。然而，也有支持的意见，认为六色底玩家对任意的左桥方块（即122）都有两种拓展到左桥的方式，这样左桥后一组就会简单很多。Fahmi也表示过，四色底确实帮助他，让很多左桥都变得很简单，因而能在预观察时看到更远（例如FB+SS)。总而言之，多色底桥确实是值得探索的，但也不必强求。

关于不同桥色的步数统计：如果你对此感兴趣，可以参照以下资源：

- [桥式步数统计表](https://docs.google.com/spreadsheets/d/1EectP3O_qwQp_2WohbDrlohxhs2ee17sjFfxZr_-D1g/edit#gid=0) - 比起单底四色桥，双底四色桥能提高左桥方块简单情况的概率从不到60%到80%.

补充说明：英文的底色和桥色一般是这样描述的：用一到两个转体操作来指代，例如x2y。意思是说，随便选定一个你会的左桥，然后对魔方做以下转体之一： {y, y', y2, x2, x2y, x2y', x2y2}（一串操作，其中每个操作都属于x2或者y的叠加)，那么转体操作完成后的那个左桥，一定也是你会做的左桥，而且所有你会做的左桥，也都能通过某一串这样的转体操作来达到。或许有点难以理解？记住结论就可以：x2y就对应我们常说的“双底四色桥”。x2y2对应“双底双色桥”。y对应“单底四色桥”。例外地，四底四色桥无法直接描述，一般称之为“dual x2y”,即“双x2y”。最后，六色桥（六底四色桥）一般称之为“CN (Color Neutral)”。
