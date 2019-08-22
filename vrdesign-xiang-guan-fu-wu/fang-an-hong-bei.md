# 方案烘焙

文档版本：1.0 

最后更新日期：2019-8-21

## 需求

1. 用户对方案二次修改后，提交烘焙任务，后台根据用户的修改重置场景，重新构建光照
2. 用户可选光照构建等级
3. 构建光照之后的方案是新方案，需要修改文件夹GUID

## 设计思路

1. 根据方案的VR3D文件重置场景
2. 将光照等级放在[JobData](../shu-ju-zu-zhi/jobdata-zu-zhi.md#fang-an-hong-bei-jobdata)里，根据JobData调整
3. 通过MoveFolder实现修改文件夹GUID

## 运行流程

1. 下载方案的VR3D文件，根据VR3D下载所有需要资源
2. 通过VR3D文件信息重置场景（模型和灯光的增、删、改）
3. 根据JobData的信息选择光照等级，构建光照
4. 生成新的文件夹guid，MoveFolder实现当前文件夹重命名（自动修复redirector）
5. cook资源，打包上传

## 相关代码

Plugins\QuVRClick2VR\Source\AssetConvert\Public\Map\\*.h

Plugins\QuVRClick2VR\Source\AssetConvert\Private\Map\\*.cpp

