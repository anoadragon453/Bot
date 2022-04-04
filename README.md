# Sgap Bot

## Installation

Make sure you have a pixel available otherwise it may have issues!

1. Install [Tampermonkey](https://www.tampermonkey.net/)
2. Click here: [https://github.com/Squarific/Bot/raw/master/sgapplace.
   user.js](https://github.com/anoadragon453/Bot/raw/master/sgapplace.user.js). Tampermonkey 
   should offer you to install. Click on **Install**.
3. Reload **r/place** tab. if everything went right you will see "Trying to get 
   Access token..."

### Disadvantages of this bot

- When the bot places a pixel, it looks to yourself as if you can still place a pixel,
  when the bot has already done this for you (so you are in the 5 minute cooldown). The
  cooldown is therefore displayed at the top right of your screen.

## Headless bot

### How to get reddit_session cookie
**NOTE: People have reported that this is annoying to do on chrome because teksts get unselected. Therefore we recommend that you use firefox.**

1. Go to [r/place](https://reddit.com/r/place)
2. Open dev tools and go to the application/storage tab
3. Refresh the page
4. Go to the tab called `Cookies`
5. Copy the value of the `reddit_session` cookie
![image](cookie.jpg)

### Installation instructions

1. Install [NodeJS](https://nodejs.org/).
2. Download the bot via [this link](https://github.com/PlaceNL/Bot/archive/refs/heads/master.zip).
3. Extract the bot anywhere on your desktop
4. Open a command prompt/terminal in this folder
    Windows: Shift+right mousebutton in the folder -> Click on "open Powershell here"
    
    Mac: No clue, sorry!
    
    Linux: Open your file manager to the file manager, right-click and Open in Terminal
5. install the dependencies: `npm i`
6. execute the bot `node bot.js SESSION_COOKIE_HERE`
7. BONUS: You can repeat these steps for any amount of accounts you'd want. Keep in mind to use different accounts.

### Installation Instructions

1. Install [NodeJS](https://nodejs.org/).
2. Download the bot from [this link](https://github.com/anoadragon453/Bot/archive/refs/heads/master.zip).
4. Extract the bot to a folder somewhere on your computer.
5. Open a command prompt/terminal in this folder
    * Windows: Shift + Right mouse button in the folder -> Click on "Open Powershell here"
    * Mac: Really no idea. Sorry!
    * Linux: Right-click in your file manager, look for "Open terminal here"
6. Install the necessary dependencies with `npm i`
7. Start the bot out with `node bot.js ACCESS_TOKEN_HERE`
8. BONUS: You can do the last two steps as many times as you want for additional accounts. Make sure you use other accounts otherwise it won't make much sense. 