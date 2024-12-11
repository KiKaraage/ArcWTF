# Arc Windows to Firefox / Floorp
For you who want to try new, shiny Arc Browser on Windows! No registration needed, compatible for all Windows versions ✨

Based on [edge-frfox theme by bmFtZQ](https://github.com/bmFtZQ/edge-frfox) | Vertical tab sidebar setup derived from [arcticfox-theme by Sirlan-ff00ff](https://github.com/sirlan-ff00ff/arcticfox-theme).

<b>July 14</b>: Sorry for not updating this theme and for ignoring messages/concerns. I don't think I'm able to maintain this at least until September/October. I just merged previous pull requests -- please make one if you find a bug/clash with new FF update and I will apply it here. Also, I don't think I will update the Floorp theme for now.

Any suggestions or concerns? [Submit new issues](https://github.com/KiKaraage/ArcWTF/issues/new/choose) or [contact me on Reddit](https://www.reddit.com/u/KiKaraage).

## Previews
![Screenshot 1 with tab sidebar pinned](https://github.com/KiKaraage/ArcWTF/assets/10529881/0f280fd2-2049-4ed2-8bf2-41e25f381f65)
![Screenshot 2, new tab panel setup](https://github.com/KiKaraage/ArcWTF/assets/10529881/d9288422-8a54-4493-b90b-56a6ebea4ed5)
![Screenshot 3 with tab sidebar unpinned](https://github.com/KiKaraage/ArcWTF/assets/10529881/aa3b66c2-1aee-46a0-8ad8-14e1320c6508)
![Screenshot 4 with popup searchbar activated](https://github.com/KiKaraage/ArcWTF/assets/10529881/3be1ab66-c9c6-44bc-a557-e26b2136b29d)

## Compability
I modify, made and test this theme on Firefox 123, Windows 10. This theme can work with Linux and MacOS too.

ArcWTF will **clash with the default Firefox system theme**, dark themes that have light toolbar/light URL bar, and light themes with dark toolbar/dark URL bar.

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
* Install [Sidebery](https://github.com/mbnuqw/sidebery) and [Userchrome Toggle](https://addons.mozilla.org/firefox/addon/userchrome-toggle/).
* Open `about:addons`, click 'Userchrome Toggle', go to 'Options' tab.
* Disable 'Display a notification', Go to 'Style Toggle 1', put `|| ` in prefix (should also have the ending space) and apply changes.

  ![Userchrome Toggle settings](https://github.com/KiKaraage/ArcWTF/assets/10529881/dde05450-f53b-497f-8107-865289b3be84)
* Click extension button (puzzle icon), right click on Userchrome Toggle icon, click 'Pin to Toolbar'.

  ![Pin to Toolbar](https://github.com/KiKaraage/ArcWTF/assets/10529881/8a72dc0c-7f40-4d34-a3d3-ca9e8820b127)
* Open Sidebery settings, go to the Style Editor and paste the [CSS config](./sidebery-css-style), or go to Help section and click import [my backup JSON file](./sidebery-ArcWTF.json). Go to Navigation Bar settings and add tab panels to use as Spaces to your liking. _Personally I use History panel as the first item to mimic 'Recently closed' button on Arc so applying custom icon on the CSS config would be easier._
  
![Sidebery navigation bar setting](https://github.com/KiKaraage/ArcWTF/assets/10529881/0471a443-8bff-46f3-9108-41ba6657b2a2)

* <details>
  <summary>Some of my favourites Firefox themes to apply with ArcWTF:</summary>
  
  * [Nord Polar](https://addons.mozilla.org/en-US/firefox/addon/nord-polar/), [Nord Dark](https://addons.mozilla.org/en-US/firefox/addon/nord-dark)
  * [Arc Dark Theme](https://addons.mozilla.org/en-US/firefox/addon/arc-dark-theme-we), [Arc Theme](https://addons.mozilla.org/en-US/firefox/addon/arc-theme-we)
  * [Activist - Soft](https://addons.mozilla.org/en-US/firefox/addon/activist-soft)
  * [Foto - Bold](https://addons.mozilla.org/en-US/firefox/addon/foto-bold)
  * [Plum Torte](https://addons.mozilla.org/en-US/firefox/addon/plum-torte)
  * [Dark Teal (chrome-like)](https://addons.mozilla.org/en-US/firefox/addon/dark-teal-chrome)
</details>
  
<b>(2/3) Applying the CSS theme</b>
  * Download - [for Firefox](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/main.zip); [for Floorp](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/floorp.zip)  - or clone this repo locally
  * Go to `about:profiles`
  * Check 'Root Directory' and click 'Open Folder'/'Show in Finder'
  * Click and open 'chrome' folder (or create the folder if it isn't existed yet)
  * Paste folders and files from this repo to the chrome folder
  * Go to `about:config`, paste `toolkit.legacyUserProfileCustomizations.stylesheets` into the bar and set its value to true/choose Boolean and click + (plus) icon.
  * After that, paste `svg.context-properties.content.enabled` into the bar and set its value to true/choose Boolean and click + (plus) icon.
  * Restart Firefox

 <b>(3/3) How to use this theme?</b>
 * Hover to browser left corner to show the vertical tabs.
 * Right-click navigation toolbar and click 'Customize Toolbar'. Move Userchrome Toggle button to the left position, before back-forward-reload buttons. Put flexible spaces before and after the URL bar. Take a look on screenshots below for guides:
 ![Toolbar configuration for "vertical bar always on"](https://github.com/KiKaraage/ArcWTF/assets/10529881/4928ae8e-55fb-42c3-8295-8748e6ae6a68)
 ![Toolbar configuration for "vertical bar autohide"](https://github.com/KiKaraage/ArcWTF/assets/10529881/40739e9f-0ee5-4165-8460-ec5cdf9e374a)
* Use the Userchrome Toggle to turn sidebar on (fixed positions) or off (autohidden, hover to show tabs).

<b>Bonus!</b> 
| Tweaks | Screenshot |
| --- | --- |
| Replace Firefox icon on Start Menu and Taskbar | ![gambar](https://github.com/KiKaraage/ArcWTF/assets/10529881/3f67829e-91b2-4496-a31c-0d6326478eb4) <br> Download [Arc.ico](https://github.com/KiKaraage/ArcWTF/blob/main/Arc.ico), open `C:\ProgramData\Microsoft\Windows\Start Menu\Programs` directory, right click Firefox shorcut, click 'Properties', click 'Change Icon...' and use the ICO file for maximum Arc feel. Pin to taskbar too. |
| Activate popup search/URL bar launchpad | ![gambar](https://github.com/KiKaraage/ArcWTF/assets/10529881/29bea83d-231a-45d2-8118-769885d87d88) <br> Go to `about:config` and add new Boolean entry: `uc.tweak.popup-search` |
| Hide header sidebar, containing space/tab panel name | Go to `about:config` and add new Boolean entry: `uc.tweak.hide-sidebar-header` |
| Extend sidebar length to 250px (original: 200px) | Go to `about:config` and add new Boolean entry: `uc.tweak.longer-sidebar` |
| Other tweaks (some might've already preapplied here) | Check [bmFtZQ/edge-frfox theme page](https://github.com/bmFtZQ/edge-frfox?tab=readme-ov-file#tweaks) and add to `about:config` |
| Use Segoe UI Variable (Windows 11 default font) as Firefox UI font, as shown on preview screenshots | Download from [CufonFonts](https://www.cufonfonts.com/font/segoe-ui-variable), install and uncomment the related settings on userchrome.css and Sidebery style configurations (sidebery-css-style) |
| Additional addons for theming  | [Adaptive Tab Bar Colour](https://addons.mozilla.org/id/firefox/addon/adaptive-tab-bar-colour/) & [Firefox Color](https://color.firefox.com) [extension](https://addons.mozilla.org/id/firefox/addon/firefox-color) |
 
### Changelogs

<details>
  <summary><b>v1.2-firefox</b> (Feb 29, 2024)</summary>

  * IMPORTANT: Fix missing window controls in FF123+ *credit to bmFtZQ/edge-frfox*
  * NEW: Option to make URL bar popped up like command bar in Arc. Add "uc.tweak.popup-search" in about:config! *credit to Naezr/ShyFox*
  * Improving inactive window behaviour - instead of lighter navbar color, opacity of navbar icons, URL bar and window controls would be decreased. *credit to MrOtherGuy*
  * Improving Sidebery look: Now icons for Sidebery settings, history, and new tab panels are replaced with Fluent icons as used in Arc on Windows
  * Improving Sidebery look: Inactive tab panels would be rendered on smaller size with monochrome colors (depend on theme) to mimic Arc.
  * Improving Sidebery look: New tab button now have similar design to Arc on Windows. It would still exist below all tabs tho, unlike in Arc where new tab button is located after pinned tabs, before regular tabs.
  * Improving Sidebery look: Fixing hidden panels popup layer, now it's correctly popped upwards. And remove dark overlay for all Sidebery popup. *partial credit to cherrynoize*
  * Improving Sidebery look: Fixing pinned tab, now active pinned tabs has light overlay to distinguished it from non-active pinned tabs.
  * Added rounded corners to the devtools. *credit to bmFtZQ/edge-frfox*
  * Added rounded corners to sidebar and sidebar header and fixing sidebar hover flickering. *credit to anoshione, and ishid4 for fixing it*
  * Now showed Space/tab panel name by enabling (and tidying) the sidebar header. *thanks to mbnuqw/Sidebery*
  * Changing unified extensions menu to grid layout.
  * Pre-applied Segoe UI Variable in Firefox UI and Sidebery - Uncomment the respective codes on userchrome.css and Sidebery style editor to activate it. 
</details>
<details> 
  <summary>v1.1-firefox (Feb 13, 2024)</summary>

  * Tab bar is now hidden by default.
  * Rounded corners are now implemented by default. (no about:config entry required)
  * Fix rounded corners issue on some websites, like Twitter/X. _credit to bmFtZQ/edge-frfox_
  * Fix PiP controls not showing. _credit to bmFtZQ/edge-frfox_
  * Fix window controls visibility when hiding the tab bar on Linux. _credit to bmFtZQ/edge-frfox_
  * Fix window controls visibility in fullscreen mode. _credit to bmFtZQ/edge-frfox_
  * Simplified find bar and navigation bar CSS codes.
  * Improved find bar look.
  * Improved in-browser notification look.
  * Adding option to extend sidebar size (from default 200px to 250px) easily: Go to about:config and enable uc.tweak.longer-sidebar (create new Boolean entry)
  * Moved Sidebery navigation bar to bottom. Now Sidebery fully worked like Arc Spaces! _credit to u/themacuser90_
  * Pinned tab width in Sidebery is now resized automatically depend on sidebar size and preferred pinned tabs columns. (I set 3 columns as default, you can customize it from Sidebery Styles Editor)
  * Changed unified extensions menu styling to horizontal-styled list like Microsoft Edge
</details>

### Current Issues/Things to Improve

* Improving Floorp compability.
* Recently added support for translucency in Mac, still on early trial mode. (thanks to artsyfriedchicken)
* Add support to apply MacOS default icons (optional), replacing Fluent icons used on ArcWTF.
* Window controls not working in Private Browsing Mode when tab bar are hidden. Current solution: Don't enable Sidebery and Userchrome Toggle on Private Browsing; the script will automatically show tab bar when you go on Private Browsing Mode. _credit to bmFtZQ/edge-frfox_ _(low priority)_
* Bookmarks bar not showing bookmarks even when enabled. Current solution: Click Menu (Arc logo) > Bookmarks, or use Sidebery bookmarks panel to access bookmarks. _(low priority)_
* Firefox alternative window controls are shown overlapping GTK window controls when using Adaptive Tab Bar Color addon in Linux. Current solution: Install [Browser Adaptation Dynamic Theme](https://github.com/linonetwo/browser-adaptation-dynamic-theme) addon. _credit to LuanderFarias & Enigma1309_

 
### Credits
 * [bmFtZQ - edge-frfox](https://github.com/bmFtZQ/edge-frfox)
 * [ssirlan-ff00ff - arcticfox-theme](https://github.com/sirlan-ff00ff/arcticfox-theme)
 * [The Browser Company](https://arc.net)
 * [Javisperez on SVGRepo - base of sidebar & split tabs icons](https://www.svgrepo.com/collection/toe-basic-line-interface-icons/)
 * [Microsoft - Fluent UI system icons]([https://github.com/aminomancer/uc.css.js/blob/master/uc-extensions.css](https://github.com/microsoft/fluentui-system-icons))
 * [MrOtherGuy - several CSS hacks](https://mrotherguy.github.io/firefox-csshacks/)
 * [DatGuyPiko - compact extensions menu](https://github.com/datguypiko/Firefox-Mod-Blur/tree/master/EXTRA%20MODS/Compact%20extensions%20menu)
 * [mbnuqw - support on Sidebery customizations](https://github.com/mbnuqw/sidebery/issues/1481)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=kikaraage/arcwtf&type=Date)](https://star-history.com/#kikaraage/arcwtf&Date)
