# FastBuilder

一个为Minecraft Bedrock设计的快速建造程序

## 快速开始

```
$ git clone https://github.com/CAIMEOX/FastBuilder.git
$ cd FastBuilder
$ node FastBuilder.js
```

### 依赖项

```
$ npm install ws
$ npm install node-uuid
```

### 开始使用

基于MinecraftWS的特性，FastBuilder完全采用命令操作（以后可能有图形界面，如果你想帮忙，请私信我）

FastBuilder的使用并不复杂，请耐心看完操作流程（不然存档暴毙就怪不得我了）

在此之前，先完成‘快速开始’里面的内容.控制台出现一下字眼就代表启动成功了：

```
FastBuilder: v1.0.0
Copyright (C) CAIMEO
Server running at ws://127.0.0.1:8080
```

接下来，打开MinecraftPE,你几乎不必担心版本问题，FastBuilder支持0.16以上任意版本～

开启作弊，并打开聊天窗口，输入：

```
/connect 127.0.0.1:8080
```

连接成功就可以开始使用FastBuilder命令了（无需加/）

首先设置生成器坐标(即获取玩家当前位置)：

```
get pos
```

设置方块（默认为铁块）：

```
let block <tileName:String>
```

OK,设置基本完成了，接着就能使用建筑命令了：

```
//round 方向 半径 高度
round <direction:String> <radius:Int> <height:Int>
//sphere 状态 半径
sphere <method:hollow/solid> <radius:Int>
//circle 方向 半径 高度
circle <direction:String> <radius:Int> <height:Int>
//ligature 坐标1 坐标2
ligature <Position:x y z> <Position2:x y z>
//ellipsoid x宽度 y宽度 z宽度 精度
ellipsoid <width:x> <width:y> <width:z> <accuracy:Int>
//ellipse 方向 x长度 z宽度 高度 精度
ellipse <direction:String> <width:x> <width:z> <accuracy:Int>
```

## 为什么不使用ModPE,而是WebsocketServer

我来告诉你为什么
###ModPE
* 需要第三方启动器
* 通常免费但是有广告
* 不同版本需要不同的启动器 
* 受到设备限制
* 无法在服务器或领域使用
### WebsocketServer
* 支持任何设备
* 没有任何广告
* 算法在不断更新
* 可以在服务器或领域使用
* 支持 0.16 及以上的版本
## 运行测试模式

```
$ node FastBuilder.js -debug
```
用于查找bug.


## 开发笔记

作者很懒，不做笔记

## 开发相关

* [Nodejs](http://nodejs.org) - 程序语言
* [PEWS-API](https://github.com/jocopa3/PEWS-API.git) - API

## 贡献

任何人都可以加入FastBuilderProject,为FastBuilder贡献算法，具体流程请[点击这里](https://github.com/CAIMEOX/FastBuilder/blob/master/Algorithms.md)

## 作者

* **CAIMEO** - *MJTG* - [CAIMEO](https://github.com/CAIMEOX)

一位极不起眼的开发者

## 版权许可证

此项目使用  [GPL](LICENSE.md) LICENSE

## 鸣谢

* Nodejs
* LNSSPsd  -参考了LNSSPsd的[MyAgent](https://github.com/mcpews/MyAgent.git)项目
* Torrekie  -修复bug
* Jocopa3  -API 提供