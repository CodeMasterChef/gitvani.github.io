**Important:** We have to use exactly version.

# React Native: 0.59.8:

Don't believe the Readme on [the reposioty home page](https://github.com/react-native-community/lottie-react-native#installing-react-native--059x).
We have to use the bellow version:

* lottie-ios: 2.5.0
* lottie-react-native: 2.5.11


Install lottie-react-native (2.5.11) and lottie-ios (2.5.0):


```
npm i --save lottie-react-native@2.5.11
npm i --save lottie-ios@2.5.0
```
Use react-native link to add the library to your project:

react-native link lottie-ios
react-native link lottie-react-native



In the Embedded Binaries section above click the + icon and add the Lottie.framework.iOS from Lottie.xcodeproj:

![](https://miro.medium.com/max/1234/1*9xdWL-x1dgXdD54DppamIw.png)

Read more: https://medium.com/react-native-training/lottie-react-native-tutorial-162d91840720

# With Expokit:

Expokit (ejected from Expo) using Pods to install library.

We using bellow command to install a suitable version: 

```
expo install lottie-react-native
```

We can get an [error](https://github.com/react-native-community/lottie-react-native/issues/409): "LottieAnimationView but name was already registered by class ExAnimationViewManager"

The way to fix: If you're using expo, expo itself has lottie-react-native. You should remove any lottie packages that have been added by react-native link, e.g. lottie-ios. This solved the issue for me. There's no need to link those packages if i'm not mistaken.

I mean remove we need to remove below line on Podfile: 
```
pod 'lottie-react-native', :path => '../node_modules/lottie-react-native'
```
