&emsp;&emsp;目前React Native(以下简称RN)在我们公司的线上产品中已经大规模使用了，在这个过程中我们踩了不少的坑，也解决了许多棘手的问题。RN项目实战是一个系列文章，主要分享我们是如何把RN框架一步一步落地应用到我们的实际业务场景，本文是系列文章的第一篇，主要介绍如何把RN框架集成到现有项目中。

## iOS篇

### 开发环境准备

&emsp;&emsp;使用RN之前，需要安装搭建必要的开发工具和环境，主要包括 Node, Watchman, React Native命令行工具，CocoaPods等，安装方法如下：

- brew install node
- brew install watchman
- npm install -g react-native-cli
- gem install cocoapods

以上分别是安装Node、watchman、React Native命令行工具和CocoaPods的命令，安装过程中如果提示权限不够，在对应的命令前加上sudo即可。

如果搭建环境过程中出现问题，可以看一下参考目录中的第一篇文章。

### 初识RN

1. 创建项目

&emsp;&emsp;RN项目创建比较简单，执行 ***react-native init <项目名字>*** 即可。

![](./Images/rn1/1.png)

2. 工程目录结构

&emsp;&emsp;RN工程的目录结构如下：

![](./Images/rn1/2.png)

- android 和 ios 目录分包是安卓和iOS原生工程项目文件夹，其实本质上就是自动生成的测试工程，如果你需要把RN框架集成到原生项目中，可以不用关心这两个目录。
- index.android.js 是RN工程JS部分对应Android的入口
- index.ios.js 是RN工程JS部分对应iOS的入口 
- node_modules 是当前工程中所有的依赖包
- package.json 如下图，package.json描述了当前工程的依赖配置，可以修改这个文件增加、删除某个依赖库，然后使用npm install命令更新依赖包

![](./Images/rn1/3.png)

3. RN项目运行
- 运行npm install命令，更新工程依赖库
- 运行npm start命令，打包JS Bundle，启动本地服务器
- 运行工程目录中iOS或Android的测试工程

### 集成RN框架到现有项目中

上面介绍了怎么搭建开发环境，创建并运行了第一个RN工程，但实际项目应用中，通常是原生和RN混合使用：也就是某些页面或业务场景会使用RN开发，其他的页面继续用原生或者H5的方式开发。

### 开发、调试
1. IDE选择
2. 调试
3. Hot load
4. ATS对local server的影响

## Android篇

## 参考目录
- [React Native 环境搭建和创建项目](http://www.jianshu.com/p/a85cba2efb7a)
