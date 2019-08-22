# 显示灯光

文档版本：1.0 

代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-22

## 需求

1. 方案里存在太多用户置入的灯光时，光照计算有较大开销，造成帧率过低，可以让用户勾选是否开启灯光

## 设计思路

1. 勾选/取消 时，获得当前World中所有VRDesign定义的灯光Actor，设置其灯光Component的HiddenInGame来实现灯光的显示/隐藏

## 相关代码

EditFunction\EditActor.h

```cpp
UFUNCTION(BlueprintCallable, Category = "EditFunc")
    void HideLight(bool bHideLight);
```

EditFunction\EditActor.cpp

