# License_Plate_Recognition_pytorch
该工作由电子科技大学陈昂、刘俊凯、夏子寒同学完成。

我们提出可以使用深度学习的方案对中国车牌进行检测和识别。使用YOLOv3网络进行车牌检测，然后创新性地对检测后的车牌使用空间变换网络STN加以校正，最后使用LPRNet网络进行车牌的字符与数字识别。

目前实测结果，在老师提供的45张数据集上，我们的YOLOv3网络检测准确率（IOU）达到98.2%，深度学习级联网络识别准确率为95.6%。

我们采用大量测试集，最终我们的YOLOv3_STN_LPRNet级联网络识别准确率稳定在93.3%，不加空间变换网络STN的话，识别准确率在66%左右。

总体来说，使用深度学习的方案比传统方案效果提升的非常好，而且我们加入空间变换网络STN的做法对于提升识别准确率很有效。


YOLOv3运行的时候需要输入命令语句python object_detection_yolo.py --image=图片名.jpg

YOLOv3的权重模型，可以从链接：https://pan.baidu.com/s/1I2Hv__uiN7ql7RLe99nWsw 提取码：rsue得到

LPRNet需要测试的车牌可以放进test文件夹内，size为94×24

LPRNet只需要运行LPRNet test函数即可得到结果

其中我们已经添加了STN网络，如果您想去掉STN，只需要对images = STN（images）进行注释即可

如果您认可我们的工作，麻烦给我们一个星星，谢谢您
