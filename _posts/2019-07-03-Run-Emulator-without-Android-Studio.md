---
title: Run AVD Emulator without Android Studio
template: post
---

```bash

cd ${ANDROID_HOME}/emulator

# List available emulator
./emulator  -list-avds

# Run it
 ./emulator -avd Pixel_2_API_28

```

Short way:

```
${ANDROID_HOME}/emulator/emulator -avd Pixel_2_API_28

```
