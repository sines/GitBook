---
description: DEPRECATED（已弃用）
---

# 模型转化

文档版本：1.0 

最后更新日期：2019-8-21

## 需求

1. 用户在3dsMax里上传模型导入UE4，UE4导入成uasset后Cook上传在VRDesign中使用

## 设计思路

1. 3dsMax导出对应的Datasmith文件，UE4 Editor载入Datasmith文件，cook资源，上传

## 相关代码

Plugins\QuVRClick2VR\Source\AssetConvert\Public\Model\\*.h

Plugins\QuVRClick2VR\Source\AssetConvert\Private\Model\\*.cpp

