# Scripting Camera

## Activate camera

```js
_r.camera.activate("Camera.FPV");
```

## Go somewhere with animation

```js
 _r.camera.goTo({ x : 0, y : 0, z : 0})
```

### Position & Rotation

```js
_r.camera.goTo({ x : 0, y : 0, z : 0}, { x : 0, y : Math.PI, z : 0})
```

### Position, Rotation & animation duration

Duration in seconds 
```js
 _r.camera.goTo({ x : 0, y : 0, z : 0}, null, 4)
```

### Animations options

```js
_r.camera.goTo({ x : 0, y : 0, z : 0}, { x : 0, y : Math.PI, z : 0}, {
    duration : 3,
    easing : "easeInSine",
    complete : function() {
        console.log("animation completed")
    }
})
```
For more animation options see [animations chapter](animation-scripting.md).