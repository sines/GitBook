# 测距

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 用户在VRDesign里可以点击两个地方来测量两点之间距离
2. 测距要有吸附功能（x，y，z轴吸附）

## 设计思路

1. 通过射线检测来获得鼠标点击的位置
2. 通过状态（EMeasureMode）来判断当前点击时第一个位置还是第二个位置
3. 右键点击时回退到上一步的状态
4. 在界面固定位置显示计算得到的距离
5. 在第二个点未确定时，计算向量方向与三轴夹角完成吸附

```cpp
UENUM(BlueprintType)
enum class EMeasureMode :uint8
{
	NONE,
	IN_MEASURE,
	IN_MEASURE_POINT2,
};
```

## 相关代码

3DScene\MeasureDistanceActor.h

3DScene\MeasureDistanceActor.cpp



