<script type="text/javascript" src="twistysim.js"></script>
<style type="text/css" rel="stylesheet">
/* modifies the opacity of the cube wireframe */
.ttk-shp-poly {
    stroke-opacity: 0.3;
}
</style>

# First Block

## Solution

### Step I: Basic Blockbuilding Strategies

Transitioning from the beginner method of edge loading spots, you should be aware of different blockbuilding strategies. There are broadly speaking two families of FB building strategy: `square + pair` and `line + line`, with the first one being more frequently used.

It is recommended to watch videos on blockbuilding strategies and have a basic understanding before you proceed to example solves.

Overall strategy:
- [Finding an Efficient FB in Inspection](https://www.youtube.com/watch?v=0Cq3YDud1dA)
- [Louis' First Block Tutorial](https://www.youtube.com/playlist?list=PLAmLIbUNCUR_e9lmyvcjAb18qlnJ72hGv)
- [Iuri's Line + Line first block](https://www.youtube.com/watch?v=i9zxR5mkgQs)

Beginner-friendly Example Solves:
- Kavin's Example Solves.
  - [Pair + Pair Example Solves](https://www.youtube.com/watch?v=sRTVptb2QrY)
  - [Square + Pair Example Solves](https://www.youtube.com/watch?v=YyY_okZ5Fj0)
  - These illustrate pure `square + pair` FB building -- they don't involve advanced stuff like influencing.

### Relationship to Planning
Before we go on, note that `planning = solution + tracking`, with solution playing perhaps a more important role. For now stay tuned on getting your solutions right, and we'll cover tracking in the last section.

## Understanding relation of each FB pair's pieces and how they can be solved
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
- [Partial SpeedBLD technique by Kian](https://www.youtube.com/watch?v=4KLFyN6ZDwk) - This is arguably underrated as a practice approach. You should try to do them regularly as warmup before solves.

[^1]: The "line + line" strategy refers to two lines: E-line (2 edges and 1 center on the E slice) and D-line (1 edge and 2 corners on the D slice). E-lines are usually formed first.
