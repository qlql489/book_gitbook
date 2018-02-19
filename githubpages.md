## GitHubPages

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

访问自己的域名 https://qlql489.github.io/

看到显示test

## Hexo

hexo是一款基于Node.js的静态博客框架，需要安装nodejs环境

详情可以参考https://www.jianshu.com/p/35e197cb1273 写的很全

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







