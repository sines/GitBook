# 增加光照场景

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 用户可以提交增加光照场景任务，给当前方案加一个不同的光照场景
2. 提交后可以看到转化进度

## 设计思路

{% hint style="warning" %}
1. 当前功能**仅支持**没有增加过光照场景的方案
2. 对于已增加过的方案再提交时，VRDesign会有相应提示
{% endhint %}

1. 方案修改通过[VR3D](../../../shu-ju-zu-zhi/vr3d-ge-shi-1.md)保存，提交时保存VR3D文件到oss
2. 增加的光照场景在[JobData](../../../shu-ju-zu-zhi/jobdata-zu-zhi.md#zeng-jia-guang-zhao-chang-jing-jobdata)中设置
3. 任务进度通过查询Job信息来获得
4. 当前的光照场景通过DirectionalLight的Tag获得，如果没有Tag，则默认为白天自然光

当前可增加光照场景：

```cpp
TArray<FString> CanAddableName = {
	TEXT("白天自然光"),
	TEXT("夜晚暖光"),
	TEXT("夜晚冷光") 
};
```

## 相关代码

UMGWidget\SceneToolWidget\SaveCaseWidget.h

UMGWidget\SceneToolWidget\SaveCaseWidget.cpp



