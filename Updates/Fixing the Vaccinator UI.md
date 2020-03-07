# FIXING THE VACCINATOR UI

We are working on **resource/ui/HudMedicCharge.res**

[HERE](https://raw.githubusercontent.com/Hypnootize/Hud-Update-Guide/master/Files/[HudMedicCharge]%20Vaccinator.txt) is the new codes we need to add at the end of our HudMedicCharge.res

## Fixing the charge bars

First I would suggest getting the new charge bars in the desired position by using the **"xpos" "ypos" "wide" and "tall"** of each one of the bars we just added **"ChargeMeter1" "ChargeMeter2" "ChargeMeter3" "ChargeMeter4"**

*They might be out of the screen (invisibles) depending on what are the general positioning values of the HudMedicCharge.res file we are updating, so if that is the case we can set the "xpos" and "ypos" of "ChargeMeter1" both to 0 and that should make at least the first bar visible.*

## Resistance icon

Last thing is the resistance icon positioning ![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Resistance.png), again to move it we are going to use the "xpos" and "ypos" of "ResistIconAnchor".
If we want to resize it, we need to change the "wide" and "tall" values of "ResistIcon", keep in mind they need to be the same or it will look really bad.