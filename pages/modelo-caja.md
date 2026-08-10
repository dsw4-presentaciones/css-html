---
# El modelo de caja
layout: two-cols
layoutClass: gap-4
---
# El modelo de caja CSS

- Se utiliza con fines de diseño y maquetación web.
- Trata de una caja que envuelve a cada elemento HTML.
- Cada caja consta de cuatro partes: contenido (content), relleno (padding), bordes (border) y márgenes(margin).

::right::

## 📦 CSS Box Model

<div class="box-model">
  <div class="layer margin-box" data-label="MARGIN">
    <div class="layer border-box" data-label="BORDER">
      <div class="layer padding-box" data-label="PADDING">
        <div class="layer content-box">
          <span class="content-title">CONTENT</span>
          <span class="content-description">Text · Images · Components</span>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="box-flow">
  <span class="tag tag-margin">Margin</span>
  <span class="arrow">&rarr;</span>
  <span class="tag tag-border">Border</span>
  <span class="arrow">&rarr;</span>
  <span class="tag tag-padding">Padding</span>
  <span class="arrow">&rarr;</span>
  <span class="tag tag-content">Content</span>
</div>

<style>
.box-model {
  max-width: 680px;
  margin: 1.5rem auto 1rem;
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
}

/* Layer Structure & Hover Focus */
.layer {
  position: relative;
  border-radius: 8px;
  transition: all 0.25s ease-in-out;
}

.layer::before {
  content: attr(data-label);
  position: absolute;
  top: 6px;
  left: 10px;
  font-size: 0.65rem;
  font-weight: 800;
  letter-spacing: 0.1em;
  opacity: 0.8;
}

.margin-box {
  background: rgba(249, 115, 22, 0.15);
  border: 2px dashed #f97316;
  padding: 2.2rem 1.8rem 1.2rem;
  color: #c2410c;
}

.border-box {
  background: rgba(234, 179, 8, 0.2);
  border: 4px solid #eab308;
  padding: 2rem 1.5rem 1.2rem;
  color: #a16207;
}

.padding-box {
  background: rgba(34, 197, 94, 0.2);
  border: 2px dashed #22c55e;
  padding: 1.8rem 1.2rem 1.2rem;
  color: #15803d;
}

.content-box {
  background: rgba(59, 130, 246, 0.25);
  border: 2px solid #3b82f6;
  padding: 1.2rem;
  text-align: center;
  color: #1d4ed8;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.layer:hover {
  filter: brightness(1.15);
  transform: scale(1.008);
}

.content-title {
  font-size: 1.2rem;
  font-weight: 900;
  letter-spacing: 0.05em;
}

.content-description {
  font-size: 0.8rem;
  opacity: 0.85;
}

/* Bottom Flow Legend Fixes */
.box-flow {
  display: flex !important;
  justify-content: center !important;
  align-items: center !important;
  gap: 0.75rem !important;
  margin-top: 1.5rem !important;
  font-weight: 600;
  font-size: 0.9rem;
}

.tag {
  padding: 0.35rem 0.85rem !important;
  border-radius: 6px !important;
  font-weight: 700 !important;
  display: inline-block !important;
  transition: transform 0.2s ease;
}

.tag:hover {
  transform: translateY(-2px);
}

.tag-margin  { background-color: #f97316 !important; color: #ffffff !important; }
.tag-border  { background-color: #eab308 !important; color: #1c1917 !important; }
.tag-padding { background-color: #22c55e !important; color: #ffffff !important; }
.tag-content { background-color: #3b82f6 !important; color: #ffffff !important; }

.arrow {
  color: #9ca3af !important;
  font-size: 1.2rem !important;
  font-weight: bold !important;
  display: inline-block !important;
}
</style>

---
# Ejemplo 1 del modelo de cajas
---
# Ejemplo 1 del modelo de cajas

<TabsMe>

<template #html>

```html
<div>
  This text is the content of the box...
</div>
```

</template>

<template #css>

```css
div {
  background-color: lightgrey;
  width: 300px;
  border: 15px solid green;
  padding: 70px;
  margin: 50px;
}
```

</template>

<template #result>

<div class="box-example">
    <h3>Título de la caja</h3>
    <p>Contenido de la caja</p>
</div>

  <style>
    .box-example {
      background-color: lightgrey;
      width: 300px;
      border: 15px solid green;
      padding: 15px;
      margin: 125px;
    }

    .box-example h3 {
      margin-top: 0;
    }
  </style>
</template>

</TabsMe>

---
# Propiedades margin, border y padding
---
# Propiedades margin, border y padding
## margin: "top-margin right-margin bottom-margin left-margin";

```css
margin: 100px 20px 50px 370px;
```
<h2>padding: "padding-top|padding-right|padding-bottom|padding-left";</h2>

```css
    padding: 20px 30px 50px 70px;
```
<h2>
border : "width style color | initial | inherit";
</h2>
```css
    border: 10px solid red;
```