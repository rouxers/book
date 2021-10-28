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

This stage of recognition eliminates the need to peek or rotations, because here you can recognize the CMLL case from any angle. 

For "H" and "Pi" CMLL cases, this should be effortless, since all the colors of the corners is already visible on the top face.

To address the other cases, inference can be very helpful. Note that on the four corner pieces, there are only a total of two stickers for each color (red, orange, blue, and green, assuming white and yellow is top and bottom). Based on this, you can infer that a sticker you cannot see is impossible to have a certain color, due to you already being able to see that color twice on the stickers that are visible to you. 

<div id="inf1">
<script type="text/javascript">
  TTk.InteractivePuzzle(3)
    .size({width:400, height:400})
    .fc('wttwttwtttttttttttrttrttttttttttttttbbbbbbtttttottottt')
    .rotate(true)
		.mouse(false)
		.keyboard(false)
    ('#inf1');
</script>


## Algorithms Resources - 2H

## Algorithms Resources - OH

## Turning

## Predicting CMLL from SB last slot

## Predicting EO from CMLL

## Predicting LR Edges from CMLL

## CMLLEO / Pinkie Pie / L10P Variants