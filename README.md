# Uni Design

技术栈:

- `Vue3`
- `TypeScript` 类型
- `Pinia` 状态管理
- `UnoCSS` 原子化 `CSS` 工具
- `iconify` 图标库
- 网络请求 `useRequest` 或 `useFetch`

## 项目整体结构

- `docs` 组件库文档
- `playground` 组件库游乐场
- `examples` 各种各样的示例`
- `materials` 设计图、各种参考资料和阅读材料
- `packages/cli` 脚手架工具
- `packages/core` 组件库核心代码

## 开发计划

### 工程化

- `Eslint`
- `Stylelint`
- `Markdownlint`
- `Prettier`
- `Husky`
- `Lint-Staged`
- `Sonar-Qube`
- `.vscode`

  - `settings.json`
  - `rec`
- `.editorconfig`

### 版本更新及说明

- 不同版本均有相应文档站点查阅, 任何版本均留有存档
- 版本更新遵循**向下兼容**的原则, 尽可能避免破坏式更新 (`breaking change`)
- 自动生成 `CHANGELOG.md`
- 自动发版, 版本号管理
- 控制台自动输出当前组件库版本信息

### 兼容列表及平台差异

- 目前仅考虑 `H5`、微信小程序平台, `H5` 可用于开发时调试 (效率高于小程序) 和 `playground`

### 配置

使用 `definConfig` 合并配置

#### 全局配置

`defineGlobalConfig`

#### 局部配置

`defineLocalConfig`

### CI/CD

#### H5

#### 微信小程序

### 国际化 I18n

### 组件

#### 组件按需引入 Tree Shaking

#### 组件名前缀

#### 组件分类

可参考现有的组件库的分类:

- [TMUI3.0](https://tmui.design/)
- [ThorUI](https://thorui.cn/doc/)
- [Wot Design Uni](https://wot-design-uni.pages.dev/)
- [Magic UI](https://magicui.design/docs/components/)

#### 组件设计指南

`Android` 和 `iOS` 官方设计规范

- [Human Interface Guidelines - iOS](https://developer.apple.com/design/human-interface-guidelines/)
- [Material Design - Google](https://m3.material.io/)

#### 组件清单

- `action-button`
- `ud.showModal(OBJECT)`

  - 对齐 [uni.showModal(OBJECT)](https://zh.uniapp.dcloud.io/api/ui/prompt.html#showmodal)
  同时可高度自定义以解决 `uniapp` 自带 `api` 的限制:
    - 根元素圆角、宽度、背景色等样式无法自定义
    - 由于是原生组件, 会随平台及相应设置不同而有所差异, 且在微信小程序中无法查看 `DOM`
    - 不支持修改按钮背景色, 仅支持传入按钮文本, 无法传入 html 字符串或插槽
  - `this.$confirm` (`Element`)
  - `ElMessageBox.confirm` (`Element Plus`)
  
- `time-picker`
- `tab-list`
- `medium-zoom` 图片放大效果
- `az-list` 仿微信通讯录列表
