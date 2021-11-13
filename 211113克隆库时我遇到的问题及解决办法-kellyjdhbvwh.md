```
---
layout: post
title: 克隆库时我遇到的问题及解决办法
date: 2021-11-13
author: kellyjdhbvwh
categories:
    - 后端部
tags:
    - github
---
```

# 克隆库时我遇到的问题及解决办法

##  Connection was reset, errno 10054                          

报错原因：

 服务器的SSL证书灭有经过第三方机构的签署。

  网上信息也有的说可能是网络不稳定，连接超时导致。

解决 1、输入 

```
git config --global http.sslVerify "false"
```

我输入了这个代码，但是没解决

2、输入

```
git clone git://github.com/xxx/xxx.git --depth 1
```

原理：将深克隆改为浅克隆，只克隆最新记录而不可隆历史记录，从而减少克隆大小，大大提高克隆速度。同时更改了IP（这个我不知道为什么会有用）

我用了这个方法解决了