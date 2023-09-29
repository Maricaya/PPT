---
layout: full
---

<h1 class="no-mb font-300">研发流程的进化</h1>
<h3 class="font-xs">
Material Design Systems 物料包
 -> Micro Frontends 微前端 -> <strong><u>Monorepo</u></strong>
</h3>
<br>

<div class="flex gap-4 mt-2">

<div style="width: 50%">
<v-clicks>


<div class="flex"> Background 背景 </div>
<br>
<div class="flex gap-1 font-300 text-sm items-start">
    - <span>With the implementation of micro-frontends within our team, the number of Git repositories in our project has increased significantly.
  <br/>
  随着微前端在组内的应用，项目中 <strong>git 仓库越来越多。</strong></span>
</div>
<div class="flex gap-1 font-300 text-sm items-start">
    - <span>
  As the size of our material package grows, the hierarchy of using foundational libraries becomes increasingly complex. If we want to modify a property of a foundational library, it often requires making changes in multiple repositories and multiple package releases.
  <br/>
  随着物料包的增大，使用<strong>基础库的层级越来越深</strong>。如果想修改一个基础库的属性，往往需要修改多个仓库，并进行<strong>多次发包</strong>。</span>
</div>

</v-clicks>
</div>

<div>

<v-clicks>
<h4 class="font-300 flex"><akar-icons:circle-check-fill class="text-success w-30px" /><strong> 解决方案: 迁移到 Monorepo </strong></h4>

<div class="flex flex-col gap-2 mt-2">

<div class="flex gap-1 font-300 text-sm items-center">
    - <span>We used Rush.js to aggregate various scattered Git repositories together.
  <br> 使用  <strong>Rush.js</strong> 把各个分散的 git 仓库聚合在一起。</span>
</div>
<div class="flex gap-1 font-300 text-sm items-center">
    - <span>By using Rush.js, we can streamline the process of making changes and upgrades, resulting in improved development efficiency. <br/>方便变更与升级、提高研发效率</span>
</div>

```
+------------------------------------+
|            Monorepo                |
+------------------------------------+
|                                    |
|  +----------------+  +----------+  |
|  |  Package A     |  | Package B|  |
|  +----------------+  +----------+  |
|  |                |  |          |  |
|  |    Component 1 |  |  Component 3|
|  |    Component 2 |  |  Component 4|
|  |                |  |          |  |
|  +----------------+  +----------+  |
|                                    |
|                                    |
+------------------------------------+
```
</div>


</v-clicks>
</div>
</div>

