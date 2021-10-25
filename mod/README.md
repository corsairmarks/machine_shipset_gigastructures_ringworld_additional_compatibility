# Overview

This is a compatibility patch between the Machine Shipset and Gigastructural Engineering & More (3.1) to allow the additional three sizes of ringworld use the Machine Shipset graphics (including the Hive and machine variants).  That includes Titanic, Behemoth, and Gargantuan.

Warning: the graphics from Machine Shipset are not altered to reduce their curvature, so ringworld appearance is somewhat "bendy."  See sample images.

# Changes

Adds graphical entities for the Machine Shipset that are compatible with the new ringworld types from Gigastructural Engineering & More (3.1).  Adds an event to assign the `machine_01` graphical culture to these ringworld megastructures if the constructing empire has that graphical culture.

## Compatibility

Same compatibility as Gigastructural Engineering & More (3.1).

Built for Stellaris version 3.1.\* "Lem."  Not compatible with achievements.

### Required Dependency Mods

[Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) for the original graphics and other ship-related code.

[Gigastructural Engineering & More (3.1)](https://steamcommunity.com/sharedfiles/filedetails/?id=1121692237) is the mod we're making compatible.

### Recommended Companion Mods

[Machine Shipset Add-on: Gigastructural Engineering Ringworlds - Standard Ringworlds]() to use Machine Shipset graphics for original-sized ringworlds.

[Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102) to apply the owner's graphical culture to the standard ringworld from Origin: Shattered Ring.  Using my mod Subtle Polish is not recommended due to a high likelihood of conflicts with Gigas.

[Machine Shipset Add-on: Shattered Ring Appearance](https://steamcommunity.com/sharedfiles/filedetails/?id=2628980994) ensures that the permanently-destroyed sections for Origin: Shattered Ring using the Machine Shipset properly display as that shipset.  Adds missing graphical definitions to the Machine Shipset.

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/machine_shipset_gigastructures_ringworld_additional_compatibility)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.