Вопросы:

1. Найдите полный хеш и комментарий коммита, хеш которого начинается на `aefea`.
2. Какому тегу соответствует коммит `85024d3`?
3. Сколько родителей у коммита `b8d720`? Напишите их хеши.
4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами  v0.12.23 и v0.12.24.
5. Найдите коммит в котором была создана функция `func providerSource`, ее определение в коде выглядит 
так `func providerSource(...)` (вместо троеточия перечислены аргументы).
6. Найдите все коммиты в которых была изменена функция `globalPluginDirs`.
7. Кто автор функции `synchronizedWriters`? 

Ответы:

1. Командой "git show aefea" выводим коммит с полным хешом начинающимся на "aefea"
2. v0.12.23
3. Командой "git show --pretty=format:' %P' b8d720"  56cd7859e05c36c06b56d013b55a252d0bb7e158,9ea88f22fc6269854151c571162c5bcf958bee2b 
4. Командой "git log  --oneline v0.12.23..v0.12.24", результат 
    33ff1c03bb (tag: v0.12.24) v0.12.24
    b14b74c493 [Website] vmc provider links
    3f235065b9 Update CHANGELOG.md
    6ae64e247b registry: Fix panic when server is unreachable
    5c619ca1ba website: Remove links to the getting started guide's old location
    06275647e2 Update CHANGELOG.md
    d5f9411f51 command: Fix bug when using terraform login on Windows
    4b6d06cc5d Update CHANGELOG.md
    dd01a35078 Update CHANGELOG.md
    225466bc3e Cleanup after v0.12.23 release
5. Командой "git log -S "func providerSource" --oneline", находим коммиты где упоминается функция "providerSource" - результат
    5af1e6234a main: Honor explicit provider_installation CLI config when present
    8c928e8358 main: Consult local directories as potential mirrors of providers
   Далее командой "git show 5af1e6234a" и "git show 8c928e8358" выясняем что создана функция в коммите с хешом 5af1e6234a
6. Коммиты - 
    78b1220558 Remove config.go and update things using its aliases
    52dbf94834 keep .terraform.d/plugins for discovery
    41ab0aef7a Add missing OS_ARCH dir to global plugin paths
    66ebff90cd move some more plugin search path logic to command
    8364383c35 Push plugin discovery down into command package
7. Командой "git log -S "func synchronizedWriters" --pretty=format:'%h - %an, %ae'" получаем результат
    bdfea50cc8 - James Bardin, j.bardin@gmail.com
    5ac311e2a9 - Martin Atkins, mart@degeneration.co.uk