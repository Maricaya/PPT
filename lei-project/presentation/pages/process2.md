---
layout: full
---

<h1 class="no-mb font-300">The Evolution of Front End Development Processes: 研发流程的进化</h1>
<h3 class="font-xs">
Material Design Systems 物料包 -> <strong><u>Micro Frontends 微前端</u></strong> -> Monorepo
</h3>
<br>

<div class="flex gap-4 mt-2">

<div style="width: 50%">
<v-clicks>


<div class="flex"> 背景 </div>
<br>
<div class="flex gap-1 font-300 text-sm items-start">
    - <span>Our repository has become increasingly large and difficult to maintain, turning into a "monolithic project." 
  <br/>我们的仓库，变得越来越庞大，越来越难以维护，成为<strong>“巨石项目”。</strong></span>
</div>
</v-clicks>
</div>

<div>

<v-clicks>
<h4 class="font-300 flex"><akar-icons:circle-check-fill class="text-success w-30px" /><strong> 解决方案: 微前端 </strong></h4>

<div class="flex flex-col gap-2 mt-2">
<div class="flex gap-1 font-300 text-sm items-start">
    - <span>
  By utilizing qiankun, we can split a project into different modules, where each module is independent and has its own Git repository. 
  <br/>
  使用 qiankun，把一个项目拆分成<strong>不同的模块</strong>，模块与模块之间<strong>互相独立</strong>，每个模块一个 git 仓库。</span>
</div>

```plaintext
+---------------------+
| Main Application    |
|                     |
| +-----------------+ |
| | Micro Frontend 1| |
| +-----------------+ |
|                     |     +---------------------+
| +-----------------+ | ->  | Shared Component    |
| | Micro Frontend 2| |     | Library             |
| +-----------------+ |     +---------------------+
|                     |
| +-----------------+ |
| | Micro Frontend 3| |
| +-----------------+ |
+---------------------+
```

</div>

</v-clicks>
</div>
</div>

