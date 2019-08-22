# 材质转化

文档版本：1.0 

最后更新日期：2019-8-21

## 需求

1. 根据用户上传的材质配置文件，生成对应的材质资源

## 设计思路

1. 从配置文件获得父材质模版，根据父材质创建材质实例（UMaterialInstanceConst），修改材质参数，cook之后打包上传，并更新数据库对应信息

## 相关代码

Plugins\QuVRClick2VR\Source\AssetConvert\Public\Material\\*.h

Plugins\QuVRClick2VR\Source\AssetConvert\Private\Material\\*.cpp

