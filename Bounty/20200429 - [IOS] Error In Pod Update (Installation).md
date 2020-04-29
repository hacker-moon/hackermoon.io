### Brief

发起者：rpavlovs

赏金要求：[IOS] Error In Pod Update (Installation)

截止日期：5月29日

奖励金额：$5

申请链接：https://gitcoin.co/issue/prscX/react-native-app-tour/96/4265

---

### Actions to reproduce:

`yarn add react-native-app-tour`

Added the following pods into ios/Podfile as per ReadMe instructions

```
use_native_modules!

pod 'RNAppTour', :path => '../node_modules/react-native-app-tour/ios'

use_frameworks!

pod 'MaterialShowcase'
```

Then ran pod update

Error happened belowimage

![](https://imgkr.cn-bj.ufileos.com/c65b4696-db9e-4dfe-a11e-6d69bc9b6ff4.png)
