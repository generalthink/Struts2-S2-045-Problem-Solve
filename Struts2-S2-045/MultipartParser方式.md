1. 在struts.xml文件中添加如下配置
		<constant name="struts.multipart.parser" value="pell" />
		<constant name="struts.multipart.maxSize" value="20000000" />
2. 在项目的lib目录下引入对应版本的包
	struts2-pell-multipart-plugin-2.3.16.1.jar(换成自己对应的版本,该包下载struts之后会在lib目录下)
	pell-multipart-2.1.5.jar