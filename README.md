# AuthCode_RC4
加解密算法，包括PHP、JAVA、Objective-C三种语言的算法实现以及Demo，可以用于APP与WEB后端加密通讯。
算法简介：
1.	加入了时间因子混淆，因此相同的明文，每次加密的结果都不一样，但是只要条件符合，均可以解密出正确的明文。
2.	加解密key均转换为数组，且做随机乱序（伪随机，根据密钥与报文长度做乱序），以增加破解难度（基于Ron Rivest提出的RC4算法做的改进），因此保证密钥不泄露是保密的关键工作。
3.	PHP端在加密时，可以指定超时时间（单位：秒），即超时后，密文无法被解密，以增强安全性。JAVA、Objective-C暂时不支持指定超时参数。
4.	三个版本的加解密的KEY需要统一，否则无法进行数据交换。这个问题只要智商正常，应该都能理解。
5.	三个版本的加解密算法，对于字符串处理，默认都使用UTF8编码…不解释。
6.	三个版本都包含了Demo。PHP的童鞋请关注PHP源码第55-63行所演示的使用方法；JAVA的童鞋请看源码文件最后的main入口；Objective-C的童鞋看main.m 源码。
