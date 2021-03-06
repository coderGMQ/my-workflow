# 我的workflow插件

这个目录下存放了我开发的 workflow 插件

### 纯自用，无意推广。由于各机型环境不同，你可能需要针对自己的环境去修改一些简单的 Python 代码。

## GoAgentX

![演示](http://images.bestswifter.com/alfred/GoAgentX-Alfred.gif)

### 使用：

开启连接:

```
gx c
```

关闭连接:

```
gx d
```

使用前先看一下脚本，修改其中的 `profileName`。

## 七牛

用于把剪贴板中的图片上传到七牛图床并且把 url 复制到剪贴板中。

### 流程

1. Command+Ctrl+A 截图(图片不要保存在本地，存在剪贴板中即可)
2. 在 Alfred 中输入 `gn` 
3. 图片会自动上传，并且把 Url 复制到剪贴板中，你只要按下 Command + V 即可

### 配置

1. 首先运行在 Alfred 中输入 `qnconf`，后面要加上 AK 和 SK，这是你的密钥，可以从官网获取，输入如下:
    
       ` qnconf xxx xxx`

2. 在 workflow 插件的文件夹中，有一个 `conf.txt` 文件，你需要打开它，设置上传到哪个 bucket，以及你的图床前缀，可以根据我现有的文件做修改。
3. 使用时，确保剪贴板中有图片，在 Alfred 中输入 `qn` 后面也可以指定一个参数名，表示上传图片的名称。如果不写则默认是当前时间戳。
4. 运行后，图片的 url 已经复制在你的剪贴板中了，尽情使用吧。

## Google 搜索

### 效果示意图

![](http://images.bestswifter.com/1469081792.png)

### 配置

1. 首先需要安装两个第三方的 Python 库：

    ```bash
    pip install pysocks
    pip install BeautifulSoup4
    ```

2. 另外，确保你的 `/usr/bin/python` 可执行且版本为 2.x，否则把当前 python2 的可执行文件做一个软连接：

    ```bash
    ln -s /path/to/python2 /usr/bin/pyhton
    ```

3. 最后。。。该脚本默认使用的是 shadowsocks 代理，如果使用 http 代理请自行参考注释修改源码。


