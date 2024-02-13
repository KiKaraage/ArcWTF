# Arc Windows to Firefox / Floorp
For you who want to try new, shiny Arc Browser on Windows! No registration needed, compatible for all Windows versions ✨

Based on [edge-frfox theme by bmFtZQ](https://github.com/bmFtZQ/edge-frfox).

Vertical tab sidebar setup derived from [arcticfox-theme by Sirlan-ff00ff](https://github.com/sirlan-ff00ff/arcticfox-theme).

Any suggestions or concerns? [Submit new issues](https://github.com/KiKaraage/ArcWTF/issues/new/choose) or [contact me on Reddit](https://www.reddit.com/r/FirefoxCSS/comments/1acgx8c/arcftw_attempt_to_replicate_arc_browser_sleek/).

## Previews
![Screenshot 1 with tab sidebar on](https://github.com/KiKaraage/ArcWTF/assets/10529881/58260699-1373-4532-b29e-2a6133008618)
![Screenshot 2 with tab sidebar off](https://github.com/KiKaraage/ArcWTF/assets/10529881/a31d486b-5dbd-4a50-83aa-0598d28102ae)

## Compability
I modify, made and test this theme on Firefox 122, Windows 10. Based on edge-frfox's compability, this theme can work with Linux and MacOS too.

ArcWTF will clash with the default Firefox system theme, dark themes that have light toolbar/light URL bar, and light themes with dark toolbar/dark URL bar.

Vertical tabs are currently disabled in Private Browsing Mode due to behaviour clashes with window controls.

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
<b>(1/3) Installing addons and choosing theme</b>
* Install [Sidebery](https://github.com/mbnuqw/sidebery) and [Userchrome Toggle](https://addons.mozilla.org/id/firefox/addon/userchrome-toggle/).
* Open `about:addons`, click 'Userchrome Toggle', go to 'Options' tab.
* Disable 'Display a notification', Go to 'Style Toggle 1', put `|| ` in prefix (should also have the ending space) and apply changes.
* Click extension button (puzzle icon), right click on Userchrome Toggle icon, click 'Pin to Toolbar'.
* Open Sidebery settings, go to the Style Editor and paste the [CSS config](sidebery/sidebery-css).
* Additional addons for theming: [Adaptive Tab Bar Colour](https://addons.mozilla.org/id/firefox/addon/adaptive-tab-bar-colour/) & [Firefox Color](https://color.firefox.com) [extension](https://addons.mozilla.org/id/firefox/addon/firefox-color)
  
<b>(2/3) Applying the CSS theme</b>
  * Download - [for Firefox](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/main.zip); [for Floorp](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/floorp.zip)  - or clone this repo locally
  * Go to `about:profiles`
  * Check 'Root Directory' and click 'Open Folder'/'Show in Finder'
  * Click and open 'chrome' folder (or create the folder if it isn't existed yet)
  * Paste folders and files from this repo to the chrome folder
  * Go to `about:config`, paste `toolkit.legacyUserProfileCustomizations.stylesheets` into the bar and set its value to true`
  * Restart Firefox

 <b>(3/3) How to use this theme?</b>
 * Hover to browser left corner to show the vertical tabs.
 * Right-click navigation toolbar and click 'Customize Toolbar'. Move Userchrome Toggle button to the left position, before back-forward-reload buttons. Put flexible spaces before and after the URL bar. Take a look on screenshots below for guides:
 ![Toolbar configuration for "vertical bar always on"](https://github.com/KiKaraage/ArcWTF/assets/10529881/4928ae8e-55fb-42c3-8295-8748e6ae6a68)
 ![Toolbar configuration for "vertical bar autohide"](https://github.com/KiKaraage/ArcWTF/assets/10529881/40739e9f-0ee5-4165-8460-ec5cdf9e374a)
* Use the Userchrome Toggle to turn sidebar on (fixed positions) or off (autohidden, hover to show tabs).

<b>Bonus!</b> 
* <b>Replace Firefox icon on Start Menu and Taskbar</b>: Download [Arc.ico](https://github.com/KiKaraage/ArcWTF/blob/main/Arc.ico), open `C:\ProgramData\Microsoft\Windows\Start Menu\Programs` directory, right click Firefox shorcut, click 'Properties', click 'Change Icon...' and use the ICO file for maximum Arc feel. Pin to taskbar too.
* <b>Check interesting tweaks</b> from [bmFtZQ/edge-frfox theme page](https://github.com/bmFtZQ/edge-frfox?tab=readme-ov-file#tweaks) - Some of them are already pre-applied in ArcWTF.
 
 ### Credits
 * [bmFtZQ - edge-frfox](https://github.com/bmFtZQ/edge-frfox)
 * [ssirlan-ff00ff - arcticfox-theme](https://github.com/sirlan-ff00ff/arcticfox-theme)
 * [The Browser Company](https://arc.net)
 * [Javisperez on SVGRepo - base of sidebar & split tabs icons](https://www.svgrepo.com/collection/toe-basic-line-interface-icons/)
 * [MrOtherGuy - several CSS hacks](https://mrotherguy.github.io/firefox-csshacks/)
 * [Aminomancer - Extension icon replacement tweak](https://github.com/aminomancer/uc.css.js/blob/master/uc-extensions.css)
 * [DatGuyPiko - Compact extensions menu](https://github.com/datguypiko/Firefox-Mod-Blur/tree/master/EXTRA%20MODS/Compact%20extensions%20menu)
