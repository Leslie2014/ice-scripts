# Changelog

## 2.1.11

- [fix] error mimetype of image
- [feat] support --disable-mock to disable mock server

## 2.1.10

- [fix] refactor mock dev server alibaba/ice#2455 alibaba/ice#2471 alibaba/ice#2462
- [fix] modular-import did not work with ice-plugin-component alibaba/ice#2724
- [feat] add dll plugin for ice-scripts
- [fix] write header for proxy request when error ocur
- [feat] support calculate color variables for multi-theme alibaba/ice#2715

## 2.1.9

- [fix] lock less verison to 3.9.0 less/less.js#3414

## 2.1.8

- [fix] add polyfill when entry path include node_modules

## 2.1.7

- [fix] add polyfill when entry modified by plugin
- [fix] require modules in shim file
- [feat] support css localize in dev mode

## 2.1.6

- [fix] remove check latest version of ice-scripts alibaba/ice#2517
- [fix] modify collect params
- [fix] use core-js and regenerator-runtime instead of @babel/polyfill
- [feat] ice-plugin-jsx-plus for support jsx+

## 2.1.5

- [feat] 支持非终端场景下构建日志的输出

## 2.1.4

- [feat] 支持 `ice-scripts test <regexForTestFiles>` 指定测试文件
- [fix] 修复 node-sass 依赖检查错误时进程退出问题

## 2.1.3

- [feat] 支持 ice-scripts test 命令
- [fix] 修复 ice-plugin-fusion 1.x组件主题 icon 编译问题
- [fix] ice-plugin-smart-debug 开启调试参数变更为 `smartDebug`

## 2.1.2

- [feat] 支持通过 `--config` 指定配置文件 #2188
- [feat] 启动时 Node 环境检测 #2145
- [fix] 修复 Windows 下构建输出路径问题 #2166
- [feat] 新增 ice-plugin-wrap-code 插件，支持编译后的脚本注入
- [feat] 新增 ice-plugin-load-asset 插件，支持资源加载
- [feat] 新增 ice-plugin-smart-debug 插件，支持代码调试

## 2.1.1

- [fix] 修改命令参数失效问题

## 2.1.0

- [feat] watch ice.config.js changed and restart dev
- [feat] hash option support string
- [fix] build error exit code
- [chore] add collect

## 2.0.2

- [fix] 修复 copy 插件未使用自定义 output 问题

## 2.0.1

- [fix] 修复多 entry 下 html 入口问题

## 2.0.0

- [feat] 工程命令由 `ice` 变更为 `ice-scripts`，废弃 `--project-type`、`--sourcemap`、`--inject-babel`、`--debug` 和 `--hash` 参数
- [feat] 将 `ice.config.js` 作为项目的配置文件，废弃 `package.json` 中的 `buildConfig`、`themeConfig`
- [feat] 支持通过插件机制扩展工程能力


## 1.10.1

- [fix] 组件&区块 build 指定 publicPath #1849
- [fix] 修复https证书无效问题
- [fix] 资源路径引用问题 #1856
- [chore] 初始化物料使用 ejs 语法替换 handlebars

## 1.10.0

- [feat] 组件开发支持 importStyle 能力 #1755
- [fix] 组件开发 export default from 报错问题 #1763
- [chore] 不再锁死依赖版本 #1794
- [feat] 支持 `add block` 命令 #1791
- [feat] 支持 `init block/component` #1790
- [feat] 内置 block 的 buildConfig，entry/output #1817
- [fix] 修复自定义 output.publicPath 的问题 #1821
- [feat] 组件 src->lib 支持 ts，同时将 style.js 的生成逻辑后置 Close #1800

## 1.9.4

- [fix] 将 webpack 固定在 `4.28.x`，解决 npm 扁平化 + webpack 4.29 导致动态 import 语法报错问题
- [feat] 优化 getEntry 逻辑，支持传统多页面需求
- [feat] 增加 copyplugin，将 public 里的文件 copy 到 build
- [feat] uniteBaseComponent 支持指定基础包名
- [fix] 修复 babelImportConfig 不支持数组的问题
- [chore] 补全业务组件的升级版本数据

## 1.9.3

- [fix] 内网 init 项目未生成 abc.json
- [fix] 组件 build 未合并自定义 buildConfig
- [chore] 接入 ice-npm-utils

## 1.9.2

- [fix] 移除掉 babel-runtime 的 alias，防止项目依赖里有不同版本导致无法构建
- [chore] 不写死 webpack 的依赖版本，防止多份 webpack 导致构建报错

## 1.9.1

- [fix] 修复 @babel/runtime alias 路径错误问题

## 1.9.0

- [feat] 支持 init 项目
- [feat] 支持 dev/build 区块&业务组件
- [feat] 新增 buildConfig.disableVendor 配置
- [feat] dev/build 前检测是否已安装依赖
- [chore] 移除部分无用的依赖

## 1.8.13

- [feat] 内置对 moment 的多语言优化
- [feat] 支持 outputAssetsPath 配置
- [fix] 修复 externals 的逻辑

## 1.8.12

- [fix] 修复 proxy target 语法错误

## 1.8.11

- [fix] console.log 拼错

## 1.8.10

- [feat] 通过 `buildConfig.uniteBaseComponent` 将不同的基础包做统一
- [fix] 依赖 typescript，解决云构建时找不到依赖的问题
- [feat] 新增依赖检测功能：多版本、多基础组件、错误版本的业务组件等
- [fix] 修复主题包 icons.scss 未构建问题
- [fix] Proxy 支持更多配置
- [feat] 支持 buildConfig.babelExclude
- [feat] 支持 buildConfig.babelPluginImportConfig

## 1.8.9

- [fix] 依赖 axios

## 1.8.8

- [feat] 支持构建 ts 语法
- [chore] 增加埋点

## 1.8.8

- [feat] 支持 TypeScript 构建

## 1.8.7

- [fix] ice-scripts 不固定ICE官方维护的包版本（ice-skin-loader&webpack-plugin-import）

## 1.8.6

- [fix] 修复 iceworks node 项目路径获取错误的问题

## 1.8.5

- [chore] 升级 ice-skin-loader 到 0.2.1

## 1.8.4

- [feat] 通过对命令行参数 --project-type 添加参数，增加对 iceworks 中生成的 node 项目的支持。

## 1.8.3

- [fix] 修复默认开启 UglifyJsPlugin sourceMap 引起的内存溢出问题，更新为默认关闭 sourceMap

## 1.8.2

- [chore] 降级 webpack-plugin-import 到 0.2.1 解决部分组件样式引入失败的问题

## 1.8.1

- [feat] 支持 css-module，仅对 `.module.[css/less/scss]` 文件后缀生效
- [feat] 命令行参数支持 --sourcemap
- [chore] 升级 webpack-plugin-import 到 0.2.2

## 1.8.0

- [fix] 没有配置 theme 也需要走 ice-skin-loader 的逻辑
- [chore] 升级 ice-skin-loader 到 0.2.x
- [chore] 移除 css-prefix-plugin

## 1.7.9

- [feat] build 支持 `customWebpackConfig` 参数
- [chore] 移除 ice-scripts 命令

## 1.7.8

- [chore] dev 模式下第一次编译成功后自动用本地浏览器打开对应地址

## 1.7.7

- [Fix] 修复 mini-css-extract-plugin 升级到 0.4.2 后报大量 warning ([issue #1057](https://github.com/alibaba/ice/issues/1057))
- [Fix] 修复设置 localization 时的路径引用问题 ([pull #1073](https://github.com/alibaba/ice/pull/1073))
