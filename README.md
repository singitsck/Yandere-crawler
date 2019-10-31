## Yande.re图片爬虫

### 前言
两个月没刷[Y站](https://yande.re/post)积了2w个post，这时候当然应该找个机器替我刷啦

感谢[@mokeyjay](https://github.com/mokeyjay)的[爬虫项目](https://github.com/mokeyjay/Yandere-crawler)节省了很多时间。

(合并分支覆盖掉了原项目的Readme, 想办法补救中)

本项目基于`Win7, Python3.5.2`开发，在`Win10, Python3.6.7`与`Ubuntu16.04, Python3.5.2`运行成功，其他环境不作考虑。

### 功能
- 支持从指定的**开始页码**爬取到**结束页码**
- 也支持从**第一页**爬取到**上一次开始爬取的位置**
- 支持设置爬取的**图片类型**（全部、横图、竖图、正方形）
- 支持最大或最小**图片尺寸**、**宽高比**限制
- 支持限制爬取的**图片体积**
- 按照当天的日期创建目录并存放爬取的图片
- 爬取结束后会在图片目录下生成日志文件
- 支持tag搜索与排除
- (可选)GUI

### 如何使用
**可选** 

编辑`config.json`中`folder_path`参数，设为自己想要的目录，如文件夹不存在将会自动创建。路径必须以斜杠结尾。
剩下的参数可以运行后根据提示修改。

Windows下命令行执行`python index.py`即可，Linux下可直接执行。

### 注意事项

每次运行后`config.json`中`last_stop_id`参数会被自动修改为爬取到的第一张图片的ID，便于下一次爬取时只爬取新post，无论停止条件为ID或是页码。

### 更新日志
#### 1.0
终于完成了啦

### 未来计划
- ~~与[ExAPI](https://github.com/pavostudio/ExAPI)相容~~
- ~~基于机器学习的自动筛选(不识别图像了，识别标签吧)~~
