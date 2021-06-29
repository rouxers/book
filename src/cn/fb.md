<script type="text/javascript" src="twistysim.js"></script>
<style type="text/css" rel="stylesheet">
/* modifies the opacity of the cube wireframe */
.ttk-shp-poly {
    stroke-opacity: 0.3;
}
</style>

# 左桥

## 解法篇

### 第一步: 掌握基本的筑块法

入门法往往是固定先做底棱的。现在你应该多了解几种搭建左桥的策略了。大体来说，左桥的搭建有四种策略，总结在下面的表里。

- 方块+一组（最为常用的两种）
  - 1.先做底棱，再做两组棱角对 
  - 2.通过横向【棱角对】和【棱心对】构成方块，再做一组棱角对
- 3.三三法
- 4.先做其他块，最后利用S插入底棱

在看实例之前，建议先看一些介绍策略的视频，对四种方法有基本的认识。
视频里的表述会各有不同，但万变不离这四种方法，尤其是前两种。

左桥策略讲解：
- [如何在观察时高效搭建左桥 by teoidus](https://www.youtube.com/watch?v=0Cq3YDud1dA)
- [Louis的左桥教学](https://www.youtube.com/playlist?list=PLAmLIbUNCUR_e9lmyvcjAb18qlnJ72hGv)
- [Iuri的Line + Line教学](https://www.youtube.com/watch?v=i9zxR5mkgQs)

适合新手的左桥实例：
- Kavin的一些实例对新手非常友好。它们介绍了最朴实的“方块+一组”系两种策略，而不涉及预控等高级技巧。
  - [Pair + Pair 实例（即文中方法1）](https://www.youtube.com/watch?v=sRTVptb2QrY)
  - [Square + Pair 实例（即文中方法2）](https://www.youtube.com/watch?v=YyY_okZ5Fj0)


在我们结束解法篇之前，请留意左桥解法的规划无非是“解法”与“跟踪”这两方面。其中尤以解法更为重要一些。现在，你只需关注把解法做对就行，我们会在本页最后细讲跟踪。 

### 第二步：提升解法

接下来，你要进一步地提升解法。可以在以下几个方面做改进（不分顺序）。精简高效的解法不仅做起来更快，从中得到的求解能力还能帮助你减少观察时间。

- 预控 (Influencing)
    - 定义：通过上一阶段的解法选择来“预先控制”下一阶段，从而实现优化整体解法的技术
    - 无论是方块+一组，还是三三法，都属于两阶段的解法。前者先做方块，再做一组。后者先做E层三块，再做D层三块。预控的意义是，我们要找到阶段一（方块或E层三块）的另解，以优化阶段二（后一组或D层三块）的情况。
    - 换言之，就是改变你原先的阶段一解法，让阶段二比不预控时更好，这样整体解法就更好。 
    - 总体上，预控有以下手段：
      1. 换一个解法来解决阶段一。见于[例1](#inf1) 和[例2](#inf2).
      2. 在已有的阶段一解法上插步。（插入用来预控的转动）
    - 通过预控，我们可以移动第二阶段的块，达到以下目的之一：
      1. 使得这些块有更好的朝向。在大多数的实例中皆是如此。
      2. 使得这些块不会被阶段一的解法所扰乱。比如阶段二的块原本就朝向或相对位置很好，那么阶段一的解法就不应该扰动这些块，以免破坏这些好的特征。 见于[例3](#inf3)。
    - 一般来讲，在阶段一的解法中，总有阶段二的某一个块（棱或角）是无法预控，或不值得去预控的。我们只需预判这个无法预控的块，在阶段一结束后所在的位置。 Predict where the uninfluencable piece will end up after the first stage, and attempt to influence the influencable piece to improve the second stage case.
    - Your influencing moveset will be restricted in some way so it doesn't affect your first stage solution, so visualise the effect of moves within this moveset on influencable pieces to figure out your influencing moves (if any).
    - Note that influencing is not always applicable or necessary.

### 理解棱角对的相对位置和组对思路
为了在解法中加入预控，
理解左桥棱角对所处位置，和对应的组对解法的思路，是非常关键的。
This is crucial for understanding many of the influencing solutions and determining how to solve second stage after predicting first stage.

The minimum information needed to know how to solve a FB pair:
- FB pair's edge position and orientation
- FB pair's corner's position and location of its D-face sticker

For example, if the front pair's corner is on the `U` layer with its D-face sticker also on the `U` layer, then to have the corner be in the same alignment with its edge (such that when they're adjacent, they form a correctly connected pair):
- the edge can be placed in FR in an orientation such that it is an `F2` from being solved.
- the edge can be placed misoriented in its solved position (FL).
- the edge can be placed in BR such that the edge will be solved with `R2 F2`.

These relations can be understood through experience and observation. Using a trainer as well as always observing the aforementioned minimum information of an FB pair before solving it helps.

The above logic can be applied to line solutions as well, especially with understanding how to pair the DL edge with an FB corner to build the D-line. For example:
- DL edge is in DF, and is a `D'` move away from being solved.
- FB's front corner is in UFR, with its D-face sticker on the R layer.
- Thus, the corner can be connected with the DL edge using `R U R'`.

### Step II: Improve Your Solutions

Next, you want to improve your solutions. There are several aspects you can work on, in no particular order. Not only are easier solutions faster to execute, but the ability to come up with them will also help bring down your inspection time.

- Influencing
    - `square + pair` and `line + line` are both two-stage solutions, and the point is we want to find alternative ways to solve the first stage i.e. `square`/`E-line` so we get a better second stage case i.e. `pair`/`D-line`, respectively. [^1]
    - Influencing involves altering your initial first stage solution so that the second stage case is better than without any influencing, and your overall FB solution is also better.
    - In general, influencing can be one of the following:
      1. Solving the same first stage differently for a better second stage, as seen in [example 1](#inf1) 
      and [example 2](#inf2).
      2. Adding influencing moves to an already existing first stage solution.
    - Influencing moves can be used to move second stage pieces with 2 different intents:
      1. So that they'll be affected by first stage solution moves to achieve better orientation, 
      as seen in the majority of examples.
      2. So that they won't be affected by first stage solution moves, such as when second stage pieces are in a good orientation or alignment (either before or after first stage), and first stage ruins that characteristic, as seen in [example 3](#inf3).
    - Typically in first stage solutions, one of the final pieces of the second stage (edge or corner) cannot 
    be influenced, or is not worth influencing. Predict where the uninfluencable piece will end up after the first stage, and attempt to influence the influencable piece to improve the second stage case.
    - Your influencing moveset will be restricted in some way so it doesn't affect your first stage solution, so visualise the effect of moves within this moveset on influencable pieces to figure out your influencing moves (if any).
    - Note that influencing is not always applicable or necessary.

Influencing examples:

**Example 1:**
<div id="inf1">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U2 R B2 U' F2")
    ('#inf1');
</script>

`U r B'` builds the back square. 

However, `U2 R B2` as a first stage solution leads to a much shorter second stage solution.
</div>

**Example 2**
<div id="inf2">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("D' r' U R2 B2 D'")
    ('#inf2');
</script>

`D' M U R2` builds the D-line, although the final piece of E-line (BL) is in a bad position.

Using `r'` instead of `M` leverages the `R2` to orient BL for an easy `B2` insertion.
</div>

**Example 3**
<div id="inf3">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("M' F2 M2 D'")
    ('#inf3');
</script>

`F2` builds the E-line, with DL being misoriented in the D-line.

Starting with `M'` causes DL to not be affected by the `F2`, and become aligned with the D-line
after the first stage.
</div>

**Example 4**
<div id="inf4">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("R' B U2 F2")
    ('#inf4');
</script>

`B` builds the back square.

Starting with `R'` sets up a much easier last pair solution.

Additionally, `R B M2 F` is another FB solution with influencing.
</div>

**Example 5**
<div id="inf5">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("F D R2 F2")
    ('#inf5');
</script>

`D` builds the back square.

Starting with `F` leverages the `D` to connect the front pair's corner with its edge.
</div>

**Example 6**
<div id="inf6">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U2 F R2 B'")
    ('#inf6');
</script>

`F` builds the front square.

Starting with `U2` leverages the `F` to align the back pair's corner with its edge.
</div>

**Example 7**
<div id="inf7">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U2 L2 D' B")
    ('#inf7');
</script>

`L2 D'` builds the front square.

Starting with `U2` leverages the `L2` to connect the back pair's corner with its edge.
</div>

**Example 8**

<div id="inf8">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("L B' D M F")
    ('#inf8');
</script>

`B' D` builds the back square.

Starting with `L` leverages the `D` to align the front pair's corner with its edge.
</div>

**Example 9**
<div id="inf9">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("B' L' B2 D2")
    ('#inf9');
</script>

`L' B2` builds the bottom line of FB and solves the blue-red edge.

Starting with `B'` leverages the `B2` to also insert the back edge, for a `line + line` block.
</div>

**Example 10**
<div id="inf10">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U R' D F' r' F")
    ('#inf10');
</script>

`R' D` builds the back square.

Starting with `U` leverages the `R'` to align the front pair's edge with its corner, 
building the front pair after the `D`.
</div>

**Example 11**
<div id="inf11">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("R D B M F'")
    ('#inf11');
</script>

`D B` builds the back square.

Starting with `R` leverages the `B` to align the front pair's edge with its corner.
</div>

**Example 12**
<div id="inf12">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U2 F D' R' F")
    ('#inf12');
</script>

`F D'` builds the back square.

Starting with `U2` leverages the `F` to align the front pair's corner to its edge after the edge moves from the `D'`.
</div>

**Example 13**
<div id="inf13">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("R F' D R' U' B")
    ('#inf13');
</script>

`F' D` builds the front square. 
Back pair's corner is clearly uninfluencable, so predict the back pair's corner's position and orientation, and then aim to influence the back pair's edge. 

We can predict the back pair's corner will be at DBR after first stage, with its D-face sticker on the bottom. 

We should know from experience that the back pair's edge needs to be misoriented in BR to pair with the back pair's corner when the back pair's corner is in DBR with its D-face sticker on the bottom.

Thus, starting with `R` connects the back pair's edge and corner after first stage, for an easy 3 move second stage.
</div>

**Example 14**
<div id="inf14">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("D' L B' D R' F")
    ('#inf14');
</script>

`D' B' D` builds the back square.

Adding an `L` after the `D'` leverages the `D` to align the front pair's edge with its corner.
</div>

**Example 15**
<div id="inf15">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("B' F' U F' R B2")
    ('#inf15');
</script>

`F' U F'` builds the front square.

Starting with `B'` leverages the `U` to align the back pair's corner to its edge, and pairs them after the final `F'`.
</div>

**Example 16**
<div id="inf16">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U' L' U2 L D B2")
    ('#inf16');
</script>

`L' U L D` builds the front square.

During the `L'` move, the final pair's corner is `U2` away from being connected with its edge.

Starting with `U'` makes us do that desired `U2` after the `L'` to insert the front pair's edge whilst
connecting the back pair's corner with its edge.
</div>

**Example 17**
<div id="inf17">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .case("U2 r U' M2 D' B")
    ('#inf17');
</script>

`r U' M2 D'` builds the front square. Back pair's edge can be predicted to be only a `B` move away from being solved after first stage. Without influencing, the second stage solution is 3 moves.

In an attempt to influence, we can try seeing the effect of specific `U` moves before first stage on the back pair's corner (`U` chosen as it doesn't affect first stage, rather than some `B` move):
- `U` leads to the back pair's corner being aligned with its edge after first stage, but this is still a 3 move second stage solution, so overall solution is longer.
- Similarly with `U'`, we have a 3 move second stage solution, so overall solution is longer.
- But with `U2`, the back pair's corner will be in ULF with its D-face sticker on the L face; this means it's a `B` move away from being solved, like the back pair's edge, and thus results in a 1 move second stage solution, saving 1 move overall.

Thus, start with a `U2`.

Note that this solution may have been harder to figure out if we tried `R U' M2 D'` to build the front square.

</div>

- Optimize your Last Pair solution
    - FB last pair has lots of cases and elegant solutions that can escape your notice. Drill on these in the following ways: use trainers to get random cases and reference the solutions; do untimed solves and experiment around with different ways to solve the same LP case.

- Watch Example Solves
    - Trainers can only help you so far -- example FB solves remain the best way to learn new ideas. Either watch example solves or go over text reconstructions.

- Develop a Taste for good FB / FS
    - Taste is about being able to tell an easy FB from a hard one quickly without fully planning it out. This would help you take advantage of all the FB options given by your orientation.

Videos:
- Kian's Example Solves

Reconstructions (text):
- Search for Kian, Alex or Sean's solves on speedcubing databases:
    - [SpeedCubeDB](http://speedcubedb.com/r/index/) - a modern database, roux solves yet to be added
    - [CubeSolves](http://cubesolv.es) - plenty of solves, but no longer maintained
- More reconstructions can be found on [Anto's subreddit](https://www.reddit.com/r/rouxles/)

## Turning

- You want to have calm and fluid turning for two reasons:
    - You need to give yourself time to track SB pieces, and turning too fast can result in losing track of pieces.
    - FB is a bad moveset group that generally involve both F and B moves. It is intrinsically more difficult to fingertrick. If you rush, you could overshoot or get your grips wrong, resulting in bad lockups.

-  Plan out your fingertricks in inspection too:
   - Unlike the rest of the solve, FB fingertricking requires your active attention. You should limit your regrips and eliminate pauses between moves. Try to figure all these out in inspection --- This can be just as important as planning out the actual solution! Over time, you'll grow familiar and be able to plan fingertricks automatically.

- Also, develop a preference for what pairs / triggers are easy for you to execute over time, and try to prioritize them in your FB solution. Use this to guide your FB planning instead of move count as this is more precise and correlated to actual times.

## FB Planning / Piece Tracking

- If you cannot plan FB entirely, try to plan FS first.
- Planning LP:
    - Only need to calculate:
        - The edge's position and orientation after FS.
        - The corner's position and location of its D-face sticker (white or yellow if x2y) after FS.
    - From the above information, one should be able to determine the LP case and solve accordingly.
    - For example, if the LP edge (where LP is the front pair) is an F move from being solved, the LP corner can be placed at DFR with its D-face sticker on the R face to solve LP with an F move.
    - If you calculate that the LP case is bad or mediocre, then try to influence.
- Similar logic applies with planning FB line solutions or two-stage solutions in general:
    1. Determine solution for the first stage.
    2. Calculate required position/orientation information of second stage pieces.
    3. Attempt influencing for better overall FB, factoring in fingertrickiness.
    4. Execute!
- [Tracking Trainer by Zhouheng](http://onionhoney.github.io/roux-trainers/#tracking)
- [Partial SpeedBLD technique by Kian](https://www.youtube.com/watch?v=4KLFyN6ZDwk) - This is arguably underrated as a practice approach. You should try to do them regularly as warmup before solves.

[^1]: The "line + line" strategy refers to two lines: E-line (2 edges and 1 center on the E slice) and D-line (1 edge and 2 corners on the D slice). E-lines are usually formed first.
