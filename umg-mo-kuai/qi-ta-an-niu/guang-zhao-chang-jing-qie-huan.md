# 光照场景切换

文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新日期：2019-08-22

## 需求

1. 有多个LightingScenario的方案可以切换

## 设计思路

1. 载入方案时如果当前方案LightingScenario个数超过一个，则载入第一个LightingScenario
2. 点击切换按钮时，循环切换LightingScenario

{% hint style="warning" %}
目前[增加光照场景](../menutool/hong-bei/zeng-jia-guang-zhao-chang-jing.md)之后的方案的LighintgScenario个数为2，按钮仅支持两个LightingScenario来回切换
{% endhint %}

## 相关代码

Light\LightingScenarioSwitch.h

Light\LightingScenarioSwitch.cpp

蓝图：

/Game/3DScene/BP\_LightingSwitch

/Game/UMG/LightingSwitch/LightSwitchPanel

