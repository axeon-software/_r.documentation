# FresnelParameters

Patch or create fresnel parameters :
* diffuseFresnelParameters
* opacityFresnelParameters
* emissiveFresnelParameters
* refractionFresnelParameters
* reflectionFresnelParameters

* [doc.bjs.com - How to use FresnelParameters](https://doc.babylonjs.com/how_to/how_to_use_fresnelparameters) 
* [playground.bjs.com - Démo](http://www.babylonjs-playground.com/?19)

## Example
```json
[{
  "scene.material.000" : {
    "emissiveFresnelParameters": {
        "leftColor": "#ffffff",
        "rightColor": "#000000",
        "power": 1,
        "bias": 0
    }
  }
}]
```

## Parameters

* isEnabled : boolean  (_activate/deactivate fresnel effect_)
* leftColor : [color](colors-vectors-patching.md#colors) (_color used on edges_)
* rightColor :[color](colors-vectors-patching.md#colors) (_define color used on center_)
* bias : number (_define bias applied to computed fresnel term_)
* power : number (_to compute exponent applied to fresnel term_)



