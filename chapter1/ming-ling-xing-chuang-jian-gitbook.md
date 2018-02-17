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





