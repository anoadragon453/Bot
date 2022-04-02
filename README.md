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
### Nadelen van deze bot

- Wanneer de bot een pixel plaatst, ziet het er voor jezelf uit alsof je nog steeds een pixel kunt plaatsen, terwijl de bot dit al voor je heeft gedaan (en je dus in de 5 minuten cooldown zit). De cooldown wordt daarom rechtsbovenin je scherm weergegeven.

## Headless bot

### Je access token verkrijgen
1. Ga naar [r/place](https://www.reddit.com/r/place/)
2. Open de browser console (F12/Element inspecteren -> Click op console)
3. Plak de volgende code en druk op enter:
```
async function getAccessToken() {
	const usingOldReddit = window.location.href.includes('new.reddit.com');
	const url = usingOldReddit ? 'https://new.reddit.com/r/place/' : 'https://www.reddit.com/r/place/';
	const response = await fetch(url);
	const responseText = await response.text();

	return responseText.split('\"accessToken\":\"')[1].split('"')[0];
}

await getAccessToken()
```
4. De tekst tussen de quotes (`"`) is je access token.

### Installatieinstructies

1. Installeer [NodeJS](https://nodejs.org/).
2. Download de bot via [deze link](https://github.com/PlaceNL/Bot/archive/refs/heads/master.zip).
3. Pak de bot uit naar een folder ergens op je computer.
4. Open een command prompt/terminal in deze folder
    Windows: Shift+Rechter muis knop in de folder -> Click op "Powershell hier openen"
    Mac: Echt geen idee. Sorry!
    Linux: Niet echt nodig toch?
5. Installeer de nodige depdendencies met `npm i`
6. Voor de bot uit met `node bot.js ACCESS_TOKEN_HIER`
7. BONUS: Je kunt de laatse twee stappen zo vaak doen als je wil voor extra accounts. Let wel op dat je andere accounts gebruikt anders heeft het niet heel veel zin.
