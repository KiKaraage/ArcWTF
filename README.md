# Arc Windows to Firefox / Floorp

### Reworked for Firefox 137+
- Still working on every platform! Windows, Linux and macOS
- Based on current Firefox vertical tabs & sidebar system. (Plus Firefox is working on locally-processed Link Preview and sidebar show on hover!)
- Refined layout compared to past ArcWTF version. Popup URL bar is enabled by default.
- Plus: Now that tab group is available natively, I can provide closer "folder" styling to Arc.
- Plus: You can utilize the Firefox sidebar for "tab splitting" using extensions like Page Sidebar.
- No need to setup Sidebery or Userchrome Toggle, all recommended extensions would be optional.
- Tradeoff: No Spaces. There's no tree-group tabs system. Still no URL bar on the left. (Install Zen! I've made some mods and worked on its documentations.)

## Screenshots
- Hidden sidebar mode

![image](https://github.com/user-attachments/assets/9ba52e06-a818-4b06-bb3c-e45e3ceb0455)
- Expanded sidebar mode

![image](https://github.com/user-attachments/assets/2756f07a-e35d-4199-bc01-5a212ccd94cf)
- "Split view" with Page Sidebar extension

![image](https://github.com/user-attachments/assets/24b3ef65-5d40-4027-8c2f-dc8ce239dcae)
- 9 folder colors available to choose
  
![9 folder icon options](https://github.com/user-attachments/assets/fbddae3a-53c4-4b8c-ad41-8e6c553498a8)

## Applying the theme
- Install latest Firefox, enable Vertical Tabs via right click menu or in Settings
- Download the repo and extract it on your Firefox profile directory (Get the path in `about:profile`. Create the "chrome" folder if you haven't)
- Make sure these **boolean** prefs in `about:config` are enabled/"true":
  - `toolkit.legacyUserProfileCustomizations.stylesheets` to enable user custom styling
  - `svg.context-properties.content.enabled` to enable SVG coloring based on theme.
- Right click toolbar > enter Customize Toolbar mode, move the buttons like this.
![Customize Toolbar layout](https://github.com/user-attachments/assets/7f2f94dd-0907-4737-8567-e3c47756ef90)
- Open the tab sidebar and adjust the length as needed. Also install some supporting extensions below if you want

### Supporting extensions (optional)
1. Use "Split View" in sidebar by using one of these extensions (I already mod the icons!)
  - [Page Sidebar by Stevan VD](https://addons.mozilla.org/en-US/firefox/addon/page-sidebar)
  - [Sidebar Tab by Shailendra](https://addons.mozilla.org/en-US/firefox/addon/sidebar-tab)
  - [Side Browser by Tukapiyo](https://addons.mozilla.org/en-US/firefox/addon/side-browser)
2.  ["Popup window" by Ett Chung](https://addons.mozilla.org/en-US/firefox/addon/popup-window/) or Maxfocus to simulate Peek
3. [Adaptive Tab Bar Color by Eason Wang](https://addons.mozilla.org/en-US/firefox/addon/adaptive-tab-bar-colour) if you like adaptive colors based on websites
4. or [automaticDark by Simon KH Zhang](https://addons.mozilla.org/en-US/firefox/addon/automatic-dark) if you prefer to switch between two specific dark/light themes.
    

### Some optional external tweaks
1. Replace Firefox icon on Windows Start Menu and Taskbar
   ![gambar](https://github.com/KiKaraage/ArcWTF/assets/10529881/3f67829e-91b2-4496-a31c-0d6326478eb4)

   Download [Arc.ico](https://github.com/KiKaraage/ArcWTF/blob/main/Arc.ico), open `C:\ProgramData\Microsoft\Windows\Start Menu\Programs` directory, right click Firefox shorcut, click 'Properties', click 'Change Icon...' and use the ICO file for maximum Arc feel. Pin to taskbar too.
   
2. Use Segoe UI Variable (Windows 11 default font) as Firefox UI font. Download from [CufonFonts](https://www.cufonfonts.com/font/segoe-ui-variable).

   Add this to your userChrome.css: `* {font-family: "Segoe UI Variable Display" !important;}`


### TODOs
- Splitting the userChrome file
- Working on refining the "Tabs on the right" mode
- Making the browser padding gap customizable as variable
- Streamlining context menu options to make it closer to Arc while still maintaining functionality for Firefox
- Transparency support (External help needed, if you've cracked transparency for your OS, reach me out or send a PR!)
- and more...

### CREDITs
* Concept & specific icons from The Browser Company
* Fluent icons from [Microsoft]([https://github.com/aminomancer/uc.css.js/blob/master/uc-extensions.css](https://github.com/microsoft/fluentui-system-icons))
* Fluent icons implementation and menu spacing from [bmFtZQ - edge-frfox](https://github.com/bmFtZQ/edge-frfox)
* Folder icons from [ferrocyante - Arc-H](https://github.com/ferrocyante/Arc-H)
* Better unloaded tabs styling from [Felkazz' Zen Mods collection](https://github.com/Felkazz)
* [Javisperez on SVGRepo - base of sidebar & split tabs icons](https://www.svgrepo.com/collection/toe-basic-line-interface-icons/)
* Past guidance from [MrOtherGuy](https://mrotherguy.github.io/firefox-csshacks/)
* Compact extensions menu (past version) from [DatGuyPiko](https://github.com/datguypiko/Firefox-Mod-Blur/tree/master/EXTRA%20MODS/Compact%20extensions%20menu)

### FF theme recommendations (2024)
  * [Nord Polar](https://addons.mozilla.org/en-US/firefox/addon/nord-polar/), [Nord Dark](https://addons.mozilla.org/en-US/firefox/addon/nord-dark)
  * [Arc Dark Theme](https://addons.mozilla.org/en-US/firefox/addon/arc-dark-theme-we), [Arc Theme](https://addons.mozilla.org/en-US/firefox/addon/arc-theme-we)
  * [Activist - Soft](https://addons.mozilla.org/en-US/firefox/addon/activist-soft)
  * [Foto - Bold](https://addons.mozilla.org/en-US/firefox/addon/foto-bold)
  * [Plum Torte](https://addons.mozilla.org/en-US/firefox/addon/plum-torte)
  * [Dark Teal (chrome-like)](https://addons.mozilla.org/en-US/firefox/addon/dark-teal-chrome)

### FF theme recommendations (2025) - coming soon

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=kikaraage/arcwtf&type=Date)](https://star-history.com/#kikaraage/arcwtf&Date)
