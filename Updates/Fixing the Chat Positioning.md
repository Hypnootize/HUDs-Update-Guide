# FIXING THE CHAT POSITIONING

Since the summer 2020 TF2 update the chat box will no longer be positioned directly from basechat.res by default but instead it will take his vertical positioning values from the **event CompetitiveGame_LowerChatWindow** and **event CompetitiveGame_RestoreChatWindow** lines which can be found inside tf2's default hud animations file.

If we look at the default animations lines we will find

```
event CompetitiveGame_LowerChatWindow
{
	Animate HudChat ypos r140 Accel 0 0
}

event CompetitiveGame_RestoreChatWindow
{
	Animate HudChat ypos 275 Accel 0 0
}
```

where **event CompetitiveGame_LowerChatWindow** lets us move the chat box in a different position exclusively while we are in the match summary screen while **event CompetitiveGame_RestoreChatWindow** will restore the chat positioning to default once we leave the match summary.


### SETTING THE CHAT TO A FIXED POSITION

If we don't feel the necessity of having our chat moved in any situation we can set his positioning to a fixed value by keeping the animation lines empty, this will make it so we can set the "ypos" of our chat directly from basechat.res again!
The animation lines in question should look like this and we can copy and paste them to any huds animation file in order to fix the chat box positioning.

```
event CompetitiveGame_LowerChatWindow
{
}
event CompetitiveGame_RestoreChatWindow
{
}
```
