# Using gradle 4.9:


I decided to try out SDKMAN! out, which looked very promising. I wasn’t disappointed. SDKMAN! gave me access to even more Gradle versions than I needed.
```
$ sdk list gradle  
 ===========================================  
 Available Gradle Versions  
 ===========================================  
  3.4-rc-3     2.2.1      2.7  
 ...
 ```
Installation of all required package versions and switchover between them was even simpler.
```
$ sdk install gradle 4.9
$ sdk install gradle 3.3
$ sdk use gradle 4.9 
```
Please note that the use command does switch between candidates in the current shell. If you want to make the change permanent you must use default command instead.
```
$ sdk default gradle 4.9
```
