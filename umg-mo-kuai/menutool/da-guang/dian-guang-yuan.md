# 点光源

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 用户可以置入点光源
2. 可以选中点光源，调整位置和参数

## 设计思路

1. 置入的点光源为自定义的点光源Actor
2. 每个Actor都带有一个UWidgetComponent，可以实现选中，显示图标

## 功能描述

1. 用户点击置入点光源后时，在鼠标位置生成一个点光源Actor
2. 在选中点光源之后，可以拖动点光源调整位置
3. 选中一个点光源时，显示点光源影响范围（球面网格）和参数页（PointLightComponent部分参数）

## 相关代码

点光源Actor：

Light\QuVRPointLightActor.h

Light\QuVRPointLightActor.cpp

点光源信息页：

UMGWidget\AssetDetailWidget\PointLightDetailWidget.h

UMGWidget\AssetDetailWidget\PointLightDetailWidget.cpp

