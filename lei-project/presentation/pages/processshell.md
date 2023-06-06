---
layout: full
---

<h1 class="no-mb font-300">工具的解耦和统一管理：</h1>
<h3 class="font-xs">shell</h3>
<br>

<div class="flex gap-4 mt-2">

<div style="width: 50%">
<v-clicks>


<div class="flex"> 背景 </div>
<br>
<div class="flex gap-1 font-300 text-sm items-start">
    - <span> 有一些不影响具体业务的工具比较<strong>分散</strong>，我们需要一个地方统一管理它们。</span>
</div>

</v-clicks>
</div>

<div>

<v-clicks>
<h4 class="font-300 flex"><akar-icons:circle-check-fill class="text-success w-30px" /><strong> 解决方案</strong></h4>

<div class="flex flex-col gap-2 mt-2">

<div class="flex gap-1 font-300 text-sm items-center">
    - <span>为了解决这个问题，我们可以在一台服务器上集中管理这些工具。</span>
</div>

<div class="flex gap-1 font-300 text-sm items-center">

```
+----------------------------------------------------+
|  +----------------+  +----------------+           |
|   服务器                   Node Tool               |
|   记录插件信息           自动从服务器上读取信息         |
|  +----------------+  +----------------+           |
|  | - Plugin Config|  | - Read Plugin  |           |
|  | - Plugin Info  |  |  Info from     |           |
|  | - Plugin Path  |  |  Server        |           |
|  | - Plugin Author|  | - Load Plugin Config       |
|  +----------------+  +----------------+           |
+----------------------------------------------------+
|                                                   |
|    Git Extensions 我写的插件                        |
|   - Check Out         - Pre Push                  |
|      - Feature          - Check                   |
|      - Release          - Update                  |
|      - Hotfix                                     |
+----------------------------------------------------+
```
</div>


</div>

</v-clicks>
</div>
</div>