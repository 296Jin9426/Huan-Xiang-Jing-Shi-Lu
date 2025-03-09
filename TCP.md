1#### Description

1. Create a comic strip to explain ho each of the internet protocols (TCP/IP, HTTPS, DNS) are used when transmitting data on the Internet.
2. Answer the following questions:

​	a)    Using your learning of Internet protocols, explain how the internet is interoperable

The devices can use a same protocol that different devices can explain once information to some result. As same as a translater that different operation system can sharing in internet.

​	b)   Protocols include HTTP and HTTPS – define each of these terms.

The HTTP is text file, it store computer language of web page that browser will understand it. So every one can read it and the hacker can read it easily.
And The HTTPS also is a HTTP protocol but it use SSL function encrypted text file so hacker cannot understand it.

​	c)    The IP Address is an important detail when communicating information.  Give an example of what an IP address may look like and explain when a business may use a static IP address and when it is appropriate to use a dynamic IP address.

IP address such as 127.0.0.1 is the coordinate of computer. It has static IP address and dynamic IP addres, for static IP address, it is always constant, it can use at server that they need working long times and the dynamic IP address is a temporary address that it back to ISP when you stop connection 

​	d)    The following web address (URL) https://themeisle.com/blog/ consists of 3 main parts.  Explain each – Protocol, Domain name, Path

protocol: https
domain name: themeisle.com
path: blog/what-is-a-website-url/

​	e)    Explain the role of the Internet Service Provider

The ISP can turn domain name into IP address and it will give each device dynamic IP address, it will back when device stop connection and ISP reuse this address to share another device.

#### 描述

1. 创建一个连环画来解释在互联网上传输数据时如何使用每种互联网协议（TCP/IP、HTTPS、DNS）。

2. 回答以下问题: 

 	a) 利用您对互联网协议的学习，解释互联网如何互操作
 	 
 	b) 协议包括 HTTP 和 HTTPS - 定义每个术语。
 	 
 	c) IP 地址是传递信息时的重要细节。举例说明 IP 地址可能是什么样子，并解释企业何时可以使用静态 IP 地址以及何时适合使用动态 IP 地址。
 	 
 	d) 以下网址 (URL) https://themeisle.com/blog/what-is-a-website-url/ 由 3 个主要部分组成。解释每个部分 - 协议、域名、路径
 	 
 	e) 解释互联网服务提供商的作用

---

# TCP

![img](https://img2020.cnblogs.com/blog/1614350/202012/1614350-20201209214135907-692951274.png)

> TCP协议:
>
> - 面向连接
> - 可靠
> - 基于字节流
>
> ****
>
> ## **TCP/IP分层模型**
>
> | 应用层         |                   |
> | -------------- | ----------------- |
> | **传输层**     | **TCP**(在这工作) |
> | **网络层**     | **IP层**          |
> | **网络接口层** |                   |
>
> ## 标志字段
>
> - URG **—** `紧急标志位，它使一端可以告诉另一端有些具有某种方式的“紧急数据”已经放置在普通的数据流中。另一端被通知这个紧急数据已被放置在普通数据流中，由接收方决定如何处理。`
>   - **紧急指针：** *占2个字节，紧急指针只有在URG=1时才有意义，紧急指针指出了紧急数据的末尾在数据报中的位置。*
> - ACK **—** `用以指示确认字段中的值是有效的，即该报文段包括一个对已被成功接收的报文段的确认；`
> - PSH **—** `推送标志位，当两个应用进程进行交互式的通信时，有时在一端的应用进程希望在键入一个命令时立即收到对方的响应。这时，发送方TCP将PSH标志位置为1时，立即创建一个报文段发送出去，接收方TCP收到PSH为1的报文，会尽快的交付给应用层，而不是等到缓存填满后交付。`
> - RST **—** `用以指示连接的强制拆除，当接收到错误连接时会发送RST位置为1的报文；`
> - SYN **—** `用以指示连接的建立，该位为1的报文表示希望建立连接；`
> - FIN **—** `用以指示连接的终止，该位为1的报文表示希望断开连接；`
>
> ## TCP 3次握手(TCP 3-way handshake)
>
> |        | 状态                          |
> | ------ | ----------------------------- |
> | 客户端 | closed                        |
> | 服务端 | closed $\rightarrow$ listened |
>
> 1. **SYN**报文(客户端$\rightarrow$服务端): 填充、发送**随机初始化序列号(序列号)**; 表示客户端向服务器发起连接; 无应用层数据. 
>
>    |        | 状态                          |
>    | ------ | ----------------------------- |
>    | 客户端 | closed $\rightarrow$ SYN-SENT |
>    | 服务端 | listened                      |
>
> 2. **SYN+ACK**报文(服务端$\rightarrow$客户端): 填充、发送**随机初始化序列号(确认应答号)**; **序列号**+1; 无应用层数据. 
>
>    |        | 状态                            |
>    | ------ | ------------------------------- |
>    | 客户端 | SYN-SENT                        |
>    | 服务端 | listened $\rightarrow$ SYN-RCVD |
>
> 3. **ACK**报文(客户端$\rightarrow$​服务端): 应答报文; 确认应答号+1; 可以携带应用层数据.
>
>    |        | 状态                               |
>    | ------ | ---------------------------------- |
>    | 客户端 | SYN-SENT $\rightarrow$ ESTABLISHED |
>    | 服务端 | SYN-RCVD $\rightarrow$ ESTABLISHED |
>
> ### advantage(**三次**握手)
>
> - 三次握手的主要原因是为了防止旧的重复连接初始化造成混乱, 避免历史连接。
>
> - 同步双方初始序列号
>
> -  避免资源浪费
>
> 

# HTTPS

## HTTP

> HyperText Transfer Protocol
>
> 目的: 提供一种发布和接收 HTML 页面的方法, 使浏览器更加高效。
>
> 明文

## SSL(TLS)

>  Secure Sockets Layer (1999年改为: TLS, Transport Layer Security)
>
> 目的: 构建一个HTTP的安全通道
>
> 加密方式

SSL



# DNS

> 将网址转换成ip地址
>
> 

## ISP

> 网络业务提供商，能提供[拨号上网](https://baike.baidu.com/item/拨号上网/7343999?fromModule=lemma_inlink)服务、网上浏览、下载文件、收发电子邮件等服务，是网络最终用户进入Internet的入口和桥梁。它包括Internet接入服务和Internet内容提供服务。这里主要是Internet接入服务，即通过电话线把你的计算机或其他[终端设备](https://baike.baidu.com/item/终端设备/643738?fromModule=lemma_inlink)连入Internet。



Who 

Gig worker 

What 

They have less rights, security & bargaining power 

 

Real Life Example 

 For drivers and couriers in the UK’s gig economy, employment status really matters. Most of them are classed as self-employed and do not receive statutory sick pay, for example.

Possible Causes 

 become very controversial, mainly due to how some of the major gig economy companies operate in the grey areas of employment law.

Negative Impacts 

 They have no protection against dismissa

 

Intervention Evaluation 

What is the Intervention 

 

Category of intervention 

Mitigate / Intercedes / Enhances / Resolves 

Description – who what, where, when 

 

How does it solve the challenge 

 

Limitations of the intervention 

 







