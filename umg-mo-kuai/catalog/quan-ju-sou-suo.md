# 全局搜索

## **一、功能需求**

1. 用户可以查看模型数据库中所有数据（包括品牌库和素材库的所有材质和模型），方便用户使用搜索自己想要的素材。

## **二、设计思路**

1. 直接访问素材数据库主目录（RequestContent中MainCategoryID设为全部模型的CategoryID），返回所有素材信息，提前指定的12个数据。
2. 提供关键字搜索功能\(指定RequestContent中KeyWords的值\)，便于用户根据已知素材信息查找到素材。
3. 功能基于素材库功能实现，但没有子目录，只需修改请求中Content信息，将访问MainCategoryID设为主目录即可。

## **三、流程图**

整体参考素材库流程。

## 四、**相关代码**

GlobalSearchPanelWidget.cpp 

GlobalSearchPanelWidget.h。

