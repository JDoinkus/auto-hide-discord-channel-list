# Auto Hide Discord Channel List
A simple bit of CSS code that will hide the server list when the window is resized until hovered.

## Preview
![discord-css-example](https://github.com/user-attachments/assets/0f9b2959-0639-450d-bff5-a74a50a4cab9)

## Code
```css
@media (max-width: 1000px) {
    /* Default (hidden) */
    .sidebarList_c48ade {
        width: 0;
        min-width: 0;                                /* Prevents Discord from forcing a width.*/
    /* smooth animation */
    }
    .buttons__37e49 {
        display: none;                               /* Hide buttons by profile.*/
    }

    /* On hover of parent, expand */
    .sidebar_c48ade:hover .sidebarList_c48ade {
        width: 300px;                                /*Or whatever width you want.*/
        min-width: 100px;
    }  
    .sidebar_c48ade:hover .buttons__37e49 {
        display: contents;
    }
}

/* Smooth transition control */
.sidebarList_c48ade {
    overflow: hidden;                               /*Hides inner content while closed */
    transition: width 0.25s ease;                   /*Animation speed, and animation interpolation control.*/
}
```

This is just a simple bit of CSS code and can be applied in many ways.

## Instructions

### Web Chrome Extensions (Stylus or Stylebot)

First, copy the CSS code above.

(Stylus)
1. Click the extension icon in your browser.
2. Click "Write style for `https://discord.com/channels/@me`"
3. Replace where it says "*/ Insert code here */" with the CSS code you copied.
4. Click the Save button in the top left of the screen.
5. Click the extension icon again, and make sure the toggle next to the style is enabled.

(Stylebot)
1. Click the extension icon in your browser.
2. Click the button at the bottom of the window pop up and switch from "Basic" "<> Code"
3. Paste the CSS in the empty text box.

### 3rd Party Discord Clients (for the Discord app)

#### Vencord

Online Theme Link
```
https://raw.githubusercontent.com/JDawgtor/auto-hide-discord-channel-list/refs/heads/main/auto-hide-server-list.theme.css
```

1. Copy the above link.
2. Open Discord.
3. Click the gear icon in the bottom left.
4. In the left menu, find: the "Themes" option under the "Vencord" section.
5. Change the tab from Local Themes to Online Themes Tab at the top of the Window.
6. Paste the link on a new line in the Online Themes text box.

By installing via Online Themes, any new updates to the code will automatically apply.

If you prefer to be installed locally on your machine, follow the below steps for BetterDiscord, but in the Vencord "Local Themes" section.

#### BetterDiscord

1. Download the auto-hide-discord-channel-list.css file.
2. Open Discord.
3. Click the gear icon in the bottom left.
4. In the left menu, find: the "Themes" option under the "BetterDiscord" section.
5. Click the button that says "Open Local Themes Folder". This will open your BetterDiscord/Themes folder.
6. Place the .css file in the Themes folder that opened.
7. Enable the theme.
