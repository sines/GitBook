# 环境切换



文档版本：1.0

代码版本：git \[b60bd0e\]

最后更新时间：2019-08-21

### 一、功能需求

1. 可以手动切换当前环境是Dev还是Prod

### 二、设计思路

1. UE4的Actor可以读取配置文件，目前通过修改配置文件字段实现环境切换，程序启动时，在PlayerController的BeingPlay\(\)中Spawn该Actor来读取信息，在读取配置文件之后，修改URL的地址。
2. 将信息保存在DefaultGame.ini里，对应字段为bIfEnvDev，为true时表示是Dev环境，为false时是正式环境

### 三、流程图

![](../.gitbook/assets/0%20%281%29.png)

### 四、相关代码

QuVRDesign/EnvSwitch.h

QuVRDesign/EnvSwitch.cpp

QuVRDesign/QuVRDesign.h

QuVRDesign/QuVRDesign.cpp

