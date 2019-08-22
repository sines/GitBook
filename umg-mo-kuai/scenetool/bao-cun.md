# 保存

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 用户修改方案之后可以保存，下次载入时载入的是保存后的方案
2. 保存方案可选覆盖或新建方案

## 设计思路

1. 点击保存时根据当前World信息生成VR3D文件
2. 勾选覆盖时，上传VR3D到原方案的VR3D地址，不覆盖时新建方案，然后上传对应信息
3. 保存时截取当前画面作为方案缩略图

## 相关代码

UMGWidget\SceneToolWidget\SaveCaseWidget.h

UMGWidget\SceneToolWidget\SaveCaseWidget.cpp



