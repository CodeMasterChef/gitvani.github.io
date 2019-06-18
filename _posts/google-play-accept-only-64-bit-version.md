---
layout: post
title: Google Play accept only 64-bit version
---

Starting from August 1, 2019 Google Play will accept only 64-bit version of the application.

Take a look at the file /android/app/build.gradle, we are interested in abi block:
```
android {
    ...
    splits {
        abi {
            reset()
            enable enableSeparateBuildPerCPUArchitecture
            universalApk false
            include "armeabi-v7a", "x86", "arm64-v8a", "x86_64"
        }
    }
    ...
}
```
IMPORTANT. Insure that in include you have "arm64-v8a" and "x86-64".

Reference: https://medium.com/@andriidrozdov/reactnative-and-android-64-bit-new-google-play-market-rules-what-to-do-584b067d6f1a
