# ADDING WAR PAINT SUPPORT

Let's start by checking if our hud has these two files:

* reource/ui/CharInfoLoadoutSubPanel.res
* reource/ui/econ/InspectionPanel.res

If these two files are not in the hud then we can skip this guide!
While if they are preset we will need to delete or rename **InspectionPanel.res** and update **CharInfoLoadoutSubPanel.res**

To fix the **CharInfoLoadoutSubPanel.res** we need to do 2 things.

First thing let's add the new button for the war paints, we can find the code [HERE](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Files/%5BCharInfoLoadoutSubPanel%5D%20War%20Paints.txt) and as usual lets add it at the end of the file.

Second thing now that our new War Paint button is now on the screen we will need to move the Backpack, Crafting, Catalog and Trading Buttons in order to make space for the new button by using the "xpos" of each on of these elements:

```
"ShowBackpackButton"
"ShowCraftingButton"
"ShowArmoryButton"
"ShowTradeButton"
"ShowPaintkitsButton"
```

Alternatively we can take the already positioning fixed buttons from the [DEFAULT HUD LOADUOUT FILE](https://github.com/Hypnootize/TF2-Default-Hud/archive/master.zip)
