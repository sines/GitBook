# 显示吊顶

文档版本：1.0 

代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-22

## 需求

1. 显示/隐藏 吊顶（吊顶Tag为 EntityType:Ceiling）

## 设计思路

1. 勾选/取消 时，获得当前World所有带吊顶Tag的模型，设置其HiddenInGame

## 相关代码

EditFunction\EditActor.h

```cpp
UFUNCTION(BlueprintCallable, Category = "EditFunc")
	void HideStructure(bool bHideStructure);
```

EditFunction\EditActor.cpp

