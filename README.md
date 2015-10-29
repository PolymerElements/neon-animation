
<!---

This README is automatically generated from the comments in these files:
neon-animatable-behavior.html  neon-animatable.html  neon-animated-pages.html  neon-animation-behavior.html  neon-animation-runner-behavior.html  neon-animation.html  neon-animations.html  neon-shared-element-animatable-behavior.html  neon-shared-element-animation-behavior.html  web-animations.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

-->

_[Demo and API Docs](https://elements.polymer-project.org/elements/neon-animation)_


##&lt;cascaded-animation&gt;


`<cascaded-animation>` applies an animation on an array of elements with a delay between each.
the delay defaults to 50ms.

Configuration:
```
{
  name: 'cascaded-animation',
  animation: <animation-name>,
  nodes: <array-of-nodes>,
  nodedelay: <node-delay-in-ms>,
  timing: <animation-timing>
}
```


##&lt;fade-in-animation&gt;


`<fade-in-animation>` animates the opacity of an element from 0 to 1.

Configuration:
```
{
  name: 'fade-in-animation',
  node: <node>
  timing: <animation-timing>
}
```


##&lt;fade-out-animation&gt;


`<fade-out-animation>` animates the opacity of an element from 1 to 0.

Configuration:
```
{
  name: 'fade-out-animation',
  node: <node>
  timing: <animation-timing>
}
```


##&lt;hero-animation&gt;


`<hero-animation>` is a shared element animation that scales and transform an element such that it
appears to be shared between two pages. Use this in `<neon-animated-pages>`. The source page
should use this animation in an 'exit' animation and set the `fromPage` configuration property to
itself, and the destination page should use this animation in an `entry` animation and set the
`toPage` configuration property to itself. They should also define the hero elements in the
`sharedElements` property (not a configuration property, see
`Polymer.NeonSharedElementAnimatableBehavior`).

Configuration:
```
{
  name: 'hero-animation',
  id: <shared-element-id>,
  timing: <animation-timing>,
  toPage: <node>, /* define for the destination page */
  fromPage: <node>, /* define for the source page */
}
```


##&lt;neon-animatable&gt;


`<neon-animatable>` is a simple container element implementing `Polymer.NeonAnimatableBehavior`. This is a convenience element for use with `<neon-animated-pages>`.

```
<neon-animated-pages selected="0"
                     entry-animation="slide-from-right-animation"
                     exit-animation="slide-left-animation">
  <neon-animatable>1</neon-animatable>
  <neon-animatable>2</neon-animatable>
</neon-animated-pages>
```


##&lt;neon-animated-pages&gt;


Material design: [Meaningful transitions](https://www.google.com/design/spec/animation/meaningful-transitions.html)

`neon-animated-pages` manages a set of pages and runs an animation when switching between them. Its
children pages should implement `Polymer.NeonAnimatableBehavior` and define `entry` and `exit`
animations to be run when switching to or switching out of the page.



##&lt;opaque-animation&gt;


`<opaque-animation>` makes an element `opacity:1` for the duration of the animation. Used to prevent
webkit/safari from drawing a frame before an animation for elements that animate from display:none.


##&lt;reverse-ripple-animation&gt;


`<reverse-ripple-animation>` scales and transform an element such that it appears to ripple down from this element, to either
a shared element, or a screen position.

If using as a shared element animation in `<neon-animated-pages>`, use this animation in an `exit`
animation in the source page and in an `entry` animation in the destination page. Also, define the
reverse-ripple elements in the `sharedElements` property (not a configuration property, see
`Polymer.NeonSharedElementAnimatableBehavior`).
If using a screen position, define the `gesture` property.
Configuration:
```
{
  name: 'reverse-ripple-animation`.
  id: <shared-element-id>, /* set this or gesture */
  gesture: {x: <page-x>, y: <page-y>}, /* set this or id */
  timing: <animation-timing>,
  toPage: <node>, /* define for the destination page */
  fromPage: <node>, /* define for the source page */
}
```


##&lt;ripple-animation&gt;


`<ripple-animation>` scales and transform an element such that it appears to ripple from either
a shared element, or from a screen position, to full screen.

If using as a shared element animation in `<neon-animated-pages>`, use this animation in an `exit`
animation in the source page and in an `entry` animation in the destination page. Also, define the
hero elements in the `sharedElements` property (not a configuration property, see
`Polymer.NeonSharedElementAnimatableBehavior`).

If using a screen position, define the `gesture` property.

Configuration:
```
{
  name: 'ripple-animation`.
  id: <shared-element-id>, /* set this or gesture */
  gesture: {x: <page-x>, y: <page-y>}, /* set this or id */
  timing: <animation-timing>,
  toPage: <node>, /* define for the destination page */
  fromPage: <node>, /* define for the source page */
}
```


##&lt;scale-down-animation&gt;


`<scale-down-animation>` animates the scale transform of an element from 1 to 0. By default it
scales in both the x and y axes.

Configuration:
```
{
  name: 'scale-down-animation',
  node: <node>,
  axis: 'x' | 'y' | '',
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;scale-up-animation&gt;


`<scale-up-animation>` animates the scale transform of an element from 0 to 1. By default it
scales in both the x and y axes.

Configuration:
```
{
  name: 'scale-up-animation',
  node: <node>,
  axis: 'x' | 'y' | '',
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;slide-down-animation&gt;


`<slide-down-animation>` animates the transform of an element from `translateY(-100%)` to `none`.
The `transformOrigin` defaults to `50% 0`.

Configuration:
```
{
  name: 'slide-down-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;slide-from-left-animation&gt;


`<slide-from-left-animation>` animates the transform of an element from
`translateX(-100%)` to `none`.
The `transformOrigin` defaults to `0 50%`.

Configuration:
```
{
  name: 'slide-from-left-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;slide-from-right-animation&gt;


`<slide-from-right-animation>` animates the transform of an element from
`translateX(100%)` to `none`.
The `transformOrigin` defaults to `0 50%`.

Configuration:
```
{
  name: 'slide-from-right-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;slide-left-animation&gt;


`<slide-left-animation>` animates the transform of an element from `none` to `translateX(-100%)`.
The `transformOrigin` defaults to `0 50%`.

Configuration:
```
{
  name: 'slide-left-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;slide-right-animation&gt;


`<slide-right-animation>` animates the transform of an element from `none` to `translateX(100%)`.
The `transformOrigin` defaults to `0 50%`.

Configuration:
```
{
  name: 'slide-right-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;slide-up-animation&gt;


`<slide-up-animation>` animates the transform of an element from `translateY(0)` to
`translateY(-100%)`. The `transformOrigin` defaults to `50% 0`.

Configuration:
```
{
  name: 'slide-up-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  timing: <animation-timing>
}
```


##&lt;transform-animation&gt;


`<transform-animation>` animates a custom transform on an element. Use this to animate multiple
transform properties, or to apply a custom transform value.

Configuration:
```
{
  name: 'transform-animation',
  node: <node>,
  transformOrigin: <transform-origin>,
  transformFrom: <transform-from-string>,
  transformTo: <transform-to-string>,
  timing: <animation-timing>
}
```


##Polymer.NeonAnimatableBehavior


`Polymer.NeonAnimatableBehavior` is implemented by elements containing animations for use with
elements implementing `Polymer.NeonAnimationRunnerBehavior`.


##Polymer.NeonAnimationBehavior


Use `Polymer.NeonAnimationBehavior` to implement an animation.


##Polymer.NeonAnimationRunnerBehavior


`Polymer.NeonAnimationRunnerBehavior` adds a method to run animations.



##Polymer.NeonSharedElementAnimatableBehavior


Use `Polymer.NeonSharedElementAnimatableBehavior` to implement elements containing shared element
animations.


##Polymer.NeonSharedElementAnimationBehavior


Use `Polymer.NeonSharedElementAnimationBehavior` to implement shared element animations.

