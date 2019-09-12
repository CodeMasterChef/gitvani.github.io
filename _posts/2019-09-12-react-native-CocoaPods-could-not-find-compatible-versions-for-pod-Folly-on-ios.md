CocoaPods could not find compatible versions for pod "Folly".

Lỗi này xảy ra khi checkout các branch khi các thư viện của Cocoapods có thay đổi. Cách giải quyết là xóa file Podfile.lock và cài đặt lại thư viện:


```
cd ios
rm Podfile.lock
pod install
```
