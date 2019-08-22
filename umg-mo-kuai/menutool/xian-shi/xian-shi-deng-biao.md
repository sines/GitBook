# 显示灯标

文档版本：1.0 

代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-22

## 需求

1. 显示/隐藏 灯光的图标

## 设计思路

1. 勾选/取消 时，获得当前World中所有VRDesign定义的灯光Actor，设置其用来表示灯光图标的UWidgetComponent的HiddenInGame。
2. 为了防止隐藏灯光后还会被选中的问题，同时设置其碰撞属性
3. 当用户点击全景图截图时，如果灯标没有被隐藏，则自动隐藏

## 相关代码

Light\QuVRPointLightActor.h

```cpp
UFUNCTION(BlueprintCallable, Category = "PointLight")
    void SetShow(bool bShow);
```

Light\QuVRPointLightActor.cpp

Light\QuVRSpotLightActor.h 

```cpp
UFUNCTION(BlueprintCallable, Category = "SpotLight")
    void SetShow(bool bShow);
```

Light\QuVRSpotLightActor.cpp

