# 显示反射球

文档版本：1.0 

代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-22

## 需求

1. 显示/隐藏 反射球

## 设计思路

1. 勾选/取消 时，获得当前World中所有VRDesign定义的反射球Actor，设置其用来表示灯光图标的UWidgetComponent的HiddenInGame。
2. 为了防止隐藏后还会被选中的问题，同时设置反射球的碰撞属性
3. 当用户点击全景图截图时，如果反射球没有被隐藏，则自动隐藏

## 相关代码

QuVRFunctionLibrary\QuVRLibrary.h

```cpp
UFUNCTION(BlueprintCallable, Category = "GlobalSettings|EffectSetting")
	static void SetRelfectionsHidden(bool bIfShow);
```

QuVRFunctionLibrary\QuVRLibrary.cpp



