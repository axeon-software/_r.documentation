# Texture

## In patch

```js
[{
        "scene.teapotMaterial.000": {
            "diffuseTexture":  {
                  texture : {
                        url: 'assets/checker01.png'
                  }
            }
        }
}]
```
or
```js
[{
        "scene.teapotMaterial.000": {
            "diffuseTexture":  function() {
                return _r.texture({
                      url: 'assets/checker01.png'
                })
            }
        }
}]
```

## By code
```js
var texture = _r.texture({
  url: 'assets/checker01.png'
});
_r("scene.teapotMaterial.000").attr("diffuseTexture", texture);
```

## Parameters

### Designers
parameter | required | type | default | description
----------|----------|------|---------|------------
url              | x  | string           | | Link of the texture
noMipmap         |    | boolean          | false | 
coordinatesMode  |    | string           | 'EXPLICIT_MODE' | 'EXPLICIT_MODE', SPHERICAL_MODE', 'PLANAR_MODE', 'CUBIC_MODE', 'PROJECTION_MODE', 'SKYBOX_MODE', 'INVCUBIC_MODE', 'EQUIRECTANGULAR_MODE', 'FIXED_EQUIRECTANGULAR_MODE'   
invertY          |    | boolean          | false
samplingMode     |    | string           |  | 'NEAREST_SAMPLINGMODE', 'BILINEAR_SAMPLINGMODE', 'TRILINEAR_SAMPLINGMODE'  


### Any other parameters...
...will be merged into the texture.

Ex :
```js
[{
    "scene.teapotMaterial.000": {
        "diffuseTexture":  {
              texture : {
                    "url": 'assets/checker01.png',
                    "level" : 0.5,
                    "coordinatesIndex" : 1,
                    "hasAlpha" : true
              }
        }
    }
}]
```

See :
* [https://doc.babylonjs.com/classes/2.5/basetexture](https://doc.babylonjs.com/classes/2.5/basetexture)
* [https://doc.babylonjs.com/classes/2.5/texture](https://doc.babylonjs.com/classes/2.5/texture)