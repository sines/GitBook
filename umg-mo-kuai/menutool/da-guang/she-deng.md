# 射灯

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 用户可以置入新的射灯
2. 置入的灯光可以调整部分属性

## 设计思路

1. 为了显示射灯的图标，VRDesign创建自己定义射灯Actor
2. 通过图标选中射灯时，显示参数面板，可在参数面板调整灯光部分参数

## 功能描述

1. 用户点击置入射灯时，在鼠标位置生成一个射灯
2. 在选中射灯之后，可以拖动射灯调整位置
3. 选中一个射灯时，显示射灯影响范围（射灯锥面）和参数页面

## 相关代码

射灯Actor：

Light\QuVRSpotLightActor.h

Light\QuVRSpotLightActor.cpp

射灯参数页：

UMGWidget\AssetDetailWidget\SpotLightDetailWidget.h

UMGWidget\AssetDetailWidget\SpotLightDetailWidget.cpp

