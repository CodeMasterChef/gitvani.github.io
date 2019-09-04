# iOS:

Khi build XCode, Gặp lỗi: Got 'React/RCTBridgeModule.h' file not found after ejected from Expo.

Sau khi reject Expo project, khi link thư viện có thể sẽ bị lỗi như trên. Chúng ta cần thêm Header Search Paths của thư viện cần link dòng như sau:

```
$(SRCROOT)/../../../ios/Pods/Headers/Public/**
```

![image](https://user-images.githubusercontent.com/10974517/64230296-a40c2400-cf16-11e9-8f2e-07cdc031c357.png)

# Android:

Khi link bị fail, khả năng cao thì trong project android cũng không thêm package trong MainApplication.java. Hãy chắc rằng:

```java
public class MainApplication extends Application implements ReactApplication {
    @Override
    protected List<ReactPackage> getPackages() {
      return Arrays.<ReactPackage>asList(
          new MainReactPackage(),
            new RNBluetoothEscposPrinterPackage()
      );
    }
}
```
