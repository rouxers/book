<script type="text/javascript" src="twistysim.js"></script>
<style type="text/css" rel="stylesheet">
/* modifies the opacity of the cube wireframe */
.ttk-shp-poly {
    stroke-opacity: 0.3;
}
</style>

# CMLL

## Recognition Method: From beginner's 4-tile to all angles

CMLL recognition is a little more tricky than something like OLL. Not only does one have to pay attention to the orinetation of the corners, one also has to pay attention to their colors. Despite that, an advanced Roux solver is able to recognize the CMLL case within fractions of a second. Here is the progression towards that.

### I. Beginner Recognition

A beginner most likely uses 2-look CMLL, so it is mostly irrelevant for them to pay attention to the colors of the corners. It is adequate to simply get used to recognizing the orientation of the corners.

Practice recognizing the corner orientations fast - this will definitely come in handy later on.

### II. Partial/Full CMLL and Peeking

Now that you have learned specific cases of CMLL, you are forced to pay attention to the colors of the corners. Practice recognizing these cases too. In addition, make sure you know beforehand which angles you should rotate to in order to see the corner colors. Keep in mind, you are only rotating the with `U` moves, not full cube rotations.

Rotations in recognition can be easily reduced by knowing how to peek to the side. Peeking is when you are 90&deg; off from an angle where you can see all corner colors, you slightly tilt your cube to the left/right to see them. This can save at least one move.

It is perfectly fine to stick with this recognition method. It will give you good company on your way to sub-12, sub-10, or even beyond. 

### III. All Angles Recognition

This stage of recognition eliminates the need to peek or rotate by recognizing cases from every angle.

For "H" and "Pi" CMLL cases, this should be effortless, since all the colors of the corners is already visible on the top face.

For the other cases, a combination of the following is used:
- Inferring the color of the stickers you cannot see
- Knowing the color patterns of cases very well

It is important to note that on the four corner pieces, there are only a total of two stickers for each color (red, orange, blue, and green, assuming white and yellow is top and bottom). There is also a limited number of combinations of colors on each corner; that is, only adjacent colors appear on one corner piece. 

Based on these properties, we may deduce the color of stickers we cannot see and take advantage of the unique color patterns that are formed. 

Here is an example trying to recognize a "U" case from the given angle:

<div id="inf1">
  <script type="text/javascript">
    var cube = TTk.InteractivePuzzle(3)
      .size({width:400, height:400})
      .fc('wdwwdwwdwggggggrdordrrdrydybdgdddydybbbbbbodrodoodobdg');
    cube.moveInteract()
      .mouse(false)
      .keyboard(false);
    cube("#inf1");
  </script>
</div>

From here we can only see blue and green stickers from the top and the red and orange stickers on the side, but that is enough to tell us exactly which CMLL case this is:
1. We notice that the two colors on the top, blue and green, are opposite to each other. Using our knowledge of unique color patterns, this brings us down to two possibilities: The ["X"](https://speedcubedb.com/a/3x3/CMLL/U_X) and ["Bottom Row"](https://speedcubedb.com/a/3x3/CMLL/U_Bottom_Row) U cases.
2. We see that one corner in the back has an orange color on it, so we can infer that the other non-yellow color on that corner has to be blue or green.
3. Out of the two possibilities, only the "X" case has colors at the back that are adjacent/opposite to the two colors on the top. Here we have blue and green on the top, and we concluded that a sticker on the back must be blue or green, therefore we must have the "X" case here.

Rotate the visual cube to check if we're right.

With enough practice, this thought process will become automatic. But where do we find all the "patterns" that we should know in order to get a case down to two possibilities? [Kian's comprehensive guide on this topic will be your best friend](https://www.youtube.com/watch?v=MKZ7JX-hW4g).

## Algorithms Resources - 2H

## Algorithms Resources - OH

## Turning

## Predicting CMLL from SB last slot

## Predicting EO from CMLL

## Predicting LR Edges from CMLL

## CMLLEO / Pinkie Pie / L10P Variants