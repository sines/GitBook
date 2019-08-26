# 使用记录

## 一、**功能需求**

1. 在VRDesign中置入到场景中的素材都会被记录在使用记录中，按最近使用时间排序。

## 二、**设计思路**

1. 从任意库中使用模型，置入场景中后，软件会调用AddUserAsset\(\)向后台告知被使用的素材ID和Token信息，使用记录会根据最新使用时间进行排序**。**

## 三、**流程图**

显示流程参考素材库流程。

## 四、**相关代码**

../PersonalCaseWidget/ModelUsageCounterWidget.cpp

../PersonalCaseWidget/ModelUsageCounterWidget.h

