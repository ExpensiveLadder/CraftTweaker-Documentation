# Saw

## Basic Recipe

* Adds Saw Recipe - inputs *MUST* have a block associated with them.

```zenscript
mods.betterwithmods.Saw.add(IIngredient input, IItemStack[] output);
//Examples
mods.betterwithmods.Saw.add(<minecraft:fence>,[<minecraft:stick>,<minecraft:stick>]);
```

## Removal by input

* Remove a recipe based on the input ingredient

```zenscript
mods.betterwithmods.Saw.remove(IIngredient input);
```

## Removal by output

* Remove a recipe based on the output

```zenscript
mods.betterwithmods.Saw.remove(IItemStack[] outputs);
```

## Remove all

* Remove all recipes

```zenscript
mods.betterwithmods.Saw.removeAll();
```

## Builder

The Saw has a recipe builder. Due to the nature of the saw it currently has no special builder methods, I will document it none-the-less.

* To create a new Saw builder. `mods.betterwithmods.Saw.builder()`

* Saw methods
     
     * Sets up the inputs and outputs of the recipe  
          zenscript buildRecipe(IIngredient[] inputs, IItemStack[] outputs)  
              Sets up the inputs and outputs of the recipe<br />
                    zenscript
                    buildRecipe(IIngredient[] inputs, IItemStack[] outputs)
     
     * Finalize the recipe and add it to the game  
          zenscript build()  
              Finalize the recipe and add it to the game<br />
                    zenscript
                    build()

### Example builder usage

    mods.betterwithmods.Saw.builder()
    .buildRecipe([<minecraft:oak_fence>], [<minecraft:stick>*6])
    .build();