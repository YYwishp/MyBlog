

title: 第2次 HEXO--换电脑编辑，指南
date: 2016-03-06 10:29:56
tags: HEXO
categories: HEXO

---
# 首先在A电脑上把【HEXO】文件整个上传到Github上，具体操作如下

1. 鼠标右击【HEXO】文件夹，选中Git在这里创建版本库

	![](http://i.imgur.com/QIX3nDR.jpg)
<!--more-->
2. 点击确定

    ![](http://i.imgur.com/OITj2Rc.png)
3. 点击确定

	![](http://i.imgur.com/RDj1eBR.png)
4. 右击选中TortoiseGit（T），然后选中（添加）
  
	![](http://i.imgur.com/eQ1HbPj.jpg)
5. 全选，确定

	![](http://i.imgur.com/u4v63wD.png)
6. 提交 

	![](http://i.imgur.com/hCuP5MV.png)
7. 写描述，提交

	![](http://i.imgur.com/FnxFZPr.png)
8. 已经提交到本地了，接下来push到Github

	![](http://i.imgur.com/CKI376T.png)
9. push到github

	![](http://i.imgur.com/qmQ3WaK.jpg)
10. 输入github地址

	![](http://i.imgur.com/KdzEzpj.png)
	![](http://i.imgur.com/k6K8RHG.png)
11. 输入Github用户名字，不是邮箱

    ![](http://i.imgur.com/87ogxdY.png)

12. 输入Github密码

	![](http://i.imgur.com/CSFE6ue.png)
13. 确定，有的时候会有问题：git 未能顺利结束 (退出码 1)
问题出现的原因很简单：就是在github创建仓库的时候，已经有文件了比如说有Readme文件，这个时候就要先在本地更新仓库，然后在push仓库就没有问题啦。还有一种解决方法：就是在github上创建仓库的时候，什么文件都不添加，就是纯空的仓库，接下来在本地第一次提交的时候就不会有问题了。
	![](http://i.imgur.com/C6aB81B.png)
14. ------------------------这个时候我们的【HEXO】整个文件就已经同步到github上了，----------------------------------



#接下来是B电脑从github上pull拉的过程
1. 在B电脑上新建一个文件夹。然后右击选中Git在这里创建版本库

	![](http://i.imgur.com/QIX3nDR.jpg)
2. 点击确定
    
	![](http://i.imgur.com/OITj2Rc.png)
3. 点击确定

	![](http://i.imgur.com/RDj1eBR.png)
4. 右击选中TortoiseGit（T），然后选中拉取（pull）
	
	![](http://i.imgur.com/1MCoQ8c.jpg)
5. 然后去github上把仓库的地址复制下来

	![](http://i.imgur.com/YwpEsfH.png)
6. 把复制的地址粘贴到

	![](http://i.imgur.com/TyHKV9s.png)
7. 或者点击管理远端

	![](http://i.imgur.com/nzzwT90.png)
8. 在URL处粘贴地址

	![](http://i.imgur.com/wxjCcD4.png)
9. origin就是刚才保存的URL命名

	![](http://i.imgur.com/o0DSmal.png)
10. 点击确定之后，成功。

	![](http://i.imgur.com/JbfMiql.png)
11. pull拉下来的文件夹是这样的：

	![](http://i.imgur.com/CIihTF4.png)
12. 但是大家先别高兴太早，这个时候还不能直接写博客，不幸可以试试看
在【HEXO】中右击选中Git Bash Here

	![](http://i.imgur.com/1M5OHSJ.png)
13. 在命令行中输入hexo，如果跳出下面的就代表不能直接使用，

	![](http://i.imgur.com/dCQhOGc.png)
14. 说明我们要先敲这行代码：npm install hexo --save
 敲完后要等一会，他会自己进行处理，处理完后是这样的，
上面省略一部分，太长了.......就截一部分。

	![](http://i.imgur.com/bYZnAlw.png)
15. 接下来安装依赖包，
输入命令 ：npm install
注意：有些同学忘了，敲上面这段代码，直接hexo g，然后再hexo s，会发现开不了服务，本地也不能访问。

	![](http://i.imgur.com/WCryyXz.png)
16. 安装依赖包之后是这样的
下面一大段安装的东西，看不懂，反正就是安装了，不相信可以输入
hexo g，然后hexo s试试能不能访问本地的localhost：4000

	![](http://i.imgur.com/99HbjpH.png)

17. 输入hexo g，然后再输入hexo s之后是这样的，
说明本地可以访问了。接下来就是部署到github上
	
	![](http://i.imgur.com/eakfl3a.png)
18. 我们先把服务停了，Ctrl c就可以了
创建新的文章，开始写文章
然后输入hexo new 第4次
在E:\HEXO\source\_posts路径下创建第4次.md

	![](http://i.imgur.com/t9FVYi4.png)

19. 进入第4次，就可以写文章了......

	![](http://i.imgur.com/tRYSs08.png)

20. 写完之后先在本地看看怎么样   
在命令行    
输入hexo g        ---生成静态文件   
输入hexo s        ---开启服务   
开启浏览器访问localhost：4000   
有的时候可能4000的端口被占用了，打不开
解决办法更换服务端口：输入：hexo server -p 4001

	![](http://i.imgur.com/cWvLYOD.jpg)
21. 这就代表服务搭建好了，可以写文章了，最后一步就是部署到github上。
为了确保能连上github，首先进入【HEXO】文件夹中找到_config.yml文件
打开看看，是不是如下：

	![](http://i.imgur.com/LE0FuQu.png)

22. 跟上面一样就ok；接下来就是输入以下命令：     
hexo g   ---生成静态文件   
hexo d   ---部署   
部署的时候会提示输入github的用户名，这里不是邮箱地址。   
还有输入密码。

	![](http://i.imgur.com/yTwtyKm.png)

23.  注意：如果不行，解决方法如下：   
输入下面代码：    
    npm install hexo-deployer-git  - -save  
	--------为了能够使Hexo部署到GitHub上，需要安装一个插件   
然后：执行    
hexo g   
hexo d    
这下就可以去浏览器输入:用户名.github.io进行访问啦！！    
有人会说域名太长记不住，这里可以自己绑定域名    
方法如下：    
接下来就是绑定域名    
在【HEXO】文件夹中的【public】文件夹内新建一个CNAME文件（文件名叫CNAME，没有文件后缀）    

	 ![](http://i.imgur.com/Yr4YOIW.png)

    【public】文件夹内部如下

	![](http://i.imgur.com/erqbNqK.png)

	CNAME文件中是域名，***yywishp.com***
	
	![](http://i.imgur.com/F2wCvRi.jpg)

      等待更改生效，一般几分钟就可以使用你自定义的域名进行访问了。


---------------------------------尼玛终于写完了教程我靠( ‵o′)凸--------------------------


	




































   


