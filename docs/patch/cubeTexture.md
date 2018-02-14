# CubeTexture

Environment mapping that uses the six faces of a cube as the map shape.

## Resources
* [https://doc.babylonjs.com/classes/2.5/cubetexture](https://doc.babylonjs.com/classes/2.5/cubetexture)
* [https://doc.babylonjs.com/tutorials/advanced_texturing](https://doc.babylonjs.com/tutorials/advanced_texturing)

## In patch

```js
[{
    "scene.cubeMaterial.000" : {
        "reflectionTexture" : {
           "cubeTexture" : {
                "rootUrl": "./assets/cubemap/",
                "coordinatesMode" : "SPHERICAL_MODE"
            }
        }
    }
}]
```
or
```js
[{
    "scene.cubeMaterial.000" : {
        "reflectionTexture" : function() {
            return _r.cubeTexture({
                "rootUrl": "./assets/cubemap/",
                "coordinatesMode" : "SPHERICAL_MODE"
            });
        }
    }
 }]
```

## By code
```js
var cubeTexture = _r.cubeTexture({
  "rootUrl": "./assets/cubemap/",
  "coordinatesMode" : "SPHERICAL_MODE"
});
_r("scene.cubeMaterial.000").attr("reflectionTexture", cubeTexture);
```

## Parameters

### Designers
parameter | required | type | default | description
----------|----------|------|---------|------------
rootUrl          | x  | string           | | Link of the texture
noMipmap         |    | boolean          | false | 
coordinatesMode  |    | string           | 'EXPLICIT_MODE' | 'EXPLICIT_MODE', SPHERICAL_MODE', 'PLANAR_MODE', 'CUBIC_MODE', 'PROJECTION_MODE', 'SKYBOX_MODE', 'INVCUBIC_MODE', 'EQUIRECTANGULAR_MODE', 'FIXED_EQUIRECTANGULAR_MODE'   

### Misc.
parameter | required | type | default | description
----------|----------|------|---------|------------
extensions       |    | string[]                                | | The cube texture extensions. The defaults extensions are : [_px.jpg, _py.jpg, _pz.jpg, _nx.jpg, _ny.jpg, _nz.jpg]
files            |    | string[]                                | | 
onLoad           |    | () => void                              | | Callback
coordinatesMode  |    | number | BABYLON.Texture.EXPLICIT_MODE  | ex : BABYLON.Texture.SPHERICAL_MODE

### Any other parameters...
...will be merged into the texture.

Ex :
```json
[{
    "scene.cubeMaterial.000" : {
        "reflectionTexture" : {
           "cubeTexture" : {
                "rootUrl": "./assets/cubemap/",
                "coordinatesMode" : "SPHERICAL_MODE",
                "level" : 0.5
            }
        }
    }
}]
```