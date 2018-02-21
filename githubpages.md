# GitHubPages

GitHubPages是GitHub提供的免费的静态资源服务器，搭建简单，不用自己购买云服务，可以绑定自己购买的域名，用来做个人博客再适合不过

步骤：

1、在github中创建一个项目，名称一定是 username.github.io这样的格式

![](/assets/屏幕快照 2018-02-19 下午12.04.32.png)

2、新建好项目后clone到本地，然后添加一个测试的html文件

```
<html>

    <body>

        test

    </body>

</html>
```

访问自己的域名 [https://qlql489.github.io/](https://qlql489.github.io/)

看到显示test

## Hexo

hexo是一款基于Node.js的静态博客框架，需要安装nodejs环境

详情可以参考[https://www.jianshu.com/p/35e197cb1273](https://www.jianshu.com/p/35e197cb1273) 写的很全

主要步骤

### 安装Hexo

```
npm install hexo-cli -g //安装
hexo init //初始化博库
hexo server // 本地加载 在浏览器中输入localhost:4000即可看到效果
```

### 添加 SSH Key 到 GitHub

hexo需要ssh的方式与github关联

```
$ ssh-keygen -t rsa -C "邮件地址@youremail.com"
```

打开本地 id\_rsa.pub 文件（ 参考地址 C:\Documents and Settings\Administrator.ssh\id\_rsa.pub）。此文件里面内容为刚才生成的密钥。如果看不到这个文件，你需要设置显示隐藏文件。准确的复制这个文件的内容，才能保证设置的成功。

登陆 GitHub 系统。点击右上角的 Account Settings---&gt;SSH and GPG keys--&gt;new SSH key

将id\_rsa.pub的内容复制到文本框内，保存

输入

```
ssh -T git@GitHub.com
```

提示

```
The authenticity of host 'github.com (192.30.255.113)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)? 
```

输入yes

在hexo的配置文件\_config.yml中配置你的git的ssh地址

```
deploy:
 type: git
 repo: git@github.com:qlql489/qlql489.github.io.git
 branch: master
```
### 部署
执行

```

hexo clean // 删除旧的 public 文件
hexo g //构建
部署到git需要安装node组件
npm install hexo-deployer-git --save
再执行
hexo d 
```
即可在你的GitHubPages中看到你的博客

![](/assets/屏幕快照 2018-02-19 下午3.24.40.png)

### 新建文章
```
hexo new "文章标题"
```
会在./source/_posts下生成一个markdown文件
文件头部有一些配置
```
---
title: 测试
date: 2018-02-19 12:56:54
categories: 随笔         #文章的分类，这个可以自己定义
tags: [Mac,效率,快捷方式]        #tag，为文章添加标签，方便搜索
---
```
下面就是markdown格式的文章了
### 更换主题
默认的主题还是比较丑的
在[官方主题](https://hexo.io/themes/)网页上可以选择其他的样式
必要的一些功能是需要集成在主题中的，比如：
- 评论
- 统计 
- 爬虫优化
- 打赏二维码

有编程基础的可以自己添加想要的功能

以我使用的主题为例：[snippet](https://github.com/shenliyang/hexo-theme-snippet)
下载下来后重命名文件夹，然后放在themes下![](/assets/1519186355824.jpg)
修改_config.yml文件中的
```
theme: snippet
```
 重新构建执行
```
 hexo clean && hexo g && hexo s
 ```
即可看到效果![](/assets/屏幕快照 2018-02-21 下午12.16.04.png)

如果你懂一些html、css和一些前端打包的知识，就可以动手自己改一下主题了。

修改后的效果 

![](/assets/屏幕快照 2018-02-21 下午8.27.11.png)


#### 参考：
[增加阅读统计](https://forum.leancloud.cn/t/yong-hu-fen-xiang-shi-yong-leancloud-wei-hexo-bo-ke-tian-jia-wen-zhang-liu-lan-liang-tong-ji-zu-jian/280)  
[hexo增加SEO](http://blog.csdn.net/qiuchengjia/article/details/52923170)
[Hexo安装和配置](https://www.jianshu.com/p/b7886271e21a)
[使用Hexo搭建博客（四），博客的部件和插件](https://www.jianshu.com/p/739bf1305e66)
[【干货】2个小时教你hexo博客添加评论、打赏、RSS等功能](https://www.jianshu.com/p/5973c05d7100)