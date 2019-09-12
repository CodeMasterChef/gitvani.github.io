CocoaPods could not find compatible versions for pod "Folly".

Lỗi này xảy ra khi checkout các branch khi các thư viện của Cocoapods có thay đổi. Cách giải quyết là xóa file Podfile.lock và cài đặt lại thư viện:


```
cd ios
rm Podfile.lock
pod install
```
Sau đó, chúng ta có thể build app thành côn bằng xCode nhưng sẽ gặp lỗi:
![image](https://user-images.githubusercontent.com/5156120/48769488-124f6500-ecbc-11e8-9cb5-a6fc9caf6659.png)

Khi đó chúng ta cần clear server:
```
expo start --clear
```
