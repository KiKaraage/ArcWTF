# Arc Windows to Firefox / Floorp
Firefox userChrome.css theme to emulate Arc Browser user interface (Windows version).
Based on [edge-frfox theme by bmFtZQ](https://github.com/bmFtZQ/edge-frfox) 

## Previews
![Main screenshot](https://github.com/KiKaraage/ArcFTW/blob/main/screenshot/Screenshot%20(19740).png)


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
  * [Download](https://github.com/KiKaraage/ArcWTF/archive/refs/heads/main.zip) or clone this repo locally
  * Go to `about:profiles`
  * Check 'Root Directory' and click 'Open Folder'/'Show in Finder'
  * Click and open 'chrome' folder (or create the folder if it isn't existed yet)
  * Paste folders and files from this repo to the chrome folder
  * Go to `about:config`, paste `toolkit.legacyUserProfileCustomizations.stylesheets` into the bar and set its value to true`
  * Restart Firefox

 <b>Toolbar configuration to use</b>

First, if you tend to 'toggle the sidebar on' longer and want to center the address bar to the browsing area, use this. Right click "Userchrome Toggle" extension icon, choose Pin to Toolbar, put the button in the left side, and gave flexible spaces
![Toolbar configuration for "vertical bar always on"](https://github.com/KiKaraage/ArcWTF/assets/10529881/4928ae8e-55fb-42c3-8295-8748e6ae6a68)

Or if you use the vertical tab bar less, want to keep it autohide, and prefer put the address bar in the screen center, use this layout
![Toolbar configuration for "vertical bar autohide"](https://github.com/KiKaraage/ArcWTF/assets/10529881/40739e9f-0ee5-4165-8460-ec5cdf9e374a)


  <b>My Firefox advanced configuration</b> (about:config)
  ![My Firefox configuration in Advanced Configurations page](https://github.com/KiKaraage/ArcWTF/assets/10529881/08582e35-e581-4450-b2f8-809ff7116d00)

 The most important one to apply are `uc.tweak.floating-tabs`, `uc.tweak.hide-tabs-bar`, and `uc.tweak.rounded-corners`. 
 
 Check other possible tweaks on [bmFtZQ/edge-frfox theme page](https://github.com/bmFtZQ/edge-frfox?tab=readme-ov-file#tweaks).
