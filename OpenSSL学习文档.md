# OpenSSL学习文档

@author：于洪伟



#### OpenSSL简介

OpenSSL是一个强大的安全套接字层密码库，囊括主要的密码算法、常用的密钥和证书封装管理功能及SSL协议，并提供丰富的应用程序供测试或其它目的使用。

OpenSSL的全称是：Open Secure Sockets Layer（开放的安全套接层协议）。Secure Sockets Layer简称为SSL，SSL能使用户/服务器应用之间的通信不被攻击者窃听，并且始终对服务器进行认证，还可选择对用户进行认证。SSL协议要求建立在可靠的传输层协议(TCP)之上。



#### OpenSSL的特点

##### 安全信道的特点

* 数据保密性

  信息加密就是把明码的输入文件用加密算法转换成加密的文件以实现数据的保密。加密的过程需要用到密钥来加密数据然后再解密。没有了密钥，就无法解开加密的数据。数据加密之后，只有密钥要用一个安全的方法传送。加密过的数据可以公开地传送。

* **数据完整性**

  加密能保证数据的一致性，能够校验用户提供的加密信息，接收者可以用MAC来校验加密数据，保证数据在传输过程中没有被篡改过。

* **安全验证**

  加密的另外一个用途是用来作为个人的标识，用户的密钥可以作为他的安全验证的标识。SSL是利用公开密钥的加密技术（RSA）来作为用户端与服务器端在传送机密资料时的加密通讯协定。

##### 开源

​	OpenSSL采用C语言作为开发语言，这使得OpenSSL具有优秀的跨平台性能，这对于广大技术人员来说是一件非常美妙的事情，可以在不同的平台使用同样熟悉的东西。OpenSSL支持Linux、Windows、BSD、Mac、VMS等平台，这使得OpenSSL具有广泛的适用性。

##### 案例

OpenSSL是一个强大的安全套接字层密码库，Apache使用它加密**HTTPS**，OpenSSH使用它加密**SSH**，但是，你不应该只将其作为一个库来使用，它还是一个多用途的、跨平台的密码工具。



#### 核心功能

OpenSSL软件包主要有三个核心功能组成：**SSL协议库**，**应用程序**以及**密码算法库**。



### 一、对称加密算法

#### 对称加密算法的种类

OpenSSL一共提供了8种对称加密算法，其中7种是**分组加密算法**，剩余一种**流加密计算法**RC4。

7组分组加密算法分别是：**AES、DES、Blowfish、CAST、IDEA、RC2、RC5**。

#### 加密模式

* 电子密码本模式：ECB
* 加密分组链接模式：CBC
* 加密反馈模式：CFB
* 输出反馈模式：OFB

以上四种模式为常用的分组密码加密模式。

###### AES算法：aes算法的分组长度是128位，其他算法的分组长度为64位。



### 二、非对称加密算法

#### 种类

OpenSSL实现了4中非对称加密算法，分别是：DH算法、RSA算法、DSA算法和椭圆曲线算法（ECC）。



### 三、信息摘要算法：哈希算法

OpenSSL实现了5种信息摘要算法，分别是：MD2、MD5、MDC2、SHA和RIPMED。SHA算法又包含了SHA和SHA1两种算法。



### 四、密钥和证书管理

#### 证书格式：DER、PEM、BASE64

OpenSSL实现了ASN.1的证书和密钥相关标准，提供了对证书、公钥、私钥、证书请求等数据对象的DER、PEM和BASE64的编解码功能。

#### PKCS规则

OpenSSL提供了各种公开密钥对的和对称密钥的方法、函数和程序，通过提供了对公钥和私钥的DER的编解码功能，同时实现了私钥的PKCS#12和PKCS#8的编解码功能。



### 五、OpenSSL学习参考资料

* OpenSSL中文网站：https://www.openssl.net.cn/
* OpenSSL的开源仓库地址：https://github.com/openssl/openssl

* OpenSSL命令使用：https://www.openssl.net.cn/column/32.html



### 六、OpenSSL的安装

* Linux下的安装：https://www.openssl.net.cn/docs/8.html
* Windows下的安装：https://www.openssl.net.cn/docs/9.html



### 七、重点

掌握命令的使用，如何生成私钥证书，公钥证书等。

genrsa： https://www.openssl.net.cn/docs/228.html

rsa：https://www.openssl.net.cn/docs/236.html

CA：https://www.openssl.net.cn/docs/242.html





















