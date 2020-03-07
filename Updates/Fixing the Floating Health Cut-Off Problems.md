# FIXING THE FLOATING HEALTH CUT-OFF PROBLEMS

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Floating_Health.png)

We are looking at **resource/ui/HealthIconPanel.res** if the file is missing in our hud we can take it from the [DEFAULT HUD FILES](https://github.com/Hypnootize/TF2-Default-Hud/archive/master.zip) as always

After we added the file to our hud we can join an offline server and spawn a bot to edit the floating number.
We need to work with both **"wide"** and **tall"** of **"HealthIcon"** until the number is completely visible and centered with the body.

Note that the floating heath is only visible if *tf_hud_target_id_disable_floating_health* is set to *0*.