# FIXING THE CHARINFOPANEL AND STOREPANEL TABS

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Loadouts_Tabs.jpg)

**This fix is only needed if the resource/ui/CharInfoPanel.res and resource/ui/econ/store/v2/StorePanel.res files are present in the hud.**

Let's open both files and scroll down until we find the **"Sheet"** code

Once found we want to add this new line to it **"yoffset" "14"** (can be added right after **"transition_time"**)
Then change his value from 14 to whatever number is needed to show the tabs entirely.

Its also possible to resize the tab by using **"tabwidth"** & **"tabheight"** and change his font by editing the **"tabskv"** font.