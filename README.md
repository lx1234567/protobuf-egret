# egret protobuf

## 特性

封装了 protobufjs 库及命令行。使用 protobufjs 6.8.4 的运行时库，并提供生成 .d.ts 文件的机制，以方便 TypeScript 项目使用

protobufjs 自身存在着 pbts 命令，虽然也可以生成 .d.ts 文件，但是在全局模式而非 ES6 module 的情况下存在一些错误，本项目致力于解决这个问题，使 protobufjs 可以在非 ES6 模块项目中（比如白鹭引擎）中也可以使用 protobufjs 

protobufjs 提供了多种使用方式，由于微信小游戏禁止 eval , new Function 等动态代码形式，所以本项目只提供了生成代码的形式，不支持通过 ```protobuf.load('awesome.proto')``` 的方式（因为这种方式也无法在微信小游戏中运行）。

本项目虽然名为 egret protobuf ，但是理论上支持所有 HTML5 游戏引擎。欢迎使用 PIXI.js , Cocos2d-js , LayaAir 等其他引擎的开发者使用本库。


## 如何安装

```
npm install protobuf@6.8.4 -g
npm install @egret/protobuf -g
```

## 如何使用

```
# 假设用户有个名为 egret-project 的白鹭项目
cd egret-project
# 将代码和项目结构拷贝至白鹭项目中
pb-egret add
# 将 protofile 文件放在 egret-project/protobuf/protofile 文件夹中
pb-egret generate
# 文件将会生成到 protobuf/bundles 文件夹中

```




## 如何运行 Demo

下载源代码，使用 ```egret run egret-project ```即可直接运行 demo 项目




## 路线图

* 集成 egret 构建管线




