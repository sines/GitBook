# 显示软装

文档版本：1.0 

代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-22

## 需求

1. 显示/隐藏 所有软装模型

## 设计思路

1. 勾选/取消 时，获得当前World所有带[软装Tag](../../../shu-ju-zu-zhi/vr3d-ge-shi.md#ruan-zhuang-mo-xing)（DecoType:Soft）的模型，设置其HiddenInGame
2. VRDesign的组合模型理论上也属于软装模型，勾选/取消 时同时设置组合模型的HiddenInGame

## 相关代码

EditFunction\EditActor.h

```cpp
UFUNCTION(BlueprintCallable, Category = "EditFunc")
	void HideSoftAdornment(bool bHideModel);
```

EditFunction\EditActor.cpp

