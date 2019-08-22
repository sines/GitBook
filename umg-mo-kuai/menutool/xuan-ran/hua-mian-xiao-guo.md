# 画面效果

文档版本：1.0 

代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-21

### 说明

画面PS效果通过设置后期处理的LUT纹理实现，LUT制作方法见[LUT制作流程](../../../vr-gong-neng-yu-mo-ban/hua-mian-xiao-guo-lut-su-cai-zhi-zuo-liu-cheng.md#lut-zhi-zuo-liu-cheng-can-kao)

### 需求

1. 给画面加PS效果，类似柔光、阿宝色等
2. 需要将PS效果应用到视频，全景图

### 设计思路

1. 通过设置后期LUT实现，用户选择不同效果，切换不同的LUT纹理

### 相关代码

LUTs\LutSwitchWidget.h

LUTs\LutSwitchWidget.cpp

