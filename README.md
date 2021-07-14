# 基于React的桌面应用程序开发

## React
React 是一个用于构建 UI 的 JavaScript 库

# Node.js
Node.js 是一个开源与跨平台的 JavaScript 运行时环境

## Electron
Electron是一个使用JavaScript、HTML和CSS构建卓桌面应用程序的框架
它将 Chromium 和 Node.js 嵌入到二进制代码中。

### 开发流程

`makdir porject`然后`cd project`之后要用`npm init`来初始化一些包

然后将`Electron`包安装到应用的开发依赖中：`npm install --save-dev electron`

最后，在`package.json`配置文件中的`scripts`字段增加一条`"start": "electron ."`

这样就可以用`npm start`命令在开发者模式下打开该应用


#### 使用 Electron Forge 打包应用程序

`npm install --save-dev @electron-forge/cli`将Electron Forge添加到我的应用的开发依赖中

`npx electron-forge import`使用它的`import`命令来设置Forge的脚手架

`npm run make`使用Forge的make命令来创建可分发的应用程序




### 进程模型
Electron控制着两种类型的进程：主进程和渲染器进程

每个Electron应用都有一个单一的主进程，作为应用程序的入口点，

在node.js环境中运行，这意味着它有require模块和所有Node.js API的能力

### package.json 和 package-lock.json
package.json记录当前项目所依赖模块的版本信息

package-lock.json记录了node_modules目录下所有模块的具体来源和版本号以及其他的信息。