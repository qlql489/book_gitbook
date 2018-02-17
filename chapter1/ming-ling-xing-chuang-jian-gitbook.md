## 命令行创建GitBook

---

稍微懂一些编码就可以使用命令行创建GitBook了

有几个好处：

* 文档自己管理，可以选择是否发布到GitBook中，即免费有自己的私有图书
* 安装插件可以导出epub、pdf、mobi等格式的文件
* 安装插件添加评论，统计等功能，自定义css样式

步骤：确保电脑中已经安装nodejs、git，没有安装请自行百度

* 执行命令安装gitbook-cli

```
sudo npm install gitbook-cli
```

安装成功后输入gitbook -V可以看到版本信息

创建文件夹并新建文件README.md和SUMMARY.md

```
mkdir test1
cd test1  
touch README.md  
vim SUMMARY.md
```

SUMMARY中填写文章的结构

```
* [简介](README.md)
* [第一章](chap1/README.md)
 - [第一节](chap1/page1.md)
 - [第二节](chap1/page2.md)
* [第二章](chap2/README.md)
 - [第一节](chap2/page1.md)
 - [第二节](chap2/page2.md)
```

然后执行

```
gitbook init
```

会生成GitBook电子书的文件结构

```
├── README.md
├── SUMMARY.md
├── chap1
│   ├── README.md
│   ├── page1.md
│   └── page2.md
└── chap2
    ├── README.md
    ├── page1.md
    └── page2.md
```

这时已经能用GItBook客户端导入了，不过还打不开

![](/assets/image2.png)

需要提交到Git仓库后才能打开

在github中新建一个名字一样的仓库test1

然后在刚才的文件夹中执行

```
git init  //初试化本地仓库
git add -A //添加所有文件
git commit -m "gitbook" //保存一下
```

没有设置远程仓库的需要设置一下

```
git remote add origin https://github.com/{username}/test1
git push origin master
```

然后输入github的邮箱和密码推送成功

这时可以使用GitBook客户端来编辑了，当然可以用别的markdown编辑器编辑

