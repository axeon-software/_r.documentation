# Textures

## Create texture with **texture::base**
```json
[{
     "material1" : {
            "diffuseTexture" : {
                "texture::base" : {
                     "name" : "textureTree", 
                     "url" : "textures/tree.png",
                     "hasAlpha" : true
                }
            }
        }
}]
```

## Patch existing texture
```json
[{
     "textureTree" : {
            "level" : 0.2
        }
}]
```

## Parameters
* name : string
* url : string;
* noMipmap : boolean;
* level : number
* isBlocking : boolean

#### Alpha
* hasAlpha : boolean
* getAlphaFromRGB : boolean

#### UV
* uOffset : number
* vOffset : number
* uScale : number
* vScale : number
* uAng : number
* vAng : number
* wAng : number
* wrapU : number
* wrapV : number

#### Coordinates
* coordinatesIndex : number
* coordinatesMode : 
    * "spherical" or BABYLON.Texture.SPHERICAL_MODE 
    * "planar" or BABYLON.Texture.PLANAR_MODE 
    * "cubic" or BABYLON.Texture.CUBIC_MODE 
    * "projection" BABYLON.Texture.PROJECTION_MODE 
    * "skybox" or BABYLON.Texture.SKYBOX_MODE 
    * "invcubic" or BABYLON.Texture.INVCUBIC_MODE 
    * "equirectangular" or BABYLON.Texture.EQUIRECTANGULAR_MODE 
    * "fixed equirectangular" or  BABYLON.Texture.FIXED_EQUIRECTANGULAR_MODE
    * "fixed equirectangular mirrored" or BABYLON.Texture.FIXED_EQUIRECTANGULAR_MIRRORED_MODE 

#### Sampling mode
* samplingMode : string | number;
    * "nearest" or BABYLON.Texture.NEAREST_SAMPLINGMODE 
    * "bilinear" or BABYLON.Texture.BILINEAR_SAMPLINGMODE 
    * "trilinear" or BABYLON.Texture.TRILINEAR_SAMPLINGMODE 


#### LOD
* lodLevelInAlpha : boolean
* lodGenerationOffset : number
* lodGenerationScale : number
    
#### Misc
* invertY : boolean;
* invertZ : boolean
* anisotropicFilteringLevel : number
* gammaSpace : boolean




