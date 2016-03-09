
title: 第2次 这是关于怎么使用HEXO的初级教程
date: 2016-03-03 22:04:46
tags: HEXO

---

# 这是一个怎么使用HEXO创建博客的简单教程<br/>

#### 导语：

>这里是为了那些不想看官方文档的兄弟姐们准备的简单教程，有什么不妥的地方地方大家还是以官方文档为准! 最后还是建议阅读本篇文章之后一定要看官方文档，因为有的时候官方的会更新API，这才是重点。

- [官方文档连接](https://hexo.io/zh-cn/docs/)


## 1,首先你要去下载两个软件

在使用Hexo之前，有两样东西是必不可少的 ,别问为什么，先去下载，下载完了之后才能进行下面的操作。

- [GitBash](https://git-for-windows.github.io/)<br/>
- [Node.js](https://nodejs.org/en/)<br/>

这里建议大家番羽土啬来下，因为GTW真的很厉害，反正是很难下........<br/>
下载下来之后，就安装吧。

<!--more-->



## 2,安装完之后，在电脑随便什么地方创建一个文件夹【HEXO】，像下面一样

![](http://i.imgur.com/GTqKpMI.png) 
  
然后双击进去，鼠标点击右键，选中**Git Bash Here**，这个时候会出现一个命令框，此时需要你给电脑上安装HEXO，很简单，在下面输入如下命令：

    $ npm install -g hexo-cli    ：使用 npm 即可完成 Hexo 的安装
安装完成之后，继续依次输入如下命令，注意顺序

    $ hexo init    ：初始化 第一次使用的使用，以后除非新建否则不要使用
    $ npm install  ：安装

安装完成后，【HEXO】文件夹的目录如下：
	
	.
	├── _config.yml     ：网站的 配置 信息，您可以在此配置大部分的参数。
	├── package.json    ：应用程序的信息。EJS, Stylus 和 Markdown renderer 已默认安装，您可以自由移除。
	├── scaffolds		：模版 文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件。
	├── source   		：资源文件夹是存放用户资源的地方。除 _posts 文件夹之外，开头命名为 _ (下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到 public 文件夹，而其他文件会被拷贝过去。
	|   ├── _drafts		
	|   └── _posts
	└── themes			：主题 文件夹。Hexo 会根据主题来生成静态页面。

 		
**配置：** 

您可以在**_config.yml**文件中修改大部份的配置。双击进去查看以下配置信息：

### 网站：
	
	参数	描述
	title	    网站标题
	subtitle	网站副标题
	description	网站描述
	author		您的名字
	language	网站使用的语言
	timezone	网站时区。Hexo 默认使用您电脑的时区。时区列表。比如说：America/New_York, Japan, 和 UTC 。

	
其实这里有很多内容我就不一一列举了........我就截一张图，大家有空可以去官网查看详细内容，这里给出链接[官网](https://hexo.io/zh-cn/docs/configuration.html)


## 3，熟悉完目录结构后，接下来就开始写文章了

还是老样子，在【HEXO】内目录下右击，点击**GitBrashHere**，然后输入如下命令
	
	$ hexo new 第一次    ：这里会在HEXO\source\_posts目录下新建一个【第一次.md】文件

以后可以直接在这个文件类写文章了，需要**注意**的是文章的语法格式是***MarkDown***语法，写完后记得保存。

## 4，文章写完后，进行下一步操作

在命令行输入下面代码：

	$ hexo generate       也可以简写为  $ hexo g具体是指生成静态文件，这是发布网页的重要一步，必须操作

接下来开启服务

	$ hexo server        也可以简写 $ hexo s   

不出什么意外的话，在浏览器里输入http://localhost:4000/就能访问了。   
如果不行的话，解决方法如下，原因是4000端口被占用，更改端口就好了，代码如下：

	$ hexo server -p 4001     :更该端口为4001

如果能打开，那么恭喜你！你的博客搭建完成了！

## 5，你以为这样就结束了吗？错了！

是不是感觉不对劲，因为这里只能你自己电脑访问，是本地的，别人根本无法访问，接下来就教大家怎么把网页发布到GitHub上



- 首先要有一个github的账号，没有就去注册一个吧
- 然后新建一个仓库，在自己的GitHub账号下创建一个新的仓库，命名为**username**.github.io（**username**是你的账号名)。
- 我们继续使用上面的文件夹D:\Hexo，在文件夹下有一个文件名字是**_config.yml**，进入该文件找到如下部分：

		# Deployment
		## Docs: http://hexo.io/docs/deployment.html
		deploy:
 	 		type：

- 修改后的_config.yml：
		
  	 	 # Deployment 部署配置
  		 ## Docs: https://hexo.io/docs/deployment.html
 	   	 deploy:
 	     	type: git
	     	repo: https://github.com/YYwishp/YYwishp.github.io.git   （这个地址可以见下图）
	      	branch: master


![](http://i.imgur.com/kMI5yxS.png)


- 为了能够使Hexo部署到GitHub上，需要安装一个插件：

		$ npm install hexo-deployer-git --save
- 然后，执行下列指令即可完成部署：
	
		$ hexo generate
    	$ hexo deploy
- 之后，可以通过在浏览器键入：username.github.io进行浏览，开心吧~
- 关于绑定一名可以在我的第一篇文章尾部有教程。大家可以去找找。


  



		

	





	

	
















