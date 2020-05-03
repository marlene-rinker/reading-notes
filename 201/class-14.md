## Code 201 Reading Assignment Notes - Class 14

_April 16, 2020_

### What Google Learned
[What Google Learned from Its Quest to Build the Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)

In 2012, Google started Project Aristotle to study hundreds of Google teams to determine why some stumbled while others soared.

They had a lot of data, but couldn't determine any patterns or evidence that the composition of a team made any difference. Even though two teams might have a similar makeup, one could be very effective while the other one wasn't.

They came across research that focused on "group norms." These are the traditions, behavioral standards and unwritten rules that govern how we function when we gather.

They concluded that understanding and influencing group norms were the keys to improving Google's teams. They just needed to figure out which norms mattered most.

There were two behaviors that good teams shared:
- members spoke in roughly the same proportion - if everyone had a chance to talk the team did well, but if only one person or a small group spoke all the time, the collective intelligence declined

- all had high "average social sensitivity" - they were sensitive to how others on the team were feeling

These behaviors are aspects of what's known as "psychological safety" which means that you don't feel afraid to speak up, you're able to be yourself, there's a climate of interpersonal trust and respect.

In the best teams, members listen to one another and show sensitivity to feelings and needs.



### CSS Animations

#### CSS Transforms

[CSS Transforms article](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

The `transform` property provides new ways to position and alter elements using CSS3. It has two different settings, 2D and 3D. Each has their own individual properties and values.

Be aware that browser support isn't great for the `transform` property. Use multiple vendor prefixes as the safest approach, with the un-prefixed declaration coming last.

```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

The article has examples of ways to use the `transform` property for both 2D and 3D transforms.

For 3D transforms to work, the elements need  a `perspective` property as well.

#### CSS Transitions and Animations

[CSS Transitions and Animations article](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

**Transitions**

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

For a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes.

There are four transition related properties in total, including `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`. The first three are the most popular.

Only properties that have an identifiable half-way point can be transitioned. The article has a list of these properties.

There is a shorthand property, `transition`, capable of supporting all of the different properties and values. Using the transition value alone, you can set every transition value in the order of `transition-property`, `transition-duration`, `transition-timing-function`, and lastly `transition-delay`. Do not use commas with these values unless you are identifying numerous transitions. Example: `transition: background .2s linear, border-radius 1s ease-in 1s;`

**Animations**


When more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.

To set multiple points at which an element should undergo a transition, use the `@keyframes` rule. The `@keyframes` rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

Just like transitions, animations can be written out in a shorthand format. This is accomplished with one `animation` property, rather than multiple declarations. The order of values within the animation property should be `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode`, and lastly `animation-play-state`.

The article has examples and demos of how to use transitions and animations.

**Examples**

[Eight Simple CSS3 Transitions that will wow your users](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users/)

1. Fade in
2. Change color
3. Grow and shrink
4. Rotate elements
5. Square to circle
6. 3D shadow
7. Swing
8. Inset border

The article has demos and the code for how to do each of these transitions.

[6 Buttons Animated](https://codepen.io/retyui/pen/ByoaXV) - this is a CodePen that shows cool effects you can use on buttons, you can see the HTML and CSS for the buttons.

[CSS Keyframes Animation](https://codepen.io/akshaychauhan/pen/oAfae) - this is a CodePen that shows using keyframes to make a bouncing ball, you can see the HTML and CSS used to create this.

[404](https://codepen.io/kieranfivestars/pen/MYdQxX) - this is a CodePen that shows numbers moving around and resizing on the page, you can see the HTML and CSS used to create this.

[Pure CSS Bounce Animation](https://codepen.io/dp_lewis/pen/gCfBv) - this is a CodePen that shows a bouncing shape and then other shapes appearing, you can see the HTML and CSS used to create this.



---
[Home page](https://marlene-rinker.github.io/reading-notes/)