# VR3D格式

文档版本：1.0

最后更新日期：2019-8-21

### 1.**根数据结构**

```java
{
    "version",
    "map_type",
    "guid",
    "HouseBrief",
    "start_position":
    "house",
    "actors",
    "RoomsSpaceDesc",
    "PanaData"
}
```

version: “1.0”, vr3d文件的版本号

map\_type: 可以选”design”, “scene” , 目前独立场景的都是”scene”\(”design”为画户型保留\).

guid: 场景文件的guid

HouseBrief：场景相关信息，包括风格，大小和项目名称

start\_position: player起始点

house: 保存场景的墙体，吊顶，定制品等产生的staticmesh信息，在下文展开说明。

actors：保存场景的软装模型信息，在下文说明。·

partitions：保存场景输出全屋全景图时需要的分区信息。

### **2.house数据信息**

```java
house:{
    "sky":,
    "wall":,
    "floor":,
    "ceiling":,
    "Molding":,
    "structure":
}
```

sky: 天空球的信息

```java
sky:{
    "name":,
    "guid":,
    "Components":
    [
        {
            "name":,
            "materials":[{}]
        }
    ]
}
```

wall: 墙体信息，数组 。

floor: 地面信息，数组

ceiling: 顶面信息，数组

```java
wall(floor/ceiling/structure/Molding) 
[
   {
     "name": ,
     "transform":,
     "Components":[],
     "roominfo":{
    		"size":{},
    		"roomtype":,
    		"typepath":,
    		"q3dtype":,
    		"attachwallflag":
      },
   }
]
```

Modling：踢脚线信息，数组

structure：硬装结构或定制品，数组

Components：目前存放actor的StaticMeshComponents信息，包含该Component的名字和材质数组，下同

roominfo：一键vr数据（待补充）

material: 材质的node，有材质的地方都采用统一格式，见下文详解。

```java
material:{
    "name":"",
    "guid":"",
    "assetpath":"",
    "config":{
    "scalar":[{
    }],
    "template":""
    }
}
```

### **3.actors 软装模型信息**

```java
actors:
{
    "modelactors":[],
    "dooractors":[
     	"name":,
     	"Components":[],
    ],
    "blueprintactors":[],
    "lightactors":[]
}
```

```java
modelactors:
[
    {
        "name",
        "guid",
        "assetpath",
        "type",
        "transform":
        {
            "location",
            "rotation",
            "scale",
        }
        "Components":[]
    }
]
```

name：actor在场景中的名字，例如"StaticMeshActor\_415"

guid: 模型pak包的guid

type：模型类型，普通的StaticMeshActor或者蓝图模型\(Blueprint\)

assetpath：模型的assetpath

transform：actor transformation

materials：此actor的StaticMeshComponent所用的material数组，material节点见下文

### **4.material材质节点的格式详解**

```java
material:{
    "name":"",
    "guid":"",
    "assetpath":"",
    "config":{
    "scalar":[{
    }],
    "template":""
    }
}
```

name:材质的名字，自动从assetpath中获取

guid:材质的guid，从assetpath中获取

assetpath:材质路径

静态材质只保存以上信息

动态材质额外保存config信息

```java
config:
{
    "scalar",
    "color",
    "template",
}
```

scalar：动态材质的信息

```java
[
    {
        "name":"",
        "value":""
    }
]
```

保存name-value，对应ScalarParameterValues 和 TextureParamterValues里信息

color:颜色信息

```java
{
    "name",
    "r",
    "g",
    "b",
    "a",
}
```

name：colorname 通常为SeamColor

```java
template:{
    "name":
}
```

template：动态材质所用的模版（父材质）名字

### **5.RoomSpaceDesc节点**

```text
RoomSpaceDesc:[

]
```

保存房间的空间划分相关信息（待补充）

### **6.PanoData**

```javascript
PanoData:{
    "RoomPoints":[],
    "SwitchPoints"[]:
}
```

保存房间的空间划分相关信息（待补充）

RoomPoints：房间的全景图相机点点位信息

SwitchPoints：全景图切换点点位信息

