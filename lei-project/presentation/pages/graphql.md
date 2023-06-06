---
layout: full
---

<h1 class="no-mb font-300">研发流程的进化</h1>
<h3 class="font-xs">
<strong><u>物料包</u></strong>
 -> 微前端 -> Monorepo
</h3>
<br>

<div class="flex gap-4 mt-2">

<div style="width: 50%">
<v-clicks>


<div class="flex"> 背景 </div>
<br>
<div class="flex gap-1 font-300 text-sm items-start">
    - <span>在多个项目中很多重复的<strong>代码片段...</strong></span>
</div>

</v-clicks>
</div>

<div>

<v-clicks>
<h4 class="font-300 flex"><akar-icons:circle-check-fill class="text-success w-30px" /><strong> 解决方案:物料包 </strong></h4>

<div class="flex flex-col gap-2 mt-2">

<div class="flex gap-1 font-300 text-sm items-center">
    - <span>使用 <strong>lerna</strong> 与 <strong>dumi</strong> 建立起 PC、移动端的物料包。</span>
</div>

```bash
material-package/
 ├─ package.json          # 根 package.json 文件
 ├─ dist/                 # 打包生成的组件
 ├─ mock/                 # Mock 数据
 ├─ src/                  # 组件、业务代码
 │   ├─ components/      # 组件
 │   │   ├─ Button/      # Button 组件
 │   │   │    ├─ index.tsx
 │   │   │    ├─ .storybook/   
 │   │   ├─ Checkbox    
 │   ├─ hooks/            # Hook函数
 │   ├─ utils/            # 工具函数
 │   ├─ styles/           # 样式文件
 │   └─ index.ts          # 导出文件
 ├─ .umirc.ts             # Dumi 配置
 ├─ test/                 # 单元测试
 ├─ jest.config.js        # Jest 配置   
 └─ package.json          # 子 package.json 文件
```

</div>

</v-clicks>
</div>
</div>