---
layout: post
title: How to clone A Rejected Expo React Native project.
---

Step 1: delete `android` and `ios` folder.

Step 2: Change the `app.json` file. Change `expo.name`, `expo.slug`. 

You can keep `ios` and `android` configuration. If you delete as bellow to reset app.json to original stage,the CLI will ask you some questions to generate configuration when you run `expo eject`.

```
{
  "expo": {
    "name": "HelloExpo",
    "slug": "my-hello-expo",
    "privacy": "public",
    "sdkVersion": "31.0.0",
    "platforms": [
      "ios",
      "android"
    ],
    "version": "1.0.0",
    "orientation": "portrait",
    "icon": "./assets/images/icon.png",
    "splash": {
      "image": "./assets/images/splash.png",
      "resizeMode": "contain",
      "backgroundColor": "#ffffff"
    },
    "updates": {
      "fallbackToCacheTimeout": 0
    },
    "assetBundlePatterns": [
      "**/*"
    ],
    "ios": {
      "supportsTablet": true
    }
  }

```


Step 3: run command:

```
expo eject
```
