# Microwave

The Microwave heats up food items.

## Default Microwave Recipes

- Beef -> Cooked Beef
- Porkchop -> Cooked Porkchop
- Potato -> Baked Potato
- Chicken -> Cooked Chicken
- Fish -> Cooked Fish
- Salmon -> Cooked Salmon
- Flesh -> Cooked Flesh

## 移除配方

## Remove matching oven recipes.

```zenscript
mods.cfm.Oven.remove(@Optional final IIngredient output, @Optional final IIngredient input);

// Remove recipes that result in Cooked Flesh
mods.cfm.Oven.remove(<cfm:item_flesh_cooked>);
// Remove recipes that require a Potato
mods.cfm.Oven.remove(null,<minecraft:potato>);
// Remove all recipes
mods.cfm.Oven.remove();
```

## 添加

## Add an oven recipe.

```zenscript
mods.cfm.Oven.addRecipe(@Nonnull final IItemStack output, @Nonnull final IItemStack input);

// Add a recipe that makes two apples from one stick
mods.cfm.Oven.addRecipe(<minecraft:apple>.withAmount(2),<minecraft:stick>);
```