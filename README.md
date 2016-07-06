# CSS experiments

## CSS only rotating cube I

This is just a simple css only rotating cube for studying purposes.

## Demo

View demo on CodePen: https://codepen.io/marcus_kober/pen/NAvWjb

## HTML

In HTML we need a scene to which we can apply the perspective and the cube with it's 6 sides:

```html
<div class="scene">
    <div class="cube">
        <div class="cube--side back">back</div>
        <div class="cube--side left">left</div>
        <div class="cube--side right">right</div>
        <div class="cube--side bottom">bottom</div>
        <div class="cube--side top">top</div>
        <div class="cube--side front">front</div>
    </div>
</div>
```

## CSS

Some of the key properties explained.

The perspective property defines the number of pixels the 3D element is viewed from. It's important to play with this property as it defines the overall look of your 3D object.

```css
.scene {
    perspective: 1800px;
}
```

The cube should not look flat, so the transform-style property needs to be set to preserve-3d. Set to preserve-3d the elements are stacked according to the translateZ values.

```css
.cube {
    transform-style: preserve-3d;
}
```

Now we need to rotate the sides of the cube to the correct positions in 3D space:

```css
.back {
    transform: translateZ(-150px) rotateX(180deg);
}

.front {
    transform: translateZ(150px);
}

.left {
    transform: translateX(-150px) rotateY(270deg);
}

.right {
    transform: translateX(150px) rotateY(90deg);
}

.top {
    transform: translateY(-150px) rotateX(90deg);
}

.bottom {
    transform: translateY(150px) rotateX(270deg);
}
```

Note that the sides back, left and bottom are flipped so that the text on the sides is displayed correctly.