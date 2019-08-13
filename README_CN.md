# Sis: Simple Image Search Engine   简单的一个图像检索引擎
#VGG16 全连接层特征进行检索

## [Demo](http://www.simple-image-search.xyz/)
![](http://yusukematsui.me/project/sis/img/screencapture2.jpg)

## Workflow
![](http://yusukematsui.me/project/sis/img/overview.jpg)

## 概述
-Sis是一个使用keras和flask实现的简单的图像检索系统，你只需要执行两个脚本后就可启动这个搜索引擎
-`offline.py`:  这个脚本提取图像的特征，给定一个数据集，使用在imageNet数据上预训练的VGG16网络提取全连接层6的4096维特征
- `server.py`:这个脚本启动一个web服务器，你可以通过flask web接口发送一个查询图像，使用近似近邻查询相关图像


## Links
- [Demo](http://www.simple-image-search.xyz/)
- [Project page](http://yusukematsui.me/project/sis/sis.html)

## 使用
```bash
# Clone the code and install libraries
$ git clone https://github.com/matsui528/sis.git
$ cd sis
$ pip install -r requirements.txt

# 将你的图像(*.jpg)放入static/img 目录下

$ python offline.py
# #fc6全连接层特征被提取并保存至static/feature目录
 #注意开始的时候会花费一些时间下载keras VGG权重文件

$ python server.py
# 现在你可以通过localhost:5000开始图像检索
```
