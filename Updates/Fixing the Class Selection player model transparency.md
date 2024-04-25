# FIXING THE CLASS SELECTION PLAYER MODEL TRANSPARENCY

![Screenshot](https://raw.githubusercontent.com/Hypnootize/Huds-Update-Guide/master/Images/Transparent_Player.png)

The class selection file is located in **resource/ui/classselection.res**

In order to fix the player model we need to update the `"TFPlayerModel"` section

Simply add

```
"render_texture"		"0"
```

inside `"TFPlayerModel"`, before the `"model"` subkey
