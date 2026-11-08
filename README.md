# Retro cosmetic picker

A separate retro edition with two deliberately ugly neon buttons: **Skins** and **Avatar**.

- The buttons and open window bounce around the screen. Movement continues while the mouse hovers over the UI. It pauses only during active dragging or typing.
- A short bonk plays on each screen-edge bounce. A corner hit makes one bonk; hidden or unloaded UI stays silent.
- Menu buttons and text fields make a short pop when clicked.
- The supplied startup audio plays once, followed by the supplied spinning image and classic Batman transition. The image then disappears.
- Skins includes Guns and Melees. Avatar uses a Roblox user ID, with Apply, Restore, and Unload controls.
- Misc, presets, and individual shirt/pants/hat inputs are removed.
- RightShift hides/reopens the entire interface; a previously saved menu key is respected. Hiding also ends the intro effects.
- Close hides the current window. On touch devices, a two-finger tap can reopen a hidden interface.
- Unload and re-execution clean up sounds, animation callbacks, and temporary UI.

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/csoldschool/el-criminality/cc5f5202a712ceb73962b9f87d5daed44e1010bb/SkinAvatarRetro.luau"))()
```

Media is bundled into the script and cached locally using writefile and getcustomasset (or getsynasset). Executors without these APIs retain the menu but cannot play/display the custom media. The startup file was an MP4 despite its extension; its audio was converted to MP3.

Batman transition source: [Classic Batman Transition on Myinstants](https://www.myinstants.com/en/instant/classic-batman-transition/). The click pop and bounce bonk are synthesized locally during packaging.

Compilation, media decoding, and local mock checks passed for cosmetics, avatar appearance, menu movement, audio sequencing, hiding, and cleanup. Live Roblox rendering and executor audio playback have not been verified.
