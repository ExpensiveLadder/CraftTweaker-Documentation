# Squeezer

The Squeezer package can be used to add/remove recipes to/from the Immersive Engineering Squeezer.

## Calling The Package

You can call the Squeezer package using `mods.immersiveengineering.Squeezer`.

## Add Recipe

| Required | Тип    | Data Type                                           |
| -------- | ------ | --------------------------------------------------- |
| Required | Output | [IItemStack](/Vanilla/Items/IItemStack/)            |
| Required | Fluid  | [Fluidstack](/Vanilla/Liquids/ILiquidStack/)        |
| Required | Input  | [IIngredient](/Vanilla/Variable_Types/IIngredient/) |
| Required | Energy | Integer                                             |

### Пример

```zenscript
//Example:
mods.immersiveengineering.Squeezer.addRecipe(IItemStack output, ILiquidStack fluid, IIngredient input, int energy);

mods.immersiveengineering.Squeezer.addRecipe(<minecraft:diamond>, <liquid:water>, <ore:logWood>, 2048);
```

## Remove Fluid Recipe

| Тип    | Data Type                                    |
| ------ | -------------------------------------------- |
| Output | [Fluidstack](/Vanilla/Liquids/ILiquidStack/) |

### Пример

```zenscript
//Example:
mods.immersiveengineering.Squeezer.removeFluidRecipe(ILiquidStack fluid);

mods.immersiveengineering.Squeezer.removeFluidRecipe(<liquid:water>);
```

## Remove Item Recipe

| Тип    | Data Type                                |
| ------ | ---------------------------------------- |
| Output | [IItemstack](/Vanilla/Items/IItemStack/) |

### Пример

```zenscript
//Example:
mods.immersiveengineering.Squeezer.removeItemRecipe(IItemStack stack);

mods.immersiveengineering.Squeezer.removeItemRecipe(<minecraft:diamond>);
```

## Remove By Input

| Тип    | Data Type                                |
| ------ | ---------------------------------------- |
| Output | [IItemstack](/Vanilla/Items/IItemStack/) |

### Пример

```zenscript
//Example:
mods.immersiveengineering.Squeezer.removeByInput(IItemStack stack);

mods.immersiveengineering.Squeezer.removeByInput(<minecraft:log>);
```