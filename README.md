# Better AI - AI Behavior Variable Tweaks for HBS BATTLETECH
This is a mod to improve the tactical AI in combat.  It has been overhauled to work better as a Lance, reserve and make smarter indivudual choices.  The AI's critical hit chance is adjusted to be on par with the player's.  The Pilot selections for AI Lances are tuned to put appropriate pilots in the right units.  This has been limited to two 'Mechs or less per Lance to preserve encounter variety, all vehicles have had "useless" pilot abilities excluded.  BetterAI should be harder to fight than stock, but some bad choices are not fixable with .json edits.  

When used with ModTek, Better AI shouldn't cause any errors with save files, even saves in combat, or with version changes. I've done extensive testing back and forth between stock and modded play without any errors. It does not add any new items to the VersionManifest.csv.  Of course, when used with the HBS Mod Loader, any save that has this mod enabled will need it going forward as normal.

##### Credits:
    Mpstark + ModTek Crew: For creating this inital git and ModTek support, and again to Mpstark for making the AIToolkit
    scJazz: The idea for Lance Pilot tuning
    Koztaz: For the fresh eyes on an old project
    Thanks to all who have provided feedback and bounced ideas around with me, 
    Team Banzai, Goons, discord modders and everyone since beta onward that has helped shape the AI.

### Instructions:

    Remove older editions of Better AI if present.
    Copy Better AI folder in to Mods folder.
    
### ModTek

This mod can use either HBS Mod Manager or ModTek:

https://github.com/BattletechModders/ModTek/releases
    
#### Optional Dependancies:
    cFixes
    Z_Sab_JK_RarityTables
Better AI will load AFTER these mods by default, none of these are required.  This is so they may apply their JSON overwrites first, then Better AI's advanvced JSON merge will apply on top of the modded file.  Better AI edits some 'Mech Tags in MechDefs and nearly all Pilot's Tags in LanceDefs.

#### Optional AI Modules:

    https://github.com/Amechwarrior/BetterAI-Permanent-Evasion-Add-On/releases/tag/v1.9.1.1
This is a module that applies on top of Better AI for players or mod packs using permanent or semi-permanent evasion mechanics.

### Full change log can be found here:

https://forum.paradoxplaza.com/forum/index.php?threads/mod-release-better-ai-tweaks-for-deadlier-ai.1075322/

### Googledoc sheets with all stock + modded variables, unit_role and unit_lance tags:

https://docs.google.com/spreadsheets/d/1Q-Z0jSjb1rRd5-r0zYHwH_yES8cgVdmv-kE2WS_7lHE/edit#gid=0&range=A1

### Recommended Companion Mods

https://github.com/BattletechModders/cFixes/releases - Commuinity bug fixes, Better AI greatly benifits from the corrected NPC pilot traits fixes and integrates with that mod's 'Mech tag fixes.

## Stock Files Edited:
#### StreamingAssets\data\behaviorVariables - AI variable edits
    global.json
    global_def.json
    global_sensorlock.json
    role_activeprobe.json
    role_ecmcarrier.json
    role_ewe.json
    role_lastmanstanding.json
    role_lastmanstanding_def.json
    role_meleeonly.json
    role_noncombatant.json
    role_scout.json
    role_sniper.json
    role_sniper_def.json
    role_vehicle.json

#### StreamingAssets\data\constants - AI Crit Chance
    CombatGameConstants.json

#### StreamingAssets\data\lance - LanceDef Pilot Optimizations
    lancedef_mech_d1_dynamic_solo.json
    lancedef_mech_d2_dynamic_solo.json
    lancedef_mech_d3_dynamic_lightBattle.json
    lancedef_mech_d3_dynamic_lightCavalry.json
    lancedef_mech_d3_dynamic_lightFire.json
    lancedef_mech_d3_dynamic_lightScout.json
    lancedef_mech_d3_dynamic_lightSupport.json
    lancedef_mech_d3_dynamic_solo.json
    lancedef_mech_d4_dynamic_lightMedBattle.json
    lancedef_mech_d4_dynamic_lightMedCavalry.json
    lancedef_mech_d4_dynamic_lightMedFire.json
    lancedef_mech_d4_dynamic_lightMedScout.json
    lancedef_mech_d4_dynamic_lightMedSupport.json
    lancedef_mech_d4_dynamic_smallLightMedBattle.json
    lancedef_mech_d4_dynamic_smallLightMedFire.json
    lancedef_mech_d4_dynamic_smallMedCavalry.json
    lancedef_mech_d4_dynamic_smallMedScout.json
    lancedef_mech_d4_dynamic_smallMedSupport.json
    lancedef_mech_d4_dynamic_solo.json
    lancedef_mech_d5_dynamic_MedBattle.json
    lancedef_mech_d5_dynamic_MedCavalry.json
    lancedef_mech_d5_dynamic_MedFire.json
    lancedef_mech_d5_dynamic_MedScout.json
    lancedef_mech_d5_dynamic_MedSupport.json
    lancedef_mech_d5_dynamic_smallMedBattle.json
    lancedef_mech_d5_dynamic_smallMedCavalry.json
    lancedef_mech_d5_dynamic_smallMedFire.json
    lancedef_mech_d5_dynamic_smallMedScout.json
    lancedef_mech_d5_dynamic_smallMedSupport.json
    lancedef_mech_d5_dynamic_solo.json
    lancedef_mech_d6_dynamic_MedHeavyBattle.json
    lancedef_mech_d6_dynamic_MedHeavyCavalry.json
    lancedef_mech_d6_dynamic_MedHeavyFire.json
    lancedef_mech_d6_dynamic_MedHeavyScout.json
    lancedef_mech_d6_dynamic_MedHeavySupport.json
    lancedef_mech_d6_dynamic_SmallMedHeavyBattle.json
    lancedef_mech_d6_dynamic_SmallMedHeavyCavalry.json
    lancedef_mech_d6_dynamic_smallMedHeavyFire.json
    lancedef_mech_d6_dynamic_smallMedHeavySupport.json
    lancedef_mech_d6_dynamic_solo.json
    lancedef_mech_d7_dynamic_HeavyBattle.json
    lancedef_mech_d7_dynamic_HeavyCavalry.json
    lancedef_mech_d7_dynamic_HeavyFire.json
    lancedef_mech_d7_dynamic_HeavyScout.json
    lancedef_mech_d7_dynamic_HeavySupport.json
    lancedef_mech_d7_dynamic_SmallHeavyBattle.json
    lancedef_mech_d7_dynamic_SmallHeavyCavalry.json
    lancedef_mech_d7_dynamic_SmallHeavyFire.json
    lancedef_mech_d7_dynamic_SmallHeavyScout.json
    lancedef_mech_d7_dynamic_SmallHeavySupport.json
    lancedef_mech_d7_dynamic_solo.json
    lancedef_mech_d8_dynamic_HeavyBattle.json
    lancedef_mech_d8_dynamic_HeavyCavalry.json
    lancedef_mech_d8_dynamic_HeavyFire.json
    lancedef_mech_d8_dynamic_HeavyScout.json
    lancedef_mech_d8_dynamic_HeavySupport.json
    lancedef_mech_d8_dynamic_solo.json
    lancedef_mech_d9_dynamic_assaultHeavyBattle.json
    lancedef_mech_d9_dynamic_assaultHeavyCavalry.json
    lancedef_mech_d9_dynamic_assaultHeavyFire.json
    lancedef_mech_d9_dynamic_assaultHeavyScout.json
    lancedef_mech_d9_dynamic_assaultHeavySupport.json
    lancedef_mech_d9_dynamic_solo.json
    lancedef_mech_d10_dynamic_assaultBattle.json
    lancedef_mech_d10_dynamic_assaultCavalry.json
    lancedef_mech_d10_dynamic_assaultFire.json
    lancedef_mech_d10_dynamic_assaultHeavySupport.json
    lancedef_mech_d10_dynamic_assaultScout.json
    lancedef_mech_d10_dynamic_solo.json
    lancedef_mixed_d3_dynamic_lightBattle.json
    lancedef_mixed_d4_dynamic_lightBattle.json
    lancedef_mixed_d5_dynamic_mediumBattle1.json
    lancedef_mixed_d5_dynamic_mediumBattle2.json
    lancedef_mixed_d5_dynamic_mediumBattle3.json
    lancedef_mixed_d6_dynamic_mediumBattle1.json
    lancedef_mixed_d6_dynamic_mediumBattle2.json
    lancedef_mixed_d6_dynamic_mediumBattle3.json
    lancedef_mixed_d7_dynamic_heavyBattle1.json
    lancedef_mixed_d7_dynamic_heavyBattle2.json
    lancedef_mixed_d8_dynamic_heavyBattle1.json
    lancedef_mixed_d8_dynamic_heavyBattle2.json
    lancedef_mixed_d9_dynamic_assaultBattle1.json
    lancedef_mixed_d9_dynamic_assaultBattle2.json
    lancedef_mixed_d10_dynamic_assaultBattle1.json
    lancedef_mixed_d10_dynamic_assaultBattle2.json
    lancedef_vehicle_d3_dynamic_lightBattle.json
    lancedef_vehicle_d4_dynamic_lightBattle.json
    lancedef_vehicle_d5_dynamic_mediumBattle.json
    lancedef_vehicle_d6_dynamic_mediumBattle.json
    lancedef_vehicle_d7_dynamic_HeavyBattle.json
    lancedef_vehicle_d8_dynamic_HeavyBattle.json
    lancedef_vehicle_d9_dynamic_AssaultBattle.json
    lancedef_vehicle_d10_dynamic_AssaultBattle.json

#### StreamingAssets\data\mech - Role Tag Replacement
    mechdef_awesome_AWS-8Q.json
    mechdef_enforcer_ENF-4R.json
    mechdef_locust_LCT-1M.json
    mechdef_quickdraw_QKD-4G.json
    mechdef_quickdraw_QKD-5A.json
    mechdef_shadowhawk_SHD-2D.json
    mechdef_urbanmech_UM-R60.json
    mechdef_urbanmech_UM-R90.json
    mechdef_victor_VTR-9S.json
    mechdef_zeus_ZEU-6S.json
    mechdef_zeus_ZEU-6T.json
