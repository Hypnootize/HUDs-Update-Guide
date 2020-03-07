# UPDATING THE CLIENTSCHEME

The clientscheme is pretty much the heart of the hud as it is the file that contains all the colors, fonts and borders used in the whole hud.

*I managed to get a pretty accurate list of all the colors/fonts/borders that got added with each update.*
*Obviously if the hud we are working on is pretty recent it probably already got most of them!*

## Colors

[HERE](https://raw.githubusercontent.com/Hypnootize/Hud-Update-Guide/master/Files/[Clientscheme]%20New%20Colors.txt) we can find the file with all the new colors added with the updates through the years.

All we need to do is copy the colors and paste them in the colors section of our ClientScheme.res
I suggest to add them at the start of the colors section like shown, that way if a customized color with the same name was already present in the file it wont get replaced!

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Adding_Colors.png)

## Fonts

[HERE](https://raw.githubusercontent.com/Hypnootize/Hud-Update-Guide/master/Files/[Clientscheme]%20New%20Fonts.txt) we can find the file with all the new fonts added with the updates through the years.

Again lets copy the fonts and paste them in the fonts section of our ClientScheme.res
As before I suggest to add them at the start of the fonts section like shown, that way if a customized font with the same name was already present in the file it wont get replaced!

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Adding_Fonts.png)

## Borders

[HERE](https://raw.githubusercontent.com/Hypnootize/Hud-Update-Guide/master/Files/[Clientscheme]%20New%20Borders.md) we can find the file with all the new borders added with the updates through the years.

Again lets copy the borders and paste them in the borders section of our ClientScheme.res
As before I suggest to add them at the start of the borders section like shown, that way if a customized border with the same name was already present in the file it wont get replaced!

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Adding_Borders.txt)

For the borders we got one more step which is replacing the old outdated item borders, used on the backpack and loadout, with the new ones.

In order to do that lets first copy the new borders from this file [HERE](https://raw.githubusercontent.com/Hypnootize/Hud-Update-Guide/master/Files/[Clientscheme]%20Item%20Borders.txt)
Next inside our clientscheme's border section we will need to select the text from **EconItemBorder** until we reach the **}** before **StoreItemBorder** 
Once that section is selected go ahead and replace it with the previously copied text of the new borders!


*The clientscheme should now be fully updated*