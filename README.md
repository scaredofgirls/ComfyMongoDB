# ComfyMongoDB
Easiest way to setup MongoDB! Run a full-fledged MongoDB server with one line of code. No download or setup. Just, `require("comfy-mongo")();`

For those of us that don't want to download and install MongoDB on the computer or want a self-contained version inside a limited directory, **ComfyMongoDB** lets you start up a full MongoDB service ***SUPER EASILY*** in just one line of code.

## Instafluff ##
> *For more coding fun like this Comfy MongoDB Module, come and hang out with us at the Comfiest Corner on Twitch!*

> https://twitch.tv/instafluff

> https://twitter.com/instafluffTV

## Instructions ##
1. Install `comfy-mongo`
```
npm install comfy-mongo --save
```

2. Start MongoDB and listen for events
```javascript
var ComfyMongo = require("comfy-mongo")();
ComfyMongo.on( "ready", () => {
  console.log( "MongoDB is ready!" );
});
```

## MongoDB Version ##

ComfyMongoDB currently runs MongoDB Community Edition v4.0.10

## Connection ##

The MongoDB server will start on port `27017` and can be connected to with the url: `mongodb://localhost:27017`

For an example connection, take a look at `example.js`!

## Events ##

Currently, the MongoDB events available are:

- **ready**`ComfyMongo.on( "ready", () => {} )`
    - MongoDB is ready for connections
- **output**`ComfyMongo.on( "output", ( data ) => {} )`
    - Stdout output stream
- **error**`ComfyMongo.on( "error", ( err ) => {} )`
    - Stderr output stream
- **close**`ComfyMongo.on( "close", ( code ) => {} )`
    - MongoDB has exited/closed with status code

## Supported Platforms ##

ComfyMongoDB currently works in Windows and Mac/OSX.

## How to Specify Your Own Database Directory ##

ComfyMongoDB defaults to `./data` for storage.

To specify your own data directory, you can pass the file path in as a parameter:
```javascript
var ComfyMongo = require("comfy-mongo")( "./MyCustomDirectory" );
```
