# 材质提取

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-8-21

### 一、功能需求

1. 用户可以提取场景中的所有材质
2. 可以将提取到的材质赋给任意模型
3. 修改之后可以保存载入
4. 提取材质要有图标显示

### 二、设计思路

鼠标左键点击时，根据状态决定是该点击操作是赋材质还是提取材质，用EMaterialBurshState来决定状态。每次鼠标左键点击时，做一次射线检测，获得检测到StaticMeshComponent的SectionIndex，如果当前状态是GET\_MATERIAL，则获得当前Section的材质给\*CurrentMaterial，根据当前材质的信息设置材质图标，如果当状态是SET\_MATERIAL，将\*CurrentMaterial的材质赋给当前Section。

### 三、流程图

![](../../.gitbook/assets/0%20%282%29.png)

### 四、相关代码

ModelAsset/QuVRMaterialBrushActor.cpp

ModelAsset/QuVRMaterialBrushActor.h

