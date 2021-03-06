# Fermenter

ModTweaker allows you to add or remove forestry Fermenter Recipes

## 导入包

You can call the package using `mods.forestry.Fermenter`

## Recipe Removal

```zenscript
//mods.forestry.Fermenter.removeRecipe(IIngredient input);
mods.forestry.Fermenter.removeRecipe(<minecraft:reeds>);
mods.forestry.Fermenter.removeRecipe(<liquid:water>);
```

## Recipe Addition

```zenscript
//mods.forestry.Fermenter.addRecipe(ILiquidStack fluidOutput, IItemStack resource, ILiquidStack fluidInput, int fermentationValue, float fluidOutputModifier);
mods.forestry.Fermenter.addRecipe(<liquid:lava>, <minecraft:obsidian>, <liquid:water>, 1000, 0.5);
```

Amount of fluid output: fermentationValue * fluidOutputModifier

| 参数                  | 类型                                             | description                                   |
| ------------------- | ---------------------------------------------- | --------------------------------------------- |
| fluidOutput         | [ILiquidStack](/Vanilla/Liquids/ILiquidStack/) | The Recipe's output                           |
| resource            | [物品堆（IItemstack）](/Vanilla/Items/IItemStack/)  | The Recipe's item input                       |
| fluidInput          | [ILiquidStack](/Vanilla/Liquids/ILiquidStack/) | The Recipe's liquid input                     |
| fermentationValue   | int                                            | Amount of inputFluid on organic item requires |
| fluidOutputModifier | int                                            | Output multiplier                             |

## Fuel Removal

```zenscript
//mods.forestry.Fermenter.removeFuel(IIngredient fermenterItem);
mods.forestry.Fermenter.removeFuel(<forestry:fertilizer_compound>);

```

## Fuel Addition

```zenscript
//mods.forestry.Fermenter.addFuel(IItemStack item, int fermentPerCycle, int burnDuration);
mods.forestry.Fermenter.addFuel(<minecraft:leaves:1>, 100, 5);
```

| 参数              | 类型                                       | 说明                                                                                  |
| --------------- | ---------------------------------------- | ----------------------------------------------------------------------------------- |
| item            | [IItemStack](/Vanilla/Items/IItemStack/) | Item to become a valid fuel for the fermenter                                       |
| fermentPerCycle | int                                      | How much is fermented per work cycle, i.e. how much fluid of the input is consumed. |
| burnDuration    | int                                      | Amount of work cycles a single item of this fuel lasts before expiring.             |