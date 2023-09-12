---
#==> Theme
theme: ./theme
# theme: 'default'
# colorSchema: light

#==> Layout
layout: cover
class: bg-blend-overlay bg-black65
background: '/media/backgrounds/mountain-bike.jpeg'

#==> Fonts
fonts:
  # Normal Font
  sans: 'Poppins'
  # Serif Font
  serif: 'Playfair Display'
  # Code Font
  mono: 'Fira Code'
  # Provider
  provider: 'google'

#==> Code Highlighter
highlighter: shiki

remoteAssets: false

#==> Slide Info
title: 褚煦露-简历
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
---

<div class="center">
  	<h1 class="font-extrabold" style="line-height: 2rem !important;">褚煦露 Chu Xulu</h1>
  	<h3 class="font-300" style="opacity: 1;font-size: 12px">4+ 前端工作经验（抖音、科大讯飞）</h3>
    <h3 class="font-300" style="opacity: 1;font-size: 12px">北方工业大学（机械）GPA：3.68/4.0  </h3>
</div>

<div class="abs-bl ml-14 mb-12 flex items-center" >
	<img src="/media/avatar.jpeg" class="size-40px br-50p  object-cover-top no-decoration">
	<div class="ml-3 flex flex-col text-left">
		<!-- <span class="font-300">褚煦露</span> -->
		<!-- <span class="mt-1 fs-10px">8160334</span> -->
	</div>
</div>

<div class="abs-br mr-6 mb-12">
    <span
      @click="$slidev.nav.next"
      class="arrow-container cursor-pointer text-white"
      hover="bg-altBlue bg-opacity-75 text-white"
    >
      <carbon:chevron-right class="inline" />
    </span>
</div>

---
src: ./pages/about-me.md
---

---
src: ./pages/structure.md
---

---
src: ./pages/company.md
---

---
src: ./pages/project.md
---

<!-- --- -->
<!-- src: ./pages/users.md -->
<!-- --- -->

---
src: ./pages/architecture.md
---

<!-- --- -->
<!-- src: ./pages/techs.md -->
<!-- --- -->

---
src: ./pages/graphql.md
---

---
src: ./pages/process2.md
---

---
src: ./pages/process3.md
---

---
src: ./pages/processformat.md
---

---
src: ./pages/processshell.md
---

---
src: ./pages/processreadme.md
---

---
src: ./pages/future-work.md
---

---
src: ./pages/iflyteck.md
---

---
src: ./pages/more.md
---