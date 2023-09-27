---
layout: two-cols
---

<template v-slot:default>
<h1 class="abs-bl font-extrabold">目录</h1>

<div class="flex flex-col gap-2 justify-between">
  <div class="flex flex-col gap-4">
    <v-clicks>
    <StructurePoint number="1" title="抖音 - 项目经历">
        <b>电子牵、乐小活、FollowMe</b>
    </StructurePoint>
    <!-- <StructurePoint number="2" title="抖音 - 技术">
        <b>前端架构</b>
    </StructurePoint> -->
    <StructurePoint number="2" title="研发流程的进化">
        <b>物料包 -> 微前端 -> Monorepo</b>
    </StructurePoint>
    <StructurePoint number="3" title="研发流程的规范">
        <b>gitflow、CI CD</b>
    </StructurePoint>
    <StructurePoint number="4" title="提效工具">
        <b>工具的解耦和统一管理</b>
    </StructurePoint>
    <StructurePoint number="5" title="工程化思维">
        <b>注重文档构建和输出，减少沟通成本</b>
    </StructurePoint>
    </v-clicks>
  </div>
  <!-- <div class="mt-5">
    <a href="https://gitlab.estg.ipp.pt/DSousa/lei_pf2021_8160334" class="inline-flex gap-2 items-center !hover:text-beapt text-sm">
      <jam-gitlab />
      Repositório
    </a>
  </div> -->
</div>

</template>
<template v-slot:right>

<div class="flex flex-col gap-4">
    <v-clicks>
    <!-- <StructurePoint number="5" title="工程化思维">
        <b>注重文档构建和输出，减少沟通成本</b>
    </StructurePoint> -->
    <StructurePoint number="6" title="抖音 - Follow Me">
        <b>担任后端开发工程师</b>
    </StructurePoint>
    <StructurePoint number="7" title="科大讯飞">
        <b>讯飞新高考门户</b>
    </StructurePoint>
    <StructurePoint number="8" title="我能为 CACS 做什么">
        <b>前端...</b>
    </StructurePoint>
    </v-clicks>
</div>
</template>