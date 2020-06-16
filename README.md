# aliPlayerDemo
A demo of aliPlayer, some Q&amp;A of useing SKD.

**在使用阿里云的视频点播及阿里播放器的过程中,遇到的问题与解决方案**

Q1.使用aliPlayer播放视频失败,返回code:4400

A1.OSS回源记录地址路径为http://abc.123,网站为https://edf.456

官方给出的解答:

>  由于网站后台配置了https，而通用代码中的视频链接为http，导致视频无法播放。解决方案：直接在视频通用代码中，将src单引号中间的网址由http更改为https，保存并发布网站即可。 

实际使用中,网站地址既可以用https访问,也可以用http访问.那么储存的回源地址更改为https就不太灵活了.

解决方案:

为回源地址配置https证书.