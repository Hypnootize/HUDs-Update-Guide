# FIXING THE MAIN MENU

**IF YOU DON’T REALLY CARE ABOUT HAVING A CUSTOM MAIN MENU THE EASIEST WAY IS TO REMOVE GAMEMENU.RES AND MAINMENUOVERRIDE.RES AND SKIP THIS SECTION!**

*This is for sure the hardest part of this update as it includes a lot of editing based on the hud we want to update. Every menu is different and needs different customizations so I’ll explain this in the most generic way possible.*

## GETTING RID OF DEAD BUTTONS

The first thing I usually do is removing the Casual, Comp, MvM buttons that became useless after the jungle inferno update.
To do that we need to edit both MainMenuOverride.res and GameMenu.res and remove all the codes related to the buttons.

I really suggest to start from the GameMenu.res and identify the three buttons in question.
A lot of times they might have different names, but usually we need to get rid of any button called:

* QuickPlayButton / QuickPlayChangeButton / CasualButton
* PlayPVEButton / MvMButton
* CompetitiveButton

After we know what buttons needs to be removed we can delete the code from both GameMenu.res and MainMenuOverride.res, THEY ALWAYS HAVE THE SAME NAME IN BOTH FILES!

Now that we have some empty space we are free to adjust the other working buttons inside the MainMenuOverride.res by moving them around with "xpos" and "ypos".
Or we could cover the empty space by adding the new RankPanel and Badge like explained later!

## FIXING UNCLICKABLE BUTTONS

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Broken_Button.png)

Let’s open our MainMenuOverride.res and what we need to do is add a new line to the Message Of The Day and Notification codes that are already there.
The line we will ad is **"actionsignallevel" "2"**

Now inside our MainMenuOverride.res let’s search for **Notifications_ShowButtonPanel_SB** and just after **"default" "1"** we add the new **"actionsignallevel" "2"** Line.
It should then look something like this:

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Fixing_Buttons.png)

We need to repeat this for these other codes:

* Notifications_ShowButtonPanel_SB
* MOTD_ShowButtonPanel_SB
* MOTD_CloseButton
* MOTD_URLButton
* MOTD_PrevButton
* MOTD_NextButton
* Notifications_CloseButton

If you did that correctly, you should now be able to click on the Notification and MOTD buttons successfully!

## ADDING THE NEW FEATURES

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Badge.png)

First of all lets copy the new codes from [HERE](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Files/%5BMainMenuOverride%5D%20Additions.txt) and add them to our MainMenuOverride.res
We can paste all of the text just after the "SaxxySettings" code as shown here:

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Menu_Codes.png)

By importing these codes, we added:

* Twitch streams button ("WatchStreamButton")
* Contracker Button ("QuestLogButton")
* Steam FriendList ("FriendsContainer")
* Name Rank and Level ("RankPanel" and can be edited by using PvPRankPanel.res)
* Rank Badge ("RankModelPanel")
* Casual/Comp toggle button ("CycleRankTypeButton")

You can edit the xpos, ypos and the other values for each of these new codes in order to get them wherever you want in the menu and change their look!
Sadly, each menu is different so I can’t really help on that, but I’ll leave these [2 PRESETS](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Files/%5BMainMenuOverride%5D%20Friend%20Panel%20Presets.txt) for the Steam Friendlist here, both work by default with any hud :)

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Friends_Right.png)
![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Friends_Bottom_Right.png)
