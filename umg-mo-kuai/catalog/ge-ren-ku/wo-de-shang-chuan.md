# 我的上传

文档版本：1.0

 代码版本：git \[b60bd0e\] 

最后更新日期：2019-8-21

### 需求

1. 显示用户通过模型工具上传的模型
2. 显示用户在VRDesign里上传的材质
3. 点击上传贴图可以上传材质
4. 上传后显示转化进度

### 设计思路

1. 通过AccessType查询个人上传的资源，返回的数据解析后生成对应的Item
2. 上传材质时从固定的材质模版（UMaterial）中选择，通过调整材质参数来实现，点击上传时，获取用户自定义的材质参数，保存为JSON格式的配置文件，如果用户替换了纹理贴图，将纹理贴图上传到oss，oss返回的链接保存到配置文件（配置文件格式见[VR3D material字段](../../../shu-ju-zu-zhi/vr3d-ge-shi-1.md#4material-cai-zhi-jie-dian-de-ge-shi-xiang-jie)）里，然后上传配置文件，更新数据库，增加任务，由后台处理[材质转化](../../../vrdesign-xiang-guan-fu-wu/cai-zhi-zhuan-hua.md)
3. 转化进度通过查询Job进度实现

### 相关代码

UMGWidget/MaterialUpload/\*.h

UMGWidget/MaterialUpload/\*.cpp

