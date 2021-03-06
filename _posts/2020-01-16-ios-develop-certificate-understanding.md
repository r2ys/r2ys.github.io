---
layout: post
title:  "ios develop certificate understanding"
date:   2020-01-16 08:47:24 +0800
categories: iOS cer p12
---

## 理解iOS开发证书

#### 术语解释
##### cer
一种文件格式，存储的是公钥，学名证书

###### 如何生成cer
* der二进制编码（cer有别于ber、der）
* base64编码

##### der
二进制格式，不可读，Java和Windows服务器偏向使用这种格式
DER格式的证书基于X.509标准

##### PKCS#12
一个公钥加密的标准，总共有15个

##### p12
.p12是基于PKCS#12标准生成的一种文件格式，存储的是私钥
mac系统下在keychains钥匙串中找到证书->导出->p12就可以

##### 数字证书
无论是cer还是p12，广义上说都可以被称为数字证书。
| 什么是数字证书呢？数字证书就是互联网通讯中标志通讯各方身份信息的一串数字，提供了一种在Internet上验证通信实体身份的方式，数字证书不是数字身份证，而是身份认证机构盖在数字身份证上的一个章或印（或者说加在数字身份证上的一个签名）。它是由权威机构——CA机构，又称为证书授权（CertificateAuthority）中心发行的，人们可以在网上用它来识别对方的身份。在当今这个互联网时代，已经成为了必不可少，不可或缺的一个过程。

[](https://blog.csdn.net/huo065000/article/details/51002799)

##### PEM
pem文件是p12文件转换后的一种文件格式，存储的也是密码（私钥还是公钥？），内容是BASE64编码
以-----BEGIN开头，-----END结束
Apache和Linux、Unix服务器偏向使用这种编码格式
PEM格式的证书基于X.509标准

##### Https和Http关于s的区别以及SSL

##### OpenSSL
是SSL规范的一种实现。它还提供了一些工具软件，SSL证书需要符合的是一种标准X.509、RFC5280

##### 证书编码格式的问题
证书编码格式常见的有pem和der，但是文件扩展名并一定就是它俩，证书可以转换为其它编码格式，内容也有差别

###### 证书格式
* CRT
* CER
* KEY
* PFX/p12
* JKS

##### CSR
Certificate Signing Request, 证书签名请求，用户生成公私钥，私钥自己保存好，公钥作为申请内容，向证书颁发机构申请获得签名证书


#### iOS证书申请、到发布、再到用户安装过程中的流程
![]({{ site.baseurl }}/images/apple_auth_process.png)
