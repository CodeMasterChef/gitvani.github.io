---
layout: post
title: Image on React Native
---

Case 1: Load image from local, we don't need to set width and height. The default is the image size:

```
<Image source={require('../../assets/images/demo.png')} />                 
```

Case 2: Load image from remote server, we need to set image size:

```
  <Image style={{width: 200, height: 100}} source={{uri: 'https://duhocvinahure.edu.vn/wp-content/uploads/2018/02/singapore-hong-kong.jpg'}} />
```

If we want to set full width image, we will set as bellow: 

```
  <Image   style={{flex: 1, height: 100}} source={{uri: 'https://duhocvinahure.edu.vn/wp-content/uploads/2018/02/singapore-hong-kong.jpg'}} />
```
