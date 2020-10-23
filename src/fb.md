<script type="text/javascript" src="twistysim.js"></script>

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

### Step II: Improve Your Solutions

Next, you want to improve your solutions. There are several aspects you can work on, in no particular order. Not only are easier solutions faster to execute, but the ability to come up with them so will also help bring down your inspection time.

- Influencing
    - `square + pair` and `line + line` are both two-stage solutions, and the point is we want to find alternative ways to solve the first stage i.e. `square`/`E-line` so we get a better second stage case i.e. `pair`/`D-line`, respectively. [^1]

<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
	.alg("F D R2 F2")
	('#ap1');			
</script>

`
F // set up LP corner to match with edge during the D move
D R2 F2
// without LP influencing, 1 move longer
`

- Optimize your Last Pair solution
    - FB last pair has lots of cases and elegant solutions can escape your notice. Drill on these in the following ways: use trainers to get random cases and reference the solutions; do untimed solves and experiment around with different ways to solve the same LP case

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

(...todo)
- [Partial SpeedBLD technique by Kian](https://www.youtube.com/watch?v=4KLFyN6ZDwk) - This is arguably underrated as a practice approach. You should try to do them regularly as warmup before solves.

[^1]: The "line + line" strategy refers to two lines: E-line (2 edges and 1 center on the E slice) and D-line (1 edge and 2 corners on the D slice). E-lines are usually formed first.
