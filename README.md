# Smart Mirror

[![Join the chat at https://gitter.im/evancohen/smart-mirror](https://badges.gitter.im/evancohen/smart-mirror.svg)](https://gitter.im/evancohen/smart-mirror?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This project is inspired by [HomeMirror](https://github.com/HannahMitt/HomeMirror) and Michael Teeuw's [Magic Mirror](http://michaelteeuw.nl/tagged/magicmirror). It uses [annyang](https://github.com/TalAter/annyang) for voice interactivity, [electron](http://electron.atom.io/) to make it cross platform, and integrates with Philips Hue. It is my own take on what a "smart mirror" can be.

[See it in action (Video)](https://www.youtube.com/watch?v=PDIbhV8Nvq8)

#### Why start from scratch?
Starting from scratch was less about other projects not being good enough and more about my own learning experience. While I did get a lot of inspiration from other projects I really wanted to see how much further I could take things.

#### Gitter:
A live chat to get help and discuss mirror related issues: https://gitter.im/evancohen/smart-mirror. Currently I'm the only one monitoring this, so don't expect an instantanious response. If I'm not online you are probubly better off [filing an issue](https://github.com/evancohen/smart-mirror/issues/new).

### Getting Started
#### Hardware Components
- Raspberry Pi 2
- USB Microphone (Or Webcam w/ microphone)
- Monitor (with the bezel removed)
- Mirror Pane (aka Observation Glass)
- Philips Hue

#### Installation
In order to get started I suggest a clean install of Raspbian. You can snag a fresh copy of Jessie (recommended, it's the future) or Wheezy from the [Raspbian Download Page](https://www.raspberrypi.org/downloads/raspbian/).

You'll also need to install Node (v4.0.0+) which now comes bundled with npm.

##### Getting the code
Next up you'll want to clone this repository onto your Pi if you haven't already yet
```
git clone https://github.com/evancohen/smart-mirror.git
```

##### Setting up the configuration
Done? Excellent, let's continue.

Time to update the config file... You'll need to fill in two things into `js/config.js`:

1. A [Forecast API key](https://developer.forecast.io/) (don't worry it's free)
2. Philips Hue Bridge IP address with a configured user. Details about how to set this up in the [Philips Hue Developer Documentation](http://www.developers.meethue.com/documentation/getting-started)

The format of your config should look something like this:
```
var FORCAST_API_KEY = "a6s5dg39j78qj38sjs91je9djadfa1e";
var HUE_BASE = "http://192.168.1.99/api/as9234ho0dfhoq01f2as3yh4m0/";
```

##### Install dependencies and run
Before we can run the thing we've got to install the projects dependencies. From the root of the `smart-mirror` directory run:
```
npm install
```

This will take a minute, it has to download [electron-prebuilt](https://github.com/mafintosh/electron-prebuilt). Once that is done you can launch the mirror with
```
npm start
```

#### Development
To launch the mirror with a debug window attached use the following command:
```
npm start dev
```
More info coming soon(ish). In the meantime head over to the [gitter chat](https://gitter.im/evancohen/smart-mirror) for help. 

#### Troubleshooting
If you are having trouble getting a USB microphone to work on your Pi try following [these steps](https://github.com/evancohen/smart-mirror/issues/20)

### License:
MIT

### More info:
Favicon from [In the Wake of the King](http://walkingmind.evilhat.com/2014/03/17/in-the-wake-of-the-king/), a head nod to **The Watcher** – "A byblow of the king and a queen of the sea, she has remained apart from the workings of her family, more home beneath the waves, watching all through water and mirror. Her ambitions lie outside the Eternal Kingdom, but her secrets are valuable everywhere."

Awesome.
