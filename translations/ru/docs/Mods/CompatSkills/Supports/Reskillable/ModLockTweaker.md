# Твикер Блокировки Мода

## Блокировка модов

Это было добавлено как возможность конфигурации в 1.2.0 и теперь реализован CrT ZenMethod для его поддержки. Это также может быть сделано с помощью конфигурации, как уже упоминалось ранее.

Блокировки модов позволяют вам блокировать все стеки ItemStacks из определенного мода за определенным блоком.

### Синтаксис:

    // Пустой пример
    mods.compatskills.ModLock.addModLock(String modId, String... заблокирован);
    
    // Пример работы:
    mods.compatskills.ModLock.addModLock("minecraft", "reskillable:building|4");
    
    Замок заблокирует всё от мода "minecraft" за замком "building 4"