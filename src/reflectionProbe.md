# Create reflectionProbe (TODO)

TODO : obselete, this should be review...

Reflection probes are used to dynamically generate cube maps that can the be used as reflection textures for instance

[How to use Reflection Probes](https://doc.babylonjs.com/how_to/how_to_use_reflection_probes)


## Example
```json
[
  { 
    "material.000" : {
      "reflectionTexture" : {
        "texture::reflectionProbe" : {
          "renderList" : [ "yellowSphere", "GreenSphere"]
        }
      }
    }
  }
]
```

## from _r 

| Parameters | Optional | Type | Default |
| ---------- |:--------:|:----:|:-------:|
| name | x | String |_r.reflectionProbe.00X | 
| size | x | Number | 512 |
| renderList | x | Array[String] | all meshes in current scene |
| attachToMesh | x | String | null |
| generateMipMaps | x | Boolean | null | 
| invertYAxis | x | Boolean | false |
| position | x | _r.Vector3 | [0, 0, 0] |
| samples | x | String or number | |

### attachToMesh or position

### samples
Could be a string or a number 
* string :
    * 'once'
    * 'everyframe'
    * 'everytwoframes' 
* number : 
    * BABYLON.RenderTexture.REFRESHRATE_RENDERONCE
    * BABYLON.RenderTexture.REFRESHRATE_RENDER_ONEVERYFRAME
    * BABYLON.RenderTexture.REFRESHRATE_RENDER_ONEVERYTWOFRAMES  




