# YouTube for Alexa
**Unofficial YouTube skill for Alexa**

## Features
* Play audio (currently no video) from YouTube videos
* Live videos are supported as much as possible
* Works in 5 languages, thanks to everyone who helped!

## Skill Commands

1. Play a video, eg "Alexa, ask YouTube to play Gangnam Style"
2. Play a playlist, eg "Alexa, ask YouTube to play playlist Ultimate Beyonce"
3. Play a channel, eg "Alexa, ask YouTube to play channel Fall Out Boy Vevo"
4. You can replace "play" with "shuffle" to get a randomized version of the search results/channel/playlist, eg "Alexa, ask YouTube to shuffle channel Nicki Minaj"
5. Next / Previous / Start Over / Pause / Resume should all work
6. Ask what is playing by "Alexa, ask YouTube what song is playing" (or just "Alexa, can you repeat that?" should tell you)

## Known issues

1. Some videos just fail, it's not clear why, they work locally. The skill just moves to the next video on the playlist, but this can mean sometimes she announces a video that doesn't play.
2. It doesn't play video, because I don't have an Echo Show or Echo Spot to test on. If you want to buy me one, get in touch!

## Setup Instructions

1. Go to the Alexa Console (https://developer.amazon.com/alexa/console/ask)
2. If you have not registered as an Amazon Developer then you will need to do so. Fill in your details and ensure you answer "NO" for "Do you plan to monetize apps by charging for apps or selling in-app items" and "Do you plan to monetize apps by displaying ads from the Amazon Mobile Ad Network or Mobile Associates?"
3. Once you are logged into your account click "Create Skill" on the right hand side.
4. Give your skill any name, eg "My YouTube Skill", and click "Next". Set the language to whatever your Alexa is set to, but currently English (any), French, Italian, German and Spanish (any) can be supported.
5. Choose "Custom" as your model, and click "Create Skill".
6. On the left hand side, click "JSON Editor".
7. Delete everything in the text box, and copy in the text from https://raw.githubusercontent.com/swapnilbansal1/Alexa-youtube/master/InteractionModel_en.json
8. Click "Save Model" at the top.
9. Click "Interfaces" in the menu on the left, and enable "Audio Player". Click "Save Interfaces".
10. Click "Endpoint" in the menu on the left, and select "AWS Lambda ARN". Under "Default Region", put:

```
arn:aws:lambda:eu-west-1:175548706300:function:YouTube
```

11. Click "Save Endpoints"
12. Click "Invocation" in the menu on the left.
13. If you want to call the skill anything other than "youtube", change it here. Click "Save Model" if you change anything.
14. Click "Build Model". This will take a minute, be patient. It should tell you if it succeeded.
15. At the top, click "Test".
16. Move the slider at the top left so that it says "Test is enabled for this skill".

That's it!


**Special thanks to @ndg63276 for PyTube!
