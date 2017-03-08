近日，安恒信息安全研究院WEBIN实验室高级安全研究员nike.zheng发现著名J2EE框架-Struts2存在远程代码执行的严重漏洞。

** 漏洞编号
S2-045，CVE-2017-5638

**漏洞名称
基于 Jakarta plugin插件的Struts远程代码执行漏洞

** 官方评级
高危

** 漏洞描述
Apache Struts 2被曝出存在远程命令执行漏洞，漏洞编号S2-045，CVE编号CVE-2017-5638，在使用基于Jakarta插件的文件上传功能时，有可能存在远程命令执行，导致系统被黑客入侵。恶意用户可在上传文件时通过修改HTTP请求头中的Content-Type值来触发该漏洞，进而执行系统命令。

** 漏洞利用条件和方式
黑客通过Jakarta 文件上传插件实现远程利用该漏洞执行代码。
1.基于Jakarta（Jakarta Multipart parser）插件的文件上传功能
2.恶意攻击者精心构造Content-Type的值

**漏洞影响范围
Struts 2.3.5 – Struts 2.3.31
Struts 2.5 – Struts 2.5.10

** 检测工具
使用lib目录下的Struts2 02-45 Poc.exe

** 加固方式如下:
	1. 通过判断Content-Type头是否为白名单类型，来限制非法Content-Type的攻击,查看content-type方式.md
	2. 采用其他的Multipart parser,查看MultipartParser方式.md

