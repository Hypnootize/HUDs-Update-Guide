# ADDING MISSING STATUS ICONS

To be clear we are talking about these icons:

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Status_Icon.png)

All these icons can be found and edited inside the **resource/ui/HudPlayerHealth.res**

What we will do is open our **HudPlayerHealth.res** and go through this list to check which icon codes we are missing:

```
PlayerStatusBleedImage
PlayerStatusHookBleedImage
PlayerStatusGasImage
PlayerStatusMilkImage
PlayerStatusMarkedForDeathImage
PlayerStatusMarkedForDeathSilentImage
PlayerStatus_MedicUberBulletResistImage
PlayerStatus_MedicUberBlastResistImage
PlayerStatus_MedicUberFireResistImage
PlayerStatus_MedicSmallBulletResistImage
PlayerStatus_MedicSmallBlastResistImage
PlayerStatus_MedicSmallFireResistImage
PlayerStatus_WheelOfDoom
PlayerStatus_SoldierOffenseBuff
PlayerStatus_SoldierDefenseBuff
PlayerStatus_SoldierHealOnHitBuff
PlayerStatus_Parachute
PlayerStatus_RuneStrength
PlayerStatus_RuneHaste
PlayerStatus_RuneRegen
PlayerStatus_RuneResist
PlayerStatus_RuneVampire
PlayerStatus_RuneReflect
PlayerStatus_RunePrecision
PlayerStatus_RuneAgility
PlayerStatus_RuneKnockout
PlayerStatus_RuneKing
PlayerStatus_RunePlague
PlayerStatus_RuneSupernova
PlayerStatusSlowed
```

The missing icons codes can be found [HERE](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Files/%5BHudPlayerHealth%5D%20Status%20Icons.txt), simply copy and paste them at the end of our HudPlayerHealth.res

The next step will be adapting the fresh added icons to the hud and in order to do that we can simply copy the "xpos", "ypos", "wide", "tall" values from a icon code that was already present in the hud and make our new icons use the same values!
