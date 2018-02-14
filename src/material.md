# Standard Material

[doc.bjs.com Materials](https://doc.babylonjs.com/features/materials)

#### Patch existing material

```json
[
  {
    "material1" : {
        "diffuseColor" : "#00ff00",
        "isFrozen" : true,
        "emissiveColor" : "#0000ff"
    }   
  }   
]
```

#### Assign existing material to a mesh

```json
[
  {
    "mesh2" : {
        "material" : "material1"
    }   
  }   
]
```

#### Create new material with _material::standard_

```json
[
  {
    "mesh1" : {
        "material" : {
            "material::standard" : {
                "name" : "material1",
                "diffuseColor" : "#ff0000"
            }
        }
    }   
  }   
]
```

## Standard Materials Parameters 

From [doc.bjs.com - Material](http://doc.babylonjs.com/classes/3.1/Material) + [StandardMaterial](http://doc.babylonjs.com/classes/3.1/StandardMaterial)

* id : string 
* name : string
* fogEnabled : boolean
* isFrozen : boolean
* zOffset : number

#### Diffuse
As viewed under a light. 
* diffuseColor : [color](colors-vectors-patching.md#colors)
* diffuseTexture : [texture](texture.md)
* useAlphaFromDiffuseTexture : boolean

#### Specular
Highlight given to the material by a light.
* specularColor :  [color](colors-vectors-patching.md#colors)
* specularTexture : [texture](texture.md)
* specularPower : number
* useSpecularOverAlpha : boolean
* useGlossinessFromSpecularMapAlpha : boolean

#### Emissive
As if self lit.
* emissiveColor : [color](colors-vectors-patching.md#colors)
* emissiveTexture : [texture](texture.md)
* useEmissiveAsIllumination : boolean
* linkEmissiveWithDiffuse : boolean

#### Ambient
Lit by the environmental background lighting.
* ambientColor : [color](colors-vectors-patching.md#colors)
* ambientTexture : [texture](texture.md)

#### Opacity
* alpha : number
* opacityTexture : [texture](texture.md)
* alphaMode [bjs-playground - alphaModes](https://www.babylonjs-playground.com/#1MSIXB#7): 
    * BABYLON.Engine.ALPHA_COMBINE,BABYLON.Engine.ALPHA_ADD
    * BABYLON.Engine.ALPHA_SUBTRACT
    * BABYLON.Engine.ALPHA_MULTIPLY
    * BABYLON.Engine.ALPHA_MAXIMIZED
* backFaceCulling : boolean

#### Bump
* bumpTexture : [texture](texture.md)

#### Reflection
* reflectionTexture : [texture](texture.md)
* useReflectionOverAlpha : boolean

#### Refraction
* refractionTexture : [texture](texture.md)
* indexOfRefraction : number
* invertRefractionY : boolean

#### Lighting
* lightmapTexture : [texture](texture.md)
* maxSimultaneousLights : number
* disableLighting : boolean
* useLightmapAsShadowmap : boolean
* twoSidedLighting : boolean

#### Fresnel
[doc.bjs.com - How to use FresnelParameters](http://doc.babylonjs.com/how_to/how_to_use_fresnelparameters)

* diffuseFresnelParameters : [FresnelParameters](fresnelParameters.md)
* opacityFresnelParameters : [FresnelParameters](fresnelParameters.md)
* reflectionFresnelParameters : [FresnelParameters](fresnelParameters.md)
* refractionFresnelParameters : [FresnelParameters](fresnelParameters.md)
* emissiveFresnelParameters : [FresnelParameters](fresnelParameters.md)
* useReflectionFresnelFromSpecular : boolean

#### Parallax
[doc.bjs.com - How to use Parallax Mapping](http://doc.babylonjs.com/how_to/using_parallax_mapping)

* useParallax : boolean
* useParallaxOcclusion : boolean
* parallaxScaleBias : number


#### Misc
* invertNormalMapX : boolean
* invertNormalMapY : boolean
* fillMode : BABYLON.Material.TriangleFillMode | BABYLON.Material.WireFrameFillMode | BABYLON.Material.PointFillMode 
* roughness : number
* useLogarithmicDepth : boolean
* wireframe : boolean
* state : string
* sideOrientation : BABYLON.Material.ClockWiseSideOrientation |  BABYLON.Material.CounterClockWiseSideOrientation 
* needDepthPrePass : boolean
* disableDepthWrite : boolean
* forceDepthWrite : boolean
* separateCullingPass : boolean
* pointSize : number
* pointsCloud : boolean
* checkReadyOnEveryCall : boolean
* checkReadyOnlyOnce : boolean

