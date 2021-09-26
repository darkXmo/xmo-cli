# Vue 3 + Vite + Xmo-Cli-Mini

本模板将帮助你使用 `Vite` 进行 `Vue3` 开发，并已经注册了开发中将会使用的通用插件，具体使用插件参照[功能点示例](##功能点示例) 。模板以 `Vue3.2` 的特性为基础，使用了 `style + v-bind` 和 `script setup` 特性，对于这些特性不了解的用户请参照官方文档。

## 推荐使用IDE（强烈）

- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.volar)

  Volar（Vue Language Features (Volar)） 能为你提供最新最完善的开发提示。

  VSCode 插件

  - Prettier

## 推荐编码规则

所有的组件都采用驼峰命名（如 TemplateComponent），组件统一首字母大写，`js` / `ts` 文件统一首字母小写。所有接口（`Interface`）统一首字母大写。所有 `style` 文件都采用 `sass` 语言。

## 主要页面

`About`：关于 `Vue3` 的最基础的功能。

`Login`：登录页面，演示了如何进行 `Vue3` 最基础的登录。

`Home` ：自适应页面，演示了如何调用 `services` 接口，如何使用 `@media` 进行项目页面自适应，如何对导航栏进行自适应，如何调用后端接口。

`404`：404页面

## 项目依赖

`axios`、 `pinia`、 `sass`、 `vue`、 `vue-router` 

### 开发依赖

`prettier` 。

## 功能点示例

| 功能                | 文件                             |
| ------------------- | -------------------------------- |
| 页面布局            | @/layouts                        |
| 项目分层            | @/api 、 @/services              |
| Vue-Router 的使用   | @/router、@/pages                |
| Pinia 的使用        | @/store                          |
| 异步 Axios 的封装   | @/api                            |
| proxy 开发代理设置  | vite.config.ts                   |
| prettier 配置       | .prettierrc.json                 |
| public 静态目录引用 | @/components/Page/Header(avatar) |
| 404 页面            | @/pages/NotFound、@/router       |
| 两栏布局            | @/layouts/Login                  |
| 侧边布局            | @/layouts/Default                |
| 自适应布局          | @/layouts/Default                |

