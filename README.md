# Sgap Bot

## Installatieinstructies

## Installation

Make sure you have a pixel available otherwise it will fuck up!

1. Install [Tampermonkey](https://www.tampermonkey.net/)
2. Click here: [https://github.com/Squarific/Bot/raw/master/sgapplace.
   user.js](https://github.com/anoadragon453/Bot/raw/master/sgapplace.user.js). Tampermonkey 
   should offer you to install. Click on **Install**.
3. Reload **r/place** tab. if everything went right you will see "Trying to get 
   Access token..."

### Disadvantages of this bot

- When the bot places a pixel, it looks to yourself as if you can still place a pixel, when the bot has already done this for you (so you are in the 5 minute cooldown). The cooldown is therefore displayed at the top right of your screen.

## Headless bot

### Obtain your access token
1. Go to [r/place](https://www.reddit.com/r/place/)
2. Open the browser console (F12/Inspect element -> Click on console)
3. Paste the following code and press enter:

```js
async function getAccessToken() {
	const usingOldReddit = window.location.href.includes('new.reddit.com');
	const url = usingOldReddit ? 'https://new.reddit.com/r/place/' : 'https://www.reddit.com/r/place/';
	const response = await fetch(url);
	const responseText = await response.text();

	return responseText.split('\"accessToken\":\"')[1].split('"')[0];
}

await getAccessToken()
```

4. The text between the quotes (`"`) is your access token.

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