# FIXING THE NEW ITEM FOUND PANEL

This fix is only needed if we have a custom item pickup panel, the file in question can be found at **resource/ui/econ/ItemPickupPanel.res** and **ItemDiscardPanel.res**
If these two files are not present, then you can skip this!

This is pretty easy to fix as all we need to do is open **ItemPickupPanel.res** and change the first **"zpos"** in the file from **"100000"** to **"10000"**
Then scroll down until we find **"ItemsFoundLabel"** and change the **"ypos"** from **"20"** to **"30"**

While for the **ItemDiscardPanel.res** we need to add the **"zpos"** **"10000"** to **"item_discard"** (right after the ypos is fine)
then again croll down to **"modelpanel"** and change the **"ypos"** from **"20"** to **"30"**