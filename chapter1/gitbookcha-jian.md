## GItBook插件

---

GitBook有很多开源的插件可以用，插件的安装需要在书籍的文件夹下简历book.json文件，然后添加在plugins字段和pluginsConfig，然后执行gitbook install，安装好插件后执行gitbook serve就可以看到效果

介绍几个插件

* 浮动目录导航

```
{
    "plugins": ["anchor-navigation-ex"],
    "pluginsConfig": {
        "anchor-navigation-ex": {
           "showLevel": false,
        "associatedWithSummary": true,
        "printLog": true,
        "multipleH1": true,
        "mode": "float",
        "float": {
                    "showLevelIcon": false,
                    "level1Icon": "fa fa-hand-o-right",
                    "level2Icon": "fa fa-hand-o-right",
                    "level3Icon": "fa fa-hand-o-right"
        }
    }
    }
}
```

点击目录能能够直接跳转

![](/assets/屏幕快照 2018-02-18 下午6.52.31.png)

详细的配置参考[https://github.com/zq99299/gitbook-plugin-anchor-navigation-ex/blob/master/doc/config.md](https://github.com/zq99299/gitbook-plugin-anchor-navigation-ex/blob/master/doc/config.md)

* 打赏插件

```
{
    "plugins": [
        "donate"
    ],
    "pluginsConfig": {
        "donate": {
            "wechat": "微信二维码图片地址",
            "alipay": "支付宝二维码图片地址",
            "title": "打赏吧",
            "button": "您的打赏是我的动力",
            "alipayText": "支付宝打赏",
            "wechatText": "微信打赏"
        }
}
```

* 评论插件

* 代码复制插件

```
{
    "plugins":["copy-code-button"]
}
```

效果![](/assets/屏幕快照 2018-02-18 下午7.14.28.png)



