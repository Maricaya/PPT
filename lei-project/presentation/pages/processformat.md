---
layout: full
---

<h1 class="no-mb font-300">规范研发流程：</h1>
<h3 class="font-xs">gitflow、CI CD...</h3>
<br>

<div class="flex gap-4 mt-2">

<div style="width: 50%">
<v-clicks>


<div class="flex"> 背景 </div>
<br>
<div class="flex gap-1 font-300 text-sm items-start">
    - <span>随着团队的不断扩大，每个小组有了一套自己的 Workflow ，一些研发流程未标准化。</span>
</div>

</v-clicks>
</div>

<div>

<v-clicks>
<h4 class="font-300 flex"><akar-icons:circle-check-fill class="text-success w-30px" /><strong> 解决方案</strong></h4>

<div class="flex flex-col gap-2 mt-2">

<div class="flex gap-1 font-300 text-sm items-center">
    - <span>如今，我们已经将很多流程标准化，并集成到 <strong>CI/CD</strong> 中，让开发者关注更少的细节。</span>
</div>
<div class="flex gap-1 font-300 text-sm items-center">

1. 物料包的 publish，交给 pipeline，而不是占用本地资源发包。
2. 业务工程接入 pipeline，<strong>lint / ut / e2e</strong>  等环节由 pipeline 集群完成校验。 
</div>

```
 Code Review   -> 物料包发布  -> Lint/UT/E2E -> Build -> 小流量发布 -> 全流量发布
```

</div>

</v-clicks>
</div>
</div>