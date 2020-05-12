# new\_settlements

## How settlements work

The way the game adds settlements is by combining two XML based files: One to define what type of settlement it is \(hideout, village, city, castle etc.\), who owns it and other relevant parameters such as prosperity, production, which town a village belongs to etc. This definition happens in the base game under Modules/SandBox/ModuleData/settlements.xml Beside this file is a distance cache Modules/SandBox/ModuleSata/Settlements\_distance\_cache.bin, which can be generated in code.

This definition does not however define the actual visuals of the settlement. This is done inside Modules/SandBox/SceneObj/Main\_map/scene.xscene file.

## Notes on future SDK support

From other code in the available DLLs it is evident that settlement modding is supposed to occur by using an editor. This editor helps place settlements, define their visuals and also generates the aforementioned distance cache. For now, none of that exists and one has to resort to pure XML modding.

## Notes on the distance cache

It is unclear what the distance cache actually does. Without updating it AI seems to visit added settlements just fine, they recruit troops there, offload prisoners and buy goods. Players can also enter the new settlements just fine. The distance cache might be associated with some AI decision making, but it is unclear. The distance cache is created by the method SaveSettlementDistanceCache\(\) in SettlementPositionScript, which is a class that is not used in the game currently, supposedly originating from the aforementioned map editor. The class can be found in SandBox.View.dll.

## How to override the default settlements of the game

When creating a mod it is possible to override the definitions from the SandBox module. It is not however possible to append \(add\) things to the files, so if you want to make changes to settlements you need to make changes to everything.

Start by copying Modules/SandBox/ModuleData/settlements.xml into Modules/YourModName/ModuleData/settlements.xml as well as Modules/SandBox/SceneObj/Main\_map \(a folder\) to Modules/YourModName/SceneObj/Main\_map.

If you can avoid it, don't use the regular notepad for XML editing. Instead use a proper XML editing tool or a more capable text editor such as Notepad++.

Inside Modules/YourModName/submodule.xml add the following XmlNode

```text
        <XmlNode>
            <XmlName id="Settlements" path="settlements"/>
            <IncludeGameTypes>
                <GameType value = "Campaign"/>
                <GameType value = "CampaignStoryMode"/>
            </IncludeGameTypes>
        </XmlNode>
```

The Main\_map is loaded automatically.

Within settlements.xml you can now copy e.g. a town and customize it however you want, or change some of the existing towns \(by e.g. changing the owner, changing starting prosperity, changing production of it etc.\). It is _imperative_ that every entry in settlements.xml has its own id.

Within your mods Main\_map/scene.xscene file there needs to be a game\_entity for each entry in your settlements.xml file. Make sure not to have any duplicate id's.

An example for a new entry \(i.e. adding to the existing file, not entirely replacing its contents\) to settlements.xml that adds a town and two villages [can be found here](https://pastebin.com/BuSbQ6x2).

Note that, the two entries for villages village\_M1\_1 and village\_M1\_2 have entries for which town they are bound to:

```text
trade_bound="Settlement.town_M1" bound="Settlement.town_M1"
```

It's not clear how exactly these two differ, but for now best set them to the town you want them to belong to. The villages also include definitions for which good you want them to produce:

```text
village_type="VillageType.fisherman"
```

Village types are defined in Modules/SandBox/ModuleData/spprojects.xml.

These three new settlements need correspondin game\_entity definitions in the Main\_map/scene.xscene file. An example entry [can be found here](https://pastebin.com/dXcKT7wf)

