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