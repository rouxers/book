<script type="text/javascript" src="twistysim.js"></script>
<style type="text/css" rel="stylesheet">
/* modifies the opacity of the cube wireframe */
.ttk-shp-poly {
    stroke-opacity: 0.3;
}
</style>

# LSE

## Regular EOLRb insertions
TODO

<div id="lrMatchingCorners">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("M' U2 M' U")
    ('#lrMatchingCorners');
</script>

## EOLRb 4C Non-Cycle Influencing

The following solutions are for specific cases where 4C will be a non-cycle case. Influencing begins when EO is solved, and involves inserting LR edges in a non-typical fashion. 

For cases **not shown**, one should:
- insert LR edges in the normal way (as shown above)
- or for swapping the upper layer LR edge with the edge below it (to get both LR edges on the bottom), do an `M/M'` move to keep that LR edge on top, then a `U2`, then the opposite of the first `M/M'` move. The solutions below typically do the opposite of this.

The solutions either:
- skip the dots case, resulting in a 4C skip,
- or end up with a 2 or 3 mover 4C (`U2 M2` or `M2 U2 M2`) instead of some 5 mover (e.g. `M' U2 M2 U2 M`), after AUF'ing when EOLRb is solved.

Either way, they're more efficient.

The cases are quite easy to recognise by only looking at the U-face colors and pattern; form your own recognition methods.

**DFDB in ULUR:**
<div id="dfdb_in_ulur">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("M U2 M U' M2 U")
    ('#dfdb_in_ulur');
</script>

</div>

**2 D-stickers on M slice and U layer**
<div id="twoDstickersOnTop">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("M U2 M U' M2' U M2' U2")
    ('#twoDstickersOnTop');
</script>

</div>

**Dots Skip 1**
<div id="dotsSkip1">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("U' M' U2 M2 U2 M' U")
    ('#dotsSkip1');
</script>

</div>

**Dots Skip 2**
<div id="dotsSkip2">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("U' M' U2 M2 U2 M' U M2")
    ('#dotsSkip2');
</script>

Note: Less efficient than inserting normally and solving dots with `E2`, but you may prefer this.
</div>

**Dots Skip 3**
<div id="dotsSkip3">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("M U2 M U2 M2 U'")
    ('#dotsSkip3');
</script>

The DFDB edge on top (blue white edge in this case) is adjacent to the center of the opposite color (green).
</div>

**Dots Skip 4**
<div id="dotsSkip4">
<script type="text/javascript">
  TTk.AlgorithmPuzzle(3)
    .size({width:400, height:400})
    .case("M' U2 M U2 M2 U'")
    ('#dotsSkip4');
</script>

The DFDB edge on top (green white edge in this case) is adjacent to the center of the opposite color (blue).
</div>

## 3-look vs. EOLR: better switch late than early

## 3-look Progression

## EOLR Progression

It is not recommended to memorize algsheets for EOLR.
Learn from text descriptions below:

- [EOLR Described](https://docs.google.com/document/d/1dvGERLfN-0rVwN914HH1zRPHLfdM6d5rPfe0HxOMK08/edit)
- [EOLR Described](https://docs.google.com/document/d/1rb5M9_5CTlozLu9acFIgqq9LYYKaUdnMDX0vcLOURT4/edit])
- (TODO: what's their difference? )

### MC vs. Non-MC: better early than late

### Should I add EOBF on top of EOLR?

## 4c Prediction: battle of recog methods

## Turning and Fingertrick - 2H

## Turning and Fingertrick - OH
