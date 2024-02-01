# Arc Windows to Firefox / Floorp
Firefox userChrome.css theme to emulate Arc Browser user interface (Windows version).
Based on [edge-frfox theme by bmFtZQ](https://github.com/bmFtZQ/edge-frfox) | Vertical tab sidebar setup from [arcticfox-theme by Sirlan-ff00ff](https://github.com/sirlan-ff00ff/arcticfox-theme), check that if you want to adopt the MacOS style Arc instead.

## Previews
![Screenshot 1 with tab sidebar on](https://github.com/KiKaraage/ArcWTF/assets/10529881/0f3711c7-4841-464f-b5d0-8b78bd4e0402)
![Screenshot 2 with tab sidebar off](https://github.com/KiKaraage/ArcWTF/assets/10529881/4d083837-0b5b-4667-a2cb-3b03068d4527)

## Compability
I modify, made and test this theme on Firefox 122, Windows 10. Based on edge-frfox's compability, it should work on Linux (especially if your window toolbar is on right side) and MacOS.

<details> 
  <summary>For Floorp, there's several incompability I currently have since it might clashed with several parts of the built-in theme they had, like:</summary>
  
* I haven't been able to modify URL font size
* Userchrome Toggle hasn't working yet, so the vertical tab sidebar is either a) autohidden but you can't toggle it to be in fixed position, or b) can be switched on to be shown/hidden, but it can't be automated.
* Advanced configurations from this theme in about:config doesn't worked, so the sidebar tab (either in Sidebery, TST or their default vertical tab) tend to mimic the window background instead of mimicking tab/toolbar background to blend with the toolbar and browser border. So far I can only fix this in Sidebery - you will have to grab toolbar's hex/RGB color and apply it to `--frame-bg` parameter, as shown in screenshots below.
* Hiding tabs bar, turning on browser border frame is applicable only through Floorp's settings instead of through the theme + about:config configurations.
* Otherwise, the theme are working quite well! Split view is available too, but since the devs haven't put the option in right-click context menu, you will have to use their default vertical tab to do it. Though it doesn't look as good as Sidebery.

| Condition | Screenshot |
| --- | --- |
| Original vertical tab bar + Split view | ![gambar](https://github.com/KiKaraage/ArcWTF/assets/10529881/1ca4cadb-146d-499d-9d1c-8d77e50183aa) |
| Original Sidebery (with CSS styling) | ![gambar](https://github.com/KiKaraage/ArcWTF/assets/10529881/8ce5ccc4-cb52-4f48-ac75-4e2c5d699074) |
| Sidebery (with CSS styling) after `--frame-bg` parameter modified, the panel blend better in Floorp | ![gambar](https://github.com/KiKaraage/ArcWTF/assets/10529881/ac47a984-d892-481f-97c2-9fb58407f8be) |

</details>


## Applying the theme
<b>Installing extensions and choosing theme</b>
* Install [Sidebery](https://github.com/mbnuqw/sidebery)
* Open Sidebery settings, go to the Style Editor and paste the [CSS config](docs/sidebery/sidebery-css)
* Install [Userchrome Toggle](https://addons.mozilla.org/id/firefox/addon/userchrome-toggle/) to toggle vertical tab state ('fixed' or 'hidden, hover to show tab sidebar')
* Open `about:addons`, click 'Userchrome Toggle', go to 'Options' tab
* Disable 'Display a notification'
* For the 'Style Toggle 1', put `|| ` in prefix (should also have the ending space) and apply changes
* Use your desired theme. Note that several themes will have clashing colors with  URL bar or sidebar, like the default themes (System default), or dark theme with light address bar, or theme with picture on tab/toolbar. You can also use [Adaptive Tab Bar Colour](https://addons.mozilla.org/id/firefox/addon/adaptive-tab-bar-colour/) or [Firefox Color](https://color.firefox.com) [extension](https://addons.mozilla.org/id/firefox/addon/firefox-color)
  
<b>Applying the CSS theme</b>
  * Download - [for Firefox](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/main.zip); [for Floorp](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/floorp.zip)  - or clone this repo locally
  * Go to `about:profiles`
  * Check 'Root Directory' and click 'Open Folder'/'Show in Finder'
  * Click and open 'chrome' folder (or create the folder if it isn't existed yet)
  * Paste folders and files from this repo to the chrome folder
  * Go to `about:config`, paste `toolkit.legacyUserProfileCustomizations.stylesheets` into the bar and set its value to true`
  * Restart Firefox

 <b>Toolbar configuration to use</b>
 * First, if you tend to 'toggle the sidebar on' longer and want to center the address bar to the browsing area, use this. Right click "Userchrome Toggle" extension icon, choose Pin to Toolbar, put the button in the left side, and gave flexible spaces
 ![Toolbar configuration for "vertical bar always on"](https://github.com/KiKaraage/ArcWTF/assets/10529881/4928ae8e-55fb-42c3-8295-8748e6ae6a68)
 * Or if you use the vertical tab bar less, want to keep it autohide, and prefer put the address bar in the screen center, use this layout
 ![Toolbar configuration for "vertical bar autohide"](https://github.com/KiKaraage/ArcWTF/assets/10529881/40739e9f-0ee5-4165-8460-ec5cdf9e374a)

 <b>Firefox advanced configuration</b> (about:config): The most important parameters to apply on this theme are `uc.tweak.floating-tabs`, `uc.tweak.hide-tabs-bar`, and `uc.tweak.rounded-corners`. Paste those parameters into the bar and set its value to true, one by one.
 
 ![My Firefox configuration in Advanced Configurations page](https://github.com/KiKaraage/ArcWTF/assets/10529881/08582e35-e581-4450-b2f8-809ff7116d00)

 You can check other possible tweaks on [bmFtZQ/edge-frfox theme page](https://github.com/bmFtZQ/edge-frfox?tab=readme-ov-file#tweaks).

<b>Bonus!</b> Download [Arc.ico](https://github.com/KiKaraage/ArcWTF/blob/main/Arc.ico), open `C:\ProgramData\Microsoft\Windows\Start Menu\Programs` directory, right click Firefox shorcut, click 'Properties', click 'Change Icon...' and use the ICO file for maximum Arc feel. Pin to taskbar too. 
 
 ### Credits
 * [bmFtZQ - edge-frfox](https://github.com/bmFtZQ/edge-frfox)
 * [ssirlan-ff00ff - arcticfox-theme](https://github.com/sirlan-ff00ff/arcticfox-theme)
 * [The Browser Company](https://arc.net)
 * [Javisperez on SVGRepo - base of sidebar & split tabs icons](https://www.svgrepo.com/collection/toe-basic-line-interface-icons/)
 * [MrOtherGuy - several CSS hacks](https://mrotherguy.github.io/firefox-csshacks/)
 * [Aminomancer - Extension icon replacement tweak](https://github.com/aminomancer/uc.css.js/blob/master/uc-extensions.css)
 * [DatGuyPiko - Compact extensions menu](https://github.com/datguypiko/Firefox-Mod-Blur/tree/master/EXTRA%20MODS/Compact%20extensions%20menu)

### Issues to Solve
- [x] Replacing Firefox menu SVG with Arc icon
- [x] Reformatting Arc, sidebar and split tab icons so they can adapt well to themes
- [ ] Improving buttonbox (window controls) so that it can be hidden on fullscreen but can be summoned when corner area is hovered
- [ ] Improving theme compability with Floorp (low priority, but it's already usable)
