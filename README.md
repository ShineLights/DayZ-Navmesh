# DayZ - Generating Navigation Mesh Guide | ENG + RUS
--------------------------------------------------------------------------------
# ENGLISH

![alt text](https://i.imgur.com/IMB5pcR.png)

This page describes the basics of generating navigation mesh file (often called 'navmesh') for your terrain. Navmesh for your terrain is not mandatory (game will cope without it), but it contains essential data for the AI (obstacles, door links, jump links,..) without which it wont be able to navigate properly (AI entities will stand frozen on their spawn point). For guaranteed behavior of the AI, it is necessary to re-generate navmesh after each new terrain build.

Requirements:

- DayZ and DayZ Tools package installed.
- Have a working custom terrain (mod) files, binarized and packed into pbo. (Just map from Workshop)

# General info

1. You need mission folder (empty.Mapname) [Check Extras folder for examples]
2. You need server config. ServerDZNV.cfg [Check Extras folder for examples]
3. Use .bat file.
4. Run as Administrator NavMeshGenerator tool [DayZ Tools\Bin\NavMeshGenerator\NavMeshGenerator_x64.exe]
5. Click on "Generation" ==> "Connect Data Server" ==> "OK". [Dont change addresses]
6. Click on "Start Generating" ==> "OK".
7. You are best!
8. After navmesh generation is finished (progress reaches 100%), make sure NOT to close the tool and use File ==> Save NavMesh. Save as navmesh.nm file.

# Structure of files:
C:\SteamLibrary\steamapps\common\DayZ\
- DayZ_x64.exe
- DayZDiag_x64.exe
- ServerDZNV.cfg
- Navmesh_Mapname.bat
- empty.Mapname
- @Mapname

# Custom mapping [DayZ Editor Loader, Builderitems, Init.c, Expansion]

1. You need mission folder (empty.Mapname) [Check Extras folder for examples]
- Put your custom buildings in mission folder. [.dze, init.c, etc.]
2. You need server config. ServerDZNV.cfg [Check Extras folder for examples]
3. Use .bat file.
- Add mods in your .bat file. [-mod=@CF;@DayZ-Editor-Loader;]
4. Run as Administrator NavMeshGenerator tool [DayZ Tools\Bin\NavMeshGenerator\NavMeshGenerator_x64.exe]
5. Click on "Generation" ==> "Connect Data Server" ==> "OK". [Dont change addresses]
6. Click on "Start Generating" ==> "OK".
7. You are best!
8. After navmesh generation is finished (progress reaches 100%), make sure NOT to close the tool and use File ==> Save NavMesh. Save as navmesh.nm file.
9. Make .pbo with new navmesh with prefix and version. [Prefix for Chernarus - "DZ\worlds\chernarusplus\navmesh"]

# Structure of files:
C:\SteamLibrary\steamapps\common\DayZ\
- DayZ_x64.exe
- DayZDiag_x64.exe
- ServerDZNV.cfg
- Navmesh_Mapname.bat
- empty.Mapname
- @Mapname
- @DayZ-Editor-Loader




# DayZ - Руководство по генерации навигационной сетки | АНГ. + РУС.
--------------------------------------------------------------------------------
# РУССКИЙ

На этой странице описаны основы создания навигационного сетчатого файла (часто называемого "navmesh") для вашей местности. Навмеш для местности не является обязательным (игра справится и без него), но он содержит важные данные для ИИ (препятствия, ссылки на двери, ссылки на прыжки...), без которых он не сможет правильно ориентироваться (сущности ИИ будут застывать на точке спавна). Для стабильного поведения ИИ необходимо заново генерировать navmesh после каждого нового построения местности.

Требования:

- Установлен пакет DayZ и DayZ Tools.
- Наличие рабочих файлов пользовательской местности (мод), бинаризованных и упакованных в pbo. (Карта из мастерской)

# Общая информация

1. Вам нужна папка с миссией (empty.Mapname) [Посмотрите папку Extras для примеров].
2. Вам нужен конфиг сервера. ServerDZNV.cfg [Проверьте папку Extras для примеров]
3. Используйте .bat-файл.
4. Запустите от имени администратора инструмент NavMeshGenerator [DayZ Tools\Bin\NavMeshGenerator\NavMeshGenerator_x64.exe]
5. Нажмите на "Generation" ==> "Connect Data Server" ==> "OK". [Не меняйте адреса].
6. Нажмите на "Start Generating" ==> "OK".
7. Вы лучший!
8. После завершения генерации navmesh (прогресс достигнет 100%), убедитесь, что инструмент не закрыт, и используйте File ==> Save NavMesh. Сохраните как файл navmesh.nm.

# Структура файлов:
C:\SteamLibrary\steamapps\common\DayZ\
- DayZ_x64.exe
- DayZDiag_x64.exe
- ServerDZNV.cfg
- Navmesh_Mapname.bat
- empty.Mapname
- @Mapname

# Пользовательские постройки [DayZ Editor Loader, Builderitems, Init.c, Expansion]

1. Вам нужна папка с миссией (empty.Mapname) [Посмотрите примеры в папке Extras].
- Поместите ваши пользовательские здания в папку миссии. [.dze, init.c и т.д.].
2. Вам нужен конфиг сервера. ServerDZNV.cfg [Проверьте папку Extras для примеров]
3. Используйте .bat-файл.
- Добавьте мод в .bat-файл. [-mod=@CF;@DayZ-Editor-Loader;]
4. Запустите от имени администратора инструмент NavMeshGenerator [DayZ Tools\Bin\NavMeshGenerator\NavMeshGenerator_x64.exe]
5. Нажмите на "Generation" ==> "Connect Data Server" ==> "OK". [Не меняйте адреса].
6. Нажмите на "Start Generating" ==> "OK".
7. Вы лучший!
8. После завершения генерации navmesh (прогресс достигнет 100%), убедитесь, что инструмент не закрыт, и используйте File ==> Save NavMesh. Сохраните как файл navmesh.nm.
9. Создайте .pbo с новым навмешем с префиксом и версией. [Префикс для Чернаруса - "DZ\worlds\chernarusplus\navmesh"].

# Структура файлов:
C:\SteamLibrary\steamapps\common\DayZ\
- DayZ_x64.exe
- DayZDiag_x64.exe
- ServerDZNV.cfg
- Navmesh_Mapname.bat
- empty.Mapname
- @Mapname
- @DayZ-Editor-Loader