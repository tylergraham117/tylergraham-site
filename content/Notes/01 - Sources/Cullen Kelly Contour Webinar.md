---
date read: 2024-08-31
tags:
  - source
author:
  - Cullen Kelly
released: 2024-08-31
link: https://app.searchie.io/hub/YoRnaK4jyd/
publish: false
---
# Cullen Kelly Contour Webinar


## What is a look?

Look development and color grading are sort of opposite ends of the process. (Example: Exposure is almost never done in look dev, but is almost always done in grading.)

Guidelines:
- Adjustments should bend, push and bias colors. It should not force, tear, or break them.
- Exposure (middle grey) should not change.
- Neutral should stay neutral.
- The broader the application of the look, the more conservative it should be.
	- Consider the application when you make the look. To avoid breakage but also to make sure it still looks good.

Color management is necessary. Wide Gamut + Intermediate.

Be in an image centric space, not a camera centric one.

Look (Contour) should be immediately upstream of final output.

Try to make your whole look within one node. You can have more than one instance, but its best not to. This is mostly to impose limitations on yourself and encourage a more optimized approach.

You should have a main look, and then potentially sub-looks (maybe for a scene or certain moments in the story).


## Contour Tour

- Unity cube, image within that.
- Contour modules are ordered by priority.
- Contour offers a balance between constraint and control. 
	- This keeps things practically useful. Rather than having unlimited control, we have simplified, useful control.

### Contrast

Our contrast slope has 3 components: Toe, middle, shoulder.

Examples:
- Increase contrast, but soften the toe. (High contrast everywhere except the blacks.)
- Leave contrast, but adjust toe or shoulder. (You can shape your contrast without the contrast slider)
	- White point will adjust brightest part of image.

Preserve color slider changes the amount the curves are applied to different channels. 0 value means its applied to all channels, full 1 means its only applied to Lum channel.

### Split

This lets us bias neutrals into the bottom and top of the image. Shadow hue and highlight hue.

A lot of the split tone sliders allow you to hide your brush strokes. If it's too obvious, its obvious and looks terrible. But the best looking images always have a bit of split toning.
The whole point of split toning is to create color contrast.

Crossover between highlight and shadow is middle grey. Pivot alters this. (Pivot is in stops.)
Pivot is helpful for moving the crossover point to a well lit face in frame, allowing us to actually feel the color contrast.

Lo vs Hi Strength. 
Versus sliders allow us to define relationships.

Hue adjustment will adjust exposure because different hues contain more or less luminance.

Subtractive Lo and Hi. Allows us to adjust the luminance of the split tone curve.
(Cullen likes all the way to 0 sometimes. Why?)

Neutral Segment Width eases the crossover curve between shadow and highlight. Can adjust up to 1/3rd of the curve.

The only difference between beautiful grades and laughable ones is how intense the neutral segment is. If it's too tight, it looks cheesy. Plenty of easing makes it look pleasing lmao.

Curve start and end allow us to create neutral segments at the top and bottom of the curve.

Divergence (Peak and Floor) just keep the tones split all the way throughout rather than coming back together. This is common in film emulations.


> [!question] Sat Mask Slider (Missed this one.) 1:20

Split Strength is usually maxed out around .3/.4

Neutral Segment Width is probably the most effective for keeping split tone out of skin tones, but you can also use Sat Mask or Pivot (depending on how much exposure varies throughout the project.)

### Saturation

The Saturation module is a better version of the Sat vs Sat curve.

Lo, Med, Hi are all Sat inputs.

Saturation usually get's too intense in skin first, so adjusting red and cyan, blue and yellow sliders allows us to avoid skin tones in saturation adjustments. This puts saturation into things like blues and greens.
This works the other way too, when you're going towards a more desaturated look.

Lum Mask limits effect of all saturation adjustments to a range of luminance values.

Cube is helpful in this module.

You can use this for Hue vs Sat also, by selecting the specific Saturation relationship towards the hue we want, then adjust sat. This is a good reason to stack Contour nodes probably.

### Density

Density is Saturation vs Exposure.

This density slider gives us much cleaner density than other tools (Including ColorSlice.)

Focus slider gives us more control. How saturated does something need to be before it receives the exposure adjustment.


### Hue

Hue is a lot like Hue vs Hue, but works more precisely. 
The focus slider takes saturation into account. It doesn't simply move the hue goal posts closer together.


## Cube





**Ways to do sublooks:**
Group post clip
Adjustment layers
Shared node





## Look Development


In Hue, pull greens cooler and yellows warmer helps create more separation. (This was an example. It's based on the color pallet of the image and general art direction)

Sound of Music brings greens towards cyan and yellows warmer.

Cullen likes the grain in the new Film Look Creator. Halation is good too.



Analyze the reference first.


### Past Lives


### The Batman

- Lifted black point.
- Very moody.
- Life in the toe (shadows)
- 


### Dune

- Desaturated look.
- Lots of sub looks based on planet.


### Tokyo Vice

- Big contrast curve
- Big toe
- 




## Rebuilding LUTs

When recreating LUTs, start at middle exposure, then go to shadows, then highlights.

Skin usually lives in the Lo Sat slider of the Saturation module.

When building LUTs, you have to pay attention to color spaces. Make sure input and output are correct. 

Most camera's work with 33 point cubes. Only Alexa's can do more.








Processing order:
Hue, Saturation, Density, Split, Curve




Future of Contour:
- Performance optimization
- Drop down profiles
- Push Pull Module
- DRT Module
- Multiple instances of a module
- Outside inside nodes
- 

