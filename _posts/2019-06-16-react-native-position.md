---
title: Position on React native
layout: post
---

Component is set to `relative` to each other component by default.

The `absolute` make a component is relative to the **parent** instead of other component.


# Example 1: relative

![Snip20190616_6](https://user-images.githubusercontent.com/10974517/59560556-60ec9400-903e-11e9-8c95-7471ffc102a2.png)



```

 <ImageBackground style={styles.thumbnail} source={{ uri: 'https://duhocvinahure.edu.vn/wp-content/uploads/2018/02/singapore-hong-kong.jpg' }} >
              <View style={styles.panel}>
                <RkText rkType='white'>Hello </RkText>
              </View>
            </ImageBackground>

```

```
export const styles = StyleSheet.create({
  background:{
    flex: 1, 
    height: 200,
  
  },
  panel: {
    backgroundColor: 'rgba(0, 149, 136, 0.5)',
    position: 'relative',
    bottom: 0,
    width: '100%',
  }
});

```

# Example 2: Absolute

![image](https://user-images.githubusercontent.com/10974517/59560573-af9a2e00-903e-11e9-8713-7661467e0c41.png)

```
export const styles = StyleSheet.create({
  background:{
    flex: 1, 
    height: 200,
  
  },
  panel: {
    backgroundColor: 'rgba(0, 149, 136, 0.5)',
    position: 'absolute',
    bottom: 0,
    width: '100%',
  }
});
```
