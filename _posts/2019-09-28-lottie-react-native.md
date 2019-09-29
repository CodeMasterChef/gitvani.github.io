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
