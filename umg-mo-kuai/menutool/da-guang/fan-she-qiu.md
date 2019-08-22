# 反射球

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-21

### 需求

1. 需要在VRDesign加入可以重新捕获的反射球
2. 用户可以调整反射球的半径，亮度，位置信息
3. 支持反射球修改的保存载入

### 一、设计思路

反射球在Editor模式下构建反射时，会将贴图存在MapBuildData里，若需要在Runtime里重新捕获，可通过修改引擎源码实现。在方案载入时，将原有的所有反射球替换成VRDesign定义的反射球Actor

### 二、功能描述

1. 用户点击置入反射球时，在鼠标位置生成一个反射球
2. 在选中反射球之后，可以拖动反射球调整位置
3. 选中一个反射球时，显示反射球影响范围（球面网格）和信息页（强度，半径和重新捕捉按钮）

### 三、相关代码

反射球Actor：

ModelAsset/ReflectionSphereActor.h

ModelAsset/ReflectionSphereActor.cpp

反射球信息页：

UMGWidget/AssetDetailWidget/ReflectionSphereDetailPanel.h

UMGWidget/AssetDetailWidget/ReflectionSphereDetailPanel.cpp

