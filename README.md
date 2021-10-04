# xmo-cli ![](https://img.shields.io/npm/l/xmo-cli.svg?sanitize=true) ![](https://img.shields.io/npm/v/xmo-cli.svg?sanitize=true)

旨在做最好的Vue3入门工具，且只关注 `Vue3 + Vite` 。

## 介绍

Cli创建项目，支持创建最新版 Vue3 的模板项目。本项目旨在提供最易上手的搭配项目质量管理的 `Vue3` 入门最佳实践。

项目模板具备足量**必用插件**的简单示例，共有分6个分支，**循序渐进，且都很简单易懂**，还可以作为拉取[热门](https://github.com/vitejs/awesome-vite#templates)的 `Vue3` 开源模板的工具。

> 本项目用到的插件如果你在开发中从来没有用过，那么说明你该用用了。

同时还支持为 `Vue3` 项目提供**质量管理初始化**和*Docker容器初始化*，一键添加相关配置，开箱即用。

**由于默认使用`yarn`作为项目包管理工具，所以请事先安装`yarn`以保证功能齐全**。

```bash
npm install -g yarn
```

## 安装教程

1. `npm install xmo-cli -g`

## 使用说明

### 📦 初始化项目

初始化Xmo-cli项目，项目细节请查看 <https://github.com/darkXmo/xmo-cli> 的除了 `master` 以外的各个分支。

1. `xmo-cli init [dir]` 
   
   ![image](https://user-images.githubusercontent.com/37503114/135218919-97b305b8-f801-4eca-bf48-878b45c0578e.png)
   
2. 按照指引输入对应内容进行操作

### ⚓ 安装开源项目

`xmo-cli` 收录了 <https://github.com/vitejs/awesome-vite#templates> 中比较热门的 `Vue3` 项目，且提供了镜像下载的方案，防止遇到境内 `github` 下载困难。

1. `xmo-cli create <dir>`

![image](https://user-images.githubusercontent.com/37503114/135219056-1f48af10-4788-467e-a47b-954f5d99f426.png)
![image](https://user-images.githubusercontent.com/37503114/135219230-f91d15a9-158f-4b75-b6a8-912444578151.png)

### ⚙️ 添加项目配置

`xmo-cli` 提供为`Vue3`项目一键添加质量管理配置（需要初始化git）和`Docker`配置的功能。

1. 一键添加质量管理工具配置（包括 `prettier` + `husky` + `lint-staged`，可选项 `commitlint` 、`eslint`）

  ```bash
  # 在项目根目录
  xmo-cli init -q
  
  # 如果项目中已经有了质量管理配置，为了防止冲突，你可能需要先删除它们。
  xmo-cli init -qf
  ```
  
  > Typescript 项目不提供 `Eslint` 质量管理配置方案。
  
  ![image](https://user-images.githubusercontent.com/37503114/135219417-e1a3d327-5117-4985-a8bd-9cbd047eada2.png)


2. 一键添加Docker配置（包括开发配置，打包配置和Nginx部署配置）。*开发中*

  ```bash
  # 在项目根目录
  xmo-cli init -d
  ```

## Help

默认情况下，所有新建项目都包含最新版 `vue3`、 `prettier` 及其默认配置、`vue-router`、`pinia`、`axios`。为保障最佳开发体验，推荐使用 `Visual Studio Code` 作为 `IDE` 进行开发。

所有项目拉取之后推荐第一时间阅读 `README.md` 和 `CHANGELOG.md` (如果有) 。

自动化构建通过读取并 `clone` 不同 `git` 分支下的内容后进行修改来实现项目初始化，当前支持从 `gitee` 和 `github` 上下载项目，请根据你的地理位置记性选择。

所有项目都推荐采用 `yarn` 作为依赖管理工具。

## 分支

🚀 默认推荐分支为 `ts/primary` 。(如果你使用`xmo-cli init [dir] -y`（添加-y参数）的话，将默认初始化该分支模板) 

### mini

`vue3` + `vue-router` + `pinia`  + `axios`。

难度系数 ★

知识面覆盖系数 ★★★

理解了这些代码，在不涉及特定UI框架的情况下，我认为可以覆盖**90%**的开发需求。

### primary

`vue3` + `vue-router` + `pinia`  + `axios` + `mitt` + `husky` + `eslint` + `commitlint + commitizen` 。

难度系数 ★☆

知识面覆盖系数 ★★★★

理解了这些代码，在不涉及特定UI框架的情况下，我认为可以覆盖**99%**的开发需求和质量管理配置需求。


### Typescript分支

将所有原项目改造成 `typescript` 版本。例如 `mini` => `ts-mini`。

## 初始化项目模板示例

![image](https://user-images.githubusercontent.com/37503114/135219728-46b6ba64-0dce-47af-9488-a0618bc6b44a.png)

### Mini

1. `setup` 使用示例
2. 页面自适应示例
3. 侧边栏自适应示例 ![image](https://user-images.githubusercontent.com/37503114/135219841-d3c5a07e-a685-45ee-8562-bb22d88df534.png)
4. `vue-router` 使用示例
5. `pinia` 使用示例
6. `axios` 使用示例
7. `prettier` 配置示例
8. `style` 的 `v-bind` 示例

### Primary

1. `Mitt` 示例
2. `eslint` + `commitlint` + `commitizen` + `husky` + `prettier` 项目质量管理示例
3. 导航栏跳转示例

### Typescript

1. `Vue3` 配置 `typescript` 示例
2. `api` + `interface` 接口使用示例

### 其它

✨ 如果需要添加其它项目分支，或认为某个开源项目最佳实践值得添加到 `cli` 中，或希望 `xmo-cli` 添加任何新的功能，都可以提交 `issue` 清单告知我。

✨ 如果你对初始化模板中的某个功能实现存在疑问，认为需要添加注释或进行修改、优化，请告知我或自行添加然后提请Request。

#### 感谢

感谢你的安装和使用。

#### 参与贡献

1. Fork 本仓库
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request
5. 欢迎添加其它项目分支
