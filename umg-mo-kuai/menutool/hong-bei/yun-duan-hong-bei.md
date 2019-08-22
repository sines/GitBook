# 云端烘焙

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 用户对方案二次调整之后，可以提交重新构建光照，由后台进行[光照构建](../../../vrdesign-xiang-guan-fu-wu/fang-an-hong-bei.md)
2. 提交时可选光照等级
3. 提交之后能看到任务进度

## 设计思路

1. 方案修改通过[VR3D](../../../shu-ju-zu-zhi/vr3d-ge-shi-1.md)保存，提交时保存VR3D文件到oss
2. 光照等级在[JobData](../../../shu-ju-zu-zhi/jobdata-zu-zhi.md#fang-an-hong-bei-jobdata)中设置
3. 任务进度通过查询Job信息来获得

## 相关代码

UMGWidget\SceneToolWidget\SaveCaseWidget.h

UMGWidget\SceneToolWidget\SaveCaseWidget.cpp



