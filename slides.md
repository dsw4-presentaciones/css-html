---
# You can also start simply with 'default'
theme: seriph
#background: /PORTADA.jpeg
layout: image
image: /portada.jpeg
backgroundSize: contain
# some information about your slides (markdown enabled)
title: HTML 5 & CSS3
info: |
  ## HTML 5 y CSS3
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
colorSchema: light
hideInToc: true
themeConfig:
  primary: '#005A9C'
---


<br> <br>
<div style="font-size: 30px;">
  HTML 5 & CSS3
</div>
 <br>
IF0009 Desarrollo de software IV
<br>

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Espaciadora para avanzar <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/progra2-presentaciones/css-html.git" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
layout: two-cols
layoutClass: gap-16
hideInToc: true
---

# Tabla de contenidos

::right::

<Toc text-sm minDepth="1" maxDepth="1" />

---
# Preparacion de Ambiente
src: ./pages/preparacionAmbiente.md
---
---
# Desarrollo web
src: ./pages/web-dev.md
---
---
# CSS
src: ./pages/css.md
---
---
# Selectores CSS
src: ./pages/selectores.md
---
---
# Box Model
src: ./pages/modelo-caja.md
---
---
# Referencias
src: ./pages/referencias.md
---


