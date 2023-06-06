---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: 褚煦露的自我介绍
---

# 褚煦露 Chu Xulu

### 4+ 前端工作经验（抖音、科大讯飞）
<br>

##### 🎓 北方工业大学（机械）GPA：3.68/4.0  


---
layout: center
---

# 工作经历
<br>

### **高级前端开发工程师（2020.12-至今）**

**抖音集团（乐小活、电子牵、FollowMe）**
- 从 0 到 1 设计和开发复杂的 Web 多端应用程序。
- 管理前端团队。
- 在 FollowMe 团队中担任后端开发。

<br>

### **中级前端开发工程师（2019.03-2020.12）**

**科大讯飞（智慧教育）**
- 负责和产品经理、后端、UI 配合，完成页面的实现。
- 参与前端组件库以及常用工具的搭建，持续提高团队的生产效率。

---
layout: center
---

# 项目经历 - 抖音集团
<br>

### **乐小活 - 用科技助力灵活就业（2020.12-2022.10）**
https://pre.letfree.com/ 

乐小活综合服务平台，赋能**用工平台、税酬机构、自由职业者**。

<img
  class="w-120"
  src="/letfree.jpeg"
/>

---
layout: center
---

# 项目经历 - 抖音集团
<br>

### **电子牵 - 合同签约管理平台（2022.10-至今）**
https://www.letsign.com/ 

面向企业和个人的一站式文件签署&管理系统平台。

<img
  class="w-150"
  src="/letsign.png"
/>

---
layout: center
--- 

# 项目经历 - 抖音集团

- PC 、移动端，均以 <u>**React**</u> 为核心技术栈，使用了 <u>**React、React Hooks、hox、ByDesign React 和 qiankun**</u> 等技术栈

TODO: 放一个讲解视频【】
- https://juejin.cn/post/6847902224144662541
- https://juejin.cn/post/6847902217475735560
- https://juejin.cn/post/6844904201332457486
- https://juejin.cn/post/6845166891200167943
---
layout: center
--- 

### 研发流程的进化：**物料包** -> 微前端 -> Monorepo
<br>

>背景
>- 很多复用的代码片段在多个项目中拷贝，统一升级/改造管理上比较困难。
>- 新同学可能不知道类似的 UI 又自己写一套浪费时间。
>- 如果有统一的组件库、样式库 ，会让产品保持统一的 UI 界面和交互设计，让用户有更好的体验。

---
layout: center
--- 
### 研发流程的进化：**物料包** -> 微前端 -> Monorepo
<br>

>解决方案 - 物料包
> - 为了快速支撑业务，我们使用了 **lerna** 与 **dumi** 建立起 PC、移动端的物料包。
> - 完善了**物料包的单元测试用例、和 E2E 测试用例**。
>   - 建立对应的流水线，在代码上线前进行测试卡点，如果测试不通过，不允许上线。
> - 当然，物料包不仅仅是组件库，还包括**一切可以复用的代码**。
>   - 比如 **hooks、utils、css 样式**等等。

---
layout: center
---

###  研发流程的进化：物料包 -> **微前端** -> Monorepo
<br>

> 背景
>  - 团队维护的前端项目，随着时间推进，变得越来越庞大，越来越难以维护，成为“巨石项目”。
>  - 其他团队想切换技术栈，从 Vue 到 React，但是不想影响之前的 Vue 项目。

---
layout: center
---

### 研发流程的进化：物料包 -> **微前端** -> Monorepo
<br>

> 解决方案
>- 把一个项目拆分成**不同的模块**，模块与模块之间**互相独立**，每个模块一个 git 仓库。不同的模块交给不同的团队维护，**减轻每个程序员的负担**。
>- https://qiankun.umijs.org/zh/guide
>- qiankun 是一个基于 single-spa 的微前端实现库，使用它能够简单、无痛的构建一个生产可用微前端架构系统。

---
layout: center
---

### 研发流程的进化：物料包 -> 微前端 -> **Monorepo**
<br>

> 背景
> - 随着微前端在组内的应用，项目中 **git 仓库越来越多**。我们在开发一个需求时，往往要在**多个仓库中切换分支**，开发代码。
> - 随着物料包的增大，使用**基础库的层级越来越深**。如果想修改一个基础库的属性，往往需要修改多个仓库，并进行**多次发包**。

---
layout: center
---
### 研发流程的进化：物料包 -> 微前端 -> **Monorepo**
<br>

>解决方案：迁移到 Monorepo，monorepo是一种将多个项目放在一个仓库(git)中的代码管理模式。
>- 使用 rush 把各个分散的 git 仓库聚合在一起。
>- 收益：
>1. 按需编译：Rush 通过检测文件 / 依赖变化等进行按需编译。总体从 3min 提升到 30s，按需编译总体可达到 **20s** 左右。
>2. 把原来的物料包、项目包迁移在一个仓库里。当一个需求涉及多个项目时，只要在**一个 git 仓库**中开发即可，不需要多次切换仓库。
>3. 使用 **PNPM Workspace 进行本地包管理**，关联本地依赖。这样物料包无需发包就可以使用。
>4. 保证 CICD / ESLint / Prettier / Git Owners  等规范的**统一性**。

---
layout: center
---

### 规范研发流程：gitflow、CI CD
<br>

> 背景
> - 随着团队的不断扩大，每个小组有了一套自己的 Workflow ，一些研发流程未标准化（比如 GitFlow）。
> - 一些已经标准化的部分环节，没有放在 CI/CD 上，会阻塞研发流程。

---
layout: center
---

### 规范研发流程：gitflow、CI CD
<br>

>解决方案
  >- 在小组内开展圆桌会议，票选出统一的 **gitflow、code review** 标准。
  >- 让 CI/CD 做更多的事情，让开发者关注更少的细节
  >   - 物料包的 publish，交给 pipeline，而不是占用本地资源发包。
  >   - 业务工程接入 pipeline，lint / ut / e2e 等环节由 pipeline 集群完成校验，本地 lint 辅助保留。
  >    - 单元测试、E2E 卡点接入 pipeline。

  
---
layout: center
---

### 提效小工具
<br>

>一键切换测试环境
>- 背景：在敏捷开发过程中，我们往往是多个项目并行，所以会涉及多个前端、后端的开发环境。
>- 解决办法：为了方便切换环境，项目的页面打开后，右下角会有一个小 icon。点击后输入环境 id，将个人数据注入，就可以实现一键切换 BOE 环境的切换。

---
layout: center
---

### 工具的解耦和统一管理:
<br>

> 背景：
>  - 有一些不影响具体业务的工具比较分散，我们需要一个地方统一管理它们。
>  - 在需要复用工具的时候，只能 copy 一份过去。比如一个 shell 脚本需要在多个 git 仓库中使用，现在只能每个仓库都 copy 一份 shell 脚本的代码。

---
layout: center
---

### 工具的解耦和统一管理:
<br>

> 解决办法：
>  - 为了解决这个问题,我们可以在一台服务器上集中管理这些工具。
>  - 首先，把这些工具写成“plugin”(包括 Shell 脚本，JS、TS 等)。
>  - 然后，把这些插件信息和配置放在服务器上统一管理。
>  - 最后，我们写一个 node 工具，能自动从服务器上读取这些插件信息和配置。
>  - 当 Shell 脚本需要修改时，只需改一次，所有项目都能使用最新版。

> 我写的 plugin：
>  - git extensions 一套符合团队规范的 git 扩展。
>    - check out：用于快速生成符合团队命名规范的 feature/release/hotfix 分支。（比如：feature-1220-test-chuxulu）
>    - pre push：检查“当前分支”是否落后于“main”，保证正在开发的分支包含最新代码。

---
layout: center
---

### 工程化思维，注重文档构建和输出，减少沟通成本
<br>

>  - 提供新人 onboarding 文档
>  - 结构化 readme 文件：
>    - 减少沟通：新同事先查看 readme 解决疑问
>    - 提取 readme 模板：
>    - 减少研发过程中的沟通成本，对工程有疑问先看 readme，提升双边开发体验 
>    - 避免口口相传的传递信息，将工程信息以工程为载体做更便捷的沉淀
>    - 输出 readme 模版，改造时直接 copy 即可
>  - 微信小程序开发踩坑总结：在小程序开发过程中遇到了一些问题，把它们记录下来，给还没有遇到的同学做个参考。
>  - 乐小活，资金篇章分享：被同事评价为，见过最详细的业务分享。

---
layout: center
class: ' pb-5 :'
---

# 抖音 Follow Me（2021.06-至今）

用户引导自助配置平台，集用户引导、功能上新、帮助中心、用户分群、埋点圈选、线索收集等客户帮助体系，以解放研发生产力。

- 担任后端开发工程师，使用 **Nest.js、Sequelize、TypeScript 和 MySQL** 构建 RESTful APIs，同时负责数据库的设计和维护。
- 为前端提供高质量的 service API，使用 Nginx 实现资源动静分离、Gzip 压缩和反向代理配置等功能。

<br/>

# Next.js 学习记录
Next.js blog 在 github 上有 27 stars：https://github.com/Maricaya/nextjs-blog)
- [Next.js + TypeScript 入门之项目搭建、三种渲染方式（BSR、SSG、SSR）](https://juejin.im/post/6855917901090652174)
- [TS + TypeORM 踩坑实践 (一) hello ORM](https://juejin.im/post/6857391336929263624)
- [TS + TypeORM 踩坑实践 (二) 操作数据表](https://juejin.im/post/6858509402798817294)
- [从 0 开始部署你的 Node 应用(Ubantu、docker、nginx)](https://juejin.im/post/6864785804066029575)

---
layout: center
class: 'pb-5 :'
---

# 讯飞新高考门户（2019.03-2020.12）
包括智能排课、智能考务等 25 个 H5 + PC 项目。
- 均以 Vue 为核心技术栈，基于 Vue-Cli 脚手架，Vuex 进行状态管理，配合 iView、Element 等 UI 框架进行业务开发，并使用 Webpack 完成打包构建。
- 综合服务项目接手时代码结构混乱，引入 TypeScript 解决类型不清晰的问题。
- 将公共组件、方法、样式与非业务模块等进行封装，在开发过程中不断完善公共依赖库，并在项目各个组件中得以复用，提升开发效率。
- 使用虚拟列表优化大数据表格，加载 2 万条数据时，页面首次加载速度由 1s 缩短至 120ms。
- 优化 Webpack 构建速度，智能排课构建速度从 2 分钟缩短至 30 秒。

---
layout: center
class: 'pb-5 :'
---

# 新高考组件库（2020.03-2020.12）

一套基于 Vue 的业务组件库，共计 23 个，避免重复造轮子，提高效率。
- 负责并使用 Webpack 4.0 进行组件库的搭建，采用 UMD / Common JS / ES Module 的模块化规范打包。
- 使用 ESLint 配置代码规范，使用 husky 进行提交前的本地代码风格检查。
- 结合 Vue 的异步组件和 Webpack 的代码分割，实现组件库的按需引入。
- 使用 gulp.js 打包 CSS，实现 CSS 的按需引入。
- 负责公共样式的维护，抽离 Less 样式变量，实现主题色自定义配置。

---
layout: center
class: 'pb-5 :'
---
# 期待方向
- 👨‍💻 去美国留学，学习新的技术。
- 您的招生信息，简直像为我设计的！
  - DePaul 有非常先进电子教育体系，在课后还能继续看上课的视频，学生可以反复观看，不用担心错过课程内容。
  - DePaul 有非常好的游戏专业，学生可以接触最新的游戏设计、开发和游戏制作工具。
  - DePaul 坐落在芝加哥，这里有低房价和丰富的餐厅。

---
layout: center
class: 'text-center pb-5 :'
---

# Thank You!
