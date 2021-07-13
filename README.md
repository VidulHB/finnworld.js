*NPM:** [npmjs.com/package/finnworld.js](https://www.npmjs.com/package/finnworld.js/)<br>


<a href="https://www.npmjs.com/package/finnworld.js/"><img src="https://img.shields.io/npm/v/disbotlist.svg?maxAge=3600" alt="NPM version" /></a>
<a href="https://www.npmjs.com/package/finnworld.js"><img src="https://img.shields.io/npm/dt/disbotlist.svg?maxAge=3600" alt="NPM downloads" /></a>


<a href="https://nodei.co/npm/finnworld.js"><img src="https://nodei.co/npm/finnworld.js.png?downloads=true&stars=true" alt="npm installnfo" /></a>


## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://discord.gg/qNVHMzRsJ9) address.*
- `npm i finnworld.js`

#### 1. What Is FinnWorld 
    Ans: Finnrorld Is The Discord Bot List Created By Chinmay Jha#1234 and Vidul.H.B#1111 

#### 2. How do I install it?
  Ans: JavaSciprt: npm i disbotlist or npm install disbotlist
            Python: pip install disbotlist

#### 3. Does it have any GitHub Repository?
  Ans: Yes It Is [Here](https://github.com/VidulHB/finnworld.js)

#### 4. What is it's uses?
  Ans: To get the daily vote count, server count and information about your bot.
Examples:  avatar, botID, discriminator, shortDescription, prefix, votes, serverCount, ownerID, owner, co-owners, tags, longDescription, certificate etc.

#### 5. How can I get my bot's server count?
  `Ans: JavaScript:`
```js
const finnworld = require("finnworld.js");
const dbl = new finnworld("TOKEN-HERE", client);
                  ^--- this token is not the token you get from discord its the token you get from our website

client.on("ready", async () => {
  dbl.serverCount();
  console.log("Server count posted")

```
 

#### 6. How can I get my bot's vote count?
  `Ans:`
```js
let hasVote = await dbl.hasVoted("Your-bot-id");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("Your-bot-id")
  console.log(search)

```

#### 7. Full Example?
  `Ans:`
```js
const finnworld = require("finnworld.js");
const dbl = new finnworld("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("your-bot-id");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("Your-bot-id")
  console.log(search)

  /* SearchResults
  {
    avatar: '',
    botID: '',
    username: '',
    discrim: '',
    shortDesc: '',
    prefix: '! [changable]',
    votes: 31,
    ownerID: '',
    owner: '',
    coowners: [ '' ],
    tags: [ 'Moderation', 'NSFW', 'Music' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});

```
