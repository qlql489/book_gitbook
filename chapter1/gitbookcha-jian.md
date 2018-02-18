## GItBook插件

---

GitBook有很多开源的插件可以用，插件的安装需要在书籍的文件夹下简历book.json文件，然后添加在plugins字段和pluginsConfig，然后执行gitbook install，安装好插件后执行gitbook serve就可以看到效果

介绍几个插件

* atoc目录

```
{
    "plugins": ["atoc"],
    "pluginsConfig": {
        "atoc": {
            "addClass": true,
            "className": "atoc"
        }
    }
}
```

* 打赏插件





