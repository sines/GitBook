# 素材库

## 一、 **功能需求**

1. 用户可以查看除套餐包中包含的所有模型，提供搜索功能及条件筛选。

## 二、 **设计思路**

1. 第一次打开素材库，向服务器请求素材库目录之下的所有素材信息\(CategoryID与全局搜索的CategoryID相同），并返回12个数据结果。
2. 点击素材库下一、二、三级目录\(修改RequestContent中的MainCategoryID为对应的目录ID\)，向服务器发请求，查询对应目录下所有的素材信息，并返回指定的12个数据。
3. 关键字查找会根据用户所在的目录下查找\(指定RequestContent中KeyWords的值\)。
4.  筛选框会根据用户当前所在目录进行对应筛选。

## 三、 **流程图**

![](../../.gitbook/assets/image%20%289%29.png)

![](file:///C:\Users\USER\AppData\Local\Temp\ksohtml33760\wps1.jpg)

## 四、 **相关代码**

PublicAssetLibraryPanelWidget.cpp

PublicAssetLibraryPanelWidget.h。

