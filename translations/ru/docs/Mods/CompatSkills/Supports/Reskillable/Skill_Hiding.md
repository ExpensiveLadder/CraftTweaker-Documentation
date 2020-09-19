# Умение скрыть / Блокировка видимости

Этот замок позволяет скрыть Навыки до тех пор, пока игрок не выполнит требования для просмотра навыка. Это имеет ограниченное количество вариантов использования, например, при добавлении «Классных» навыков в Настраиваемые наборы, где вы не хотите, чтобы кто-то, кто является «инженером», видел или мог получить доступ к странице навыка «Маг».

## Синтаксис:

    Пример пусто:
    mods.compatskills.VisibilityLock.addVisibilityLock(CTSkill, строка... Требования по умолчанию);
    
    Пример работы:
    mods.compatskills.VisibilityLock.addVisibilityLock(<skill:reskillable:attack>, "dim|1");