# 增加光照情景

文档版本：1.0 

最后更新日期：2019-8-21

## 需求

1. 给当前Map增加一个LightingScenario

## 设计思路

1. 生成一个Map，使它成为主Map的sub-level，将sub-level类型改为LightingScenario
2. 用户选择增加的场景通过[JobData](../shu-ju-zu-zhi/jobdata-zu-zhi.md#zeng-jia-guang-zhao-chang-jing-jobdata)获得
3. LightingScenario只保存光照相关Actor（SkyLight、DirectionalLight、SpotLight、RectLight、PointLight、WindowLightActor（VRTemplate420自定义Actor））

## 运行流程

1. 下载方案的VR3D文件，根据VR3D下载所有需要资源
2. 通过VR3D文件信息重置场景（模型和灯光的增、删、改），保存当前Map
3. 删除当前方案所有非光照相关Actor（除了AWorldSetting）
4. 保存当前Level到新的Map，使新Map成为原Map的LightingScenario，调整灯光参数
5. 载入原Map，重复步骤3、4生成一个新的LightingScenario，保存
6. 构建光照（自动构建两个LightingScenario的光照，保存在各自的MapBuildData里）
7. 生成新的文件夹guid，MoveFolder实现当前文件夹重命名（自动修复redirector）
8. cook资源，打包上传

## 相关代码

Plugins\QuVRClick2VR\Source\AssetConvert\Public\Map\AddScenarioProcess.h

Plugins\QuVRClick2VR\Source\AssetConvert\Private\Map\AddScenarioProcess.cpp

Plugins\QuVRClick2VR\Source\AssetConvert\Public\Map\AddScenarioProcessHelper.h

Plugins\QuVRClick2VR\Source\AssetConvert\Private\Map\AddScenarioProcessHelper.cpp

