# DayZ-Generating Navigation Mesh Guide | ENG + RUS
--------------------------------------------------------------------------------
# ENGLISH

![alt text](https://i.imgur.com/IMB5pcR.png)

This page describes the basics of generating navigation mesh file (often called 'navmesh') for your terrain. Navmesh for your terrain is not mandatory (game will cope without it), but it contains essential data for the AI (obstacles, door links, jump links,..) without which it wont be able to navigate properly (AI entities will stand frozen on their spawn point). For guaranteed behavior of the AI, it is necessary to re-generate navmesh after each new terrain build (each time wrp is binarized to be precise).

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