# Auto Hide Discord Channel List
A simple bit of CSS code that hides the channel list when the window is resized. The channel list will reappear when you hover your mouse over the server list.

## Preview
![discord-css-example](https://github.com/user-attachments/assets/0f9b2959-0639-450d-bff5-a74a50a4cab9)

## Code
```css
/* When window is resized */
@media (max-width: 1000px) {

    /* Hide by default */
    [class^="sidebarList_"] {
        width: 0;
        min-width: 0;
    }
    .panel__5dec7,
    .wrapper_e131a9,
    [class^="buttons__"] {
        opacity: 0;
        pointer-events: none;
    }
    
    /* On hover, expand and reveal */
    [class^="sidebar_"]:hover [class^="sidebarList_"] {
        width: 300px;
        min-width: 100px;
    }
    [class^="sidebar_"]:hover .panel__5dec7,
    [class^="sidebar_"]:hover .wrapper_e131a9,
    [class^="sidebar_"]:hover [class^="buttons__"] {
        opacity: 1;
        pointer-events: auto;
    }

    /* Smooth transitions */
    [class^="sidebarList_"],
    .panel__5dec7,
    .wrapper_e131a9,
    [class^="buttons__"] {
        transition: width 0.25s ease, opacity 0.25s ease;   /*Animation speed, and animation interpolation control*/
        overflow: hidden;
        will-change: width, opacity;
    }
}
```

## Instructions
**WARNING!:** This will NOT work in the Discord App, only the website version, or 3rd party clients listed below.

### Web Chrome Extensions (Stylus or Stylebot)
- First, copy the CSS code above.
- To apply the CSS to your browser's website, you'll need an extension that allows you to edit the CSS of the website. Stylus and Stylebot are the one's I've used and they are fairly simple to use.

**Chrome Extension Links**
Stylebot (simplest): https://chromewebstore.google.com/detail/stylebot/

Stylus: https://chromewebstore.google.com/detail/stylus/

(Stylebot)
1. Click the extension icon in your browser.
2. Click the button at the bottom of the window pop up and switch from "Basic" "<> Code"
3. Paste the CSS in the empty text box.

(Stylus)
1. Click the extension icon in your browser.
2. Click "Write style for `https://discord.com/channels/@me`"
3. Replace where it says "*/ Insert code here */" with the CSS code you copied.
4. Click the Save button in the top left of the screen.
5. Click the extension icon again, and make sure the toggle next to the style is enabled.

### 3rd Party Discord Clients (for the Discord app)
**WARNING!:** Using 3rd party clients is technically against Discord's TOS. Use at your own risk.

#### Vencord
https://vencord.dev

Online Theme Link
```
https://raw.githubusercontent.com/JDoinkus/auto-hide-discord-channel-list/refs/heads/main/auto-hide-server-list.theme.css
```

1. Copy the above link.
2. Open Discord.
3. Click the gear icon in the bottom left.
4. In the left menu, find: the "Themes" option under the "Vencord" section.
5. Change the tab from Local Themes to Online Themes Tab at the top of the Window.
6. Paste the link on a new line in the Online Themes text box.

By installing via Online Themes, **future updates to the code will automatically apply**.

If you prefer a **local install** on your machine, follow the below steps for BetterDiscord, but in the Vencord "Local Themes" section.

#### BetterDiscord
https://betterdiscord.app

1. Download the auto-hide-discord-channel-list.css file.
2. Open Discord.
3. Click the gear icon in the bottom left.
4. In the left menu, find: the "Themes" option under the "BetterDiscord" section.
5. Click the button that says "Open Local Themes Folder". This will open your BetterDiscord/Themes folder.
6. Place the .css file in the Themes folder that opened.
7. Enable the theme.
