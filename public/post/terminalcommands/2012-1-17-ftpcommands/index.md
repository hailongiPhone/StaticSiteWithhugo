

# [命令行工具]Ftp

	本文用来记录使用到的Ftp基本命令。

# 本文涉及命令：

+ 登陆远程服务器
+ 上传文件
+ 下载文件

## 登陆远程服务器

### 登陆方式一：

1 发送连接请求

		ftp> open 远程服务器地址

2 输入用户命

		Name （远程服务器：用户）：

3 输入密码

		331 Please specify the password.
		Password:


### 登陆方式二：

	ftp 登陆用户名@远程服务器地址

## 上传文件：

		ftp> put 要上传的文件路径 [在服务器上保存路径]


## 下载文件：

		ftp> get 服务器上要下载的文件路径 [本地保存路径]

# 与路径相关的命令

		ftp> pwd 				//显示服务器上的当前路径
		ftp> ls  				//列表显示服务器上的当前路径目录文件
		ftp> dir  				//同上
		ftp> mkdir 目录  		//新建目录
		ftp> rmdir 目录  		//删除目录
		ftp> cd 目录
		ftp> delete 文件名  				//删除文件
		ftp> rename [文件名] [新文件名]  	//修改文件名

# 与服务器断开连接

		ftp> close 				//断开连接，但保留"ftp>"会话
		ftp> disconnect  		//同上
		ftp> bye  				//结束连接会话
		ftp> quit		  		//结束连接会话



# ftp环境与本地shell之间的切换

		ftp> ！			  		//进入本地shell
		XXX > exit				//从本地shell环境回到ftp远程服务器环境
