# PushReaction

A push reaction is what happens when a piston tries to push a block.

# 패키지 임포트하기

It might be required for you to import the package if you encounter any issues, so better be safe than sorry and add the import.  
`import mods.contenttweaker.PushReaction;`

## Comparing two reactions

You can see if two reactions are equal by using the `==` operator.

```zenscript
if(a == b){}
```

## Static methods

You can use these methods to get PushReaction Objects:

```zenscript
mods.contenttweaker.PushReaction.normal();
mods.contenttweaker.PushReaction.destroy();
mods.contenttweaker.PushReaction.block();
mods.contenttweaker.PushReaction.ignore();
mods.contenttweaker.PushReaction.pushOnly();
```