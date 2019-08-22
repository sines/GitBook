# JobData组织

文档版本：1.0 

最后更新日期：2019-8-21

### 说明

JobData是在AddJob时自定义的JSON，用以传递不同数据

### 材质转化JobData

```java
{
    "Guid":"",
    "Type":"Material",
    "ProjectName":"",
    "UserName":""
}
```

| 字段 | 含义 |
| :--- | :--- |
| Guid | 材质的Guid（自动生成） |
| Type | Material（固定） |
| ProjectName | 材质名称 |
| UserName | 上传者名字（中文） |

### 模型转化JobData

```java
{
    "Guid":"",
    "AssetType":"Model",
    "IsAuto":,
    "DesignAssetGUID":"",
    "ShortDesignAssetGUID":"",
    "IsForceUpdate":,
    "dataSmithFile":""
}
```

| 字段 | 含义 |
| :--- | :--- |
| Guid | 模型的Guid（自动生成） |
| AssetType | Model（固定） |
| IsAuto | 是否自动上传 |
| DesignAssetGUID | 云设计素材ID |
| ShortDesignAssetGUID | 云设计短ID |
| IsForceUpdate | 是否强制更新 |
| dataSmithFile | DataSmith文件的URL |

### 方案烘焙JobData

```java
{
    "Guid":"",
    "Type":"Map",
    "BuildLevel":"",
    "UserId":"",
    "ProjectName":"",
    "UserName":""
}
```

| 字段 | 含义 |
| :--- | :--- |
| Guid | 方案的Guid（自动生成） |
| Type | Map（固定） |
| BuildLevel | 光照构建等级（用户选择） |
| UserId | 用户Guid |
| ProjectName | 方案名 |
| UserName | 用户名（中文） |

### 增加光照场景JobData

```java
{
    "Guid":"",
    "Type":"LightingScenario",
    "BuildLevel":"",
    "UserId":"",
    "ProjectName":"",
    "UserName":"",
    "LightingScenario":"",
    "CurrentScenario":""
}
```

| 字段 | 含义 |
| :--- | :--- |
| Guid | 方案的Guid（自动生成） |
| Type | LightingScenario（固定） |
| BuildLevel | 光照构建等级（用户选择） |
| UserId | 用户Guid |
| ProjectName | 方案名 |
| UserName | 用户名（中文） |
| LightingScenario | 要增加的LightingScenario类型（用户选择） |
| CurrentScenario | 当前的LightingScenario类型（根据方案自动生成） |

