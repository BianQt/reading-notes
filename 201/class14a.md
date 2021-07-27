# Transforms 
The transform property applies a 2D or 3D transformation to an element. This property allows you to rotate, scale, move, skew, etc., elements.

## Transform Syntax#transform-syntax
The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```
## 2D Transforms
CSS transforms allow you to move, rotate, scale, and skew elements.
### CSS 2D Transforms Methods
With the CSS transform property you can use the following 2D transformation methods:

* ```translate()```
* ```rotate()```
* ```scaleX()```
* ```scaleY()```
* ```scale()```
* ```skewX()```
* ```skewY()```
* ```skew()```
* ```matrix()```
 ## CSS 3D Transforms
CSS also supports 3D transformations.
### CSS 3D Transforms Methods
With the CSS transform property you can use the following 3D transformation methods:

* ```rotateX()```
* ```rotateY()```
* ```rotateZ()```

# Transitions & Animations
Transitions are the grease in the wheel of CSS transforms. Without a transition, an element being transformed would change abruptly from one state to another. By applying a transition you can control the change, making it smooth and gradual. 

## Transitions
CSS transitions allows you to change property values smoothly, over a given duration.

## How to Use CSS Transitions?
To create a transition effect, you must specify two things:
###
the CSS property you want to add an effect to
the duration of the effect.
###
The following example shows a 100px * 100px red ```<div>``` element. The ```<div>``` element has also specified a transition effect for the width property, with a duration of 2 seconds:

### Example
```div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}
```

The transition effect will start when the specified CSS property (width) changes value.
### 
Now, let us specify a new value for the width property when a user mouses over the ```<div>``` element:

### Example
```div:hover {
  width: 300px;
}
```

## CSS Animations
CSS allows animation of HTML elements without using JavaScript or Flash!

## What are CSS Animations?
An animation lets an element gradually change from one style to another.

You can change as many CSS properties you want, as many times as you want.

To use CSS animation, you must first specify some keyframes for the animation.

Keyframes hold what styles the element will have at certain times.

## The @keyframes Rule
When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.

To get an animation to work, you must bind the animation to an element.
### 
The following example binds the "example" animation to the ```<div>``` element. The animation will last for 4 seconds, and it will gradually change the background-color of the ```<div>``` element from "red" to "yellow":

### Example
```/* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```