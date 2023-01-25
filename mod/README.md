# Overview

This is a compatibility patch between the Machine Shipset and Gigastructural Engineering & More (3.6) to allow the additional three sizes of ringworld use the Machine Shipset graphics (including the Hive and machine variants).  That includes titanic, behemoth, and gargantuan.

Warning: the graphics from Machine Shipset are not altered to reduce their curvature, so ringworld appearance is somewhat "bendy."  See sample images.

# Changes

Adds graphical entities for the Machine Shipset that are compatible with the new ringworld types from Gigastructural Engineering & More (3.6).  Adds an event to assign the `machine_01` graphical culture to these ringworld megastructures if the constructing empire has that graphical culture.  Overrides the final stage of titanic, behemoth, and gargantuan ringworld construction as well as restoration from ruined, so that seam sections are flagged and can be identified for changing the graphical culture.

## Compatibility

Same compatibility as Gigastructural Engineering & More (3.6).  Overrides six megastructures from Gigastructural Engineering: `ringworld_titanic_2`, `ring_world_titanic_restored`, `ringworld_behemoth_2`, `ring_world_behemoth_restored`, `ringworld_gargantuan_2`, and `ring_world_gargantuan_restored` in order to ensure the seam sectors are flagged with the ringworld size, for easier targeting to change the graphical culture, which could conflict with other Gigastructres add-ons.

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements, but neither are the dependencies.

### Required Dependency Mods

* [Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) for the original graphics and other ship-related code
* [Gigastructural Engineering & More (3.6)](https://steamcommunity.com/sharedfiles/filedetails/?id=1121692237) is the mod we're making compatible

### Recommended Companion Mods

* [Machine Shipset Add-on: Gigastructural Engineering Ringworlds - Standard Ringworlds](https://steamcommunity.com/sharedfiles/filedetails/?id=2644466861) to enable the Machine Shipset graphics for standard-sized ringworlds
* [Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102) to apply the owner's graphical culture to the standard ringworld from Origin: Shattered Ring ( my mod Subtle Polish is not recommended due to a high likelihood of conflicts with Gigas)
* [Machine Shipset Add-on: Shattered Ring Appearance](https://steamcommunity.com/sharedfiles/filedetails/?id=2628980994) ensures that the permanently-destroyed sections for Origin: Shattered Ring using the Machine Shipset properly display as that shipset (adds missing graphical definitions to the Machine Shipset)

### When to Install

This mod can be safely added after the game has started, but should not be removed from a game in-progress.  It can theoretically be removed from a game in progress - any titanic, behemoth, or gargantuan ringworlds should revert to the fallback appearance for the Machine Shipset (`mammalian_01`).  Back up your savegame before attempting to remove a mod.

### Known Issues

Overriding a megastructure results in the game logging an error in the error.log file.  Expect to see six errors like this:

```
[23:42:22][game_singleobjectdatabase.h:165]: Object with key: ringworld_behemoth_2 already exists, using the one at  file: common/megastructures/zzz_behemoth_ringworld_overrides.txt line: 1
[23:42:22][game_singleobjectdatabase.h:165]: Object with key: ring_world_behemoth_restored already exists, using the one at  file: common/megastructures/zzz_behemoth_ringworld_overrides.txt line: 190
[23:42:22][game_singleobjectdatabase.h:165]: Object with key: ringworld_gargantuan_2 already exists, using the one at  file: common/megastructures/zzz_gargantuan_ringworld_overrides.txt line: 1
[23:42:22][game_singleobjectdatabase.h:165]: Object with key: ring_world_gargantuan_restored already exists, using the one at  file: common/megastructures/zzz_gargantuan_ringworld_overrides.txt line: 196
[23:42:22][game_singleobjectdatabase.h:165]: Object with key: ringworld_titanic_2 already exists, using the one at  file: common/megastructures/zzz_titanic_ringworld_overrides.txt line: 1
[23:42:22][game_singleobjectdatabase.h:165]: Object with key: ring_world_titanic_restored already exists, using the one at  file: common/megastructures/zzz_titanic_ringworld_overrides.txt line: 179
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 Mark as compatible with Stellaris version 3.2 "Herbert" - no script changes
* 1.2.0 Mark as compatible with Stellaris version 3.3 "Libra" - no script changes
* 1.3.0 Mark as compatible with Stellaris version 3.4 "Cepheus" - no script changes
* 2.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Integrate underlying changes from Gigastructural Engineering
* 2.1.0 Add compatibility trigger for other mods to check whether this one is active

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/machine_shipset_gigastructures_ringworld_additional_compatibility)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.