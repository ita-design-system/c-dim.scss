---
title: Box-sizing
description: Modifieurs c-dim dédiés à la propriété box-sizing
layout: libdoc/page-split
order: 300
---
```html
<div class="c-dim">Comportement c-dim par défaut <br>box-sizing: border-box</div>
<div class="c-dim m-bsizing-content">m-bsizing-content <br>box-sizing: content-box</div>
<p>Pour chaque boîte :</p>
<ul>
    <li>width: 300px</li>
    <li>padding: var(--ita-spacing-4)</li>
    <li>border: 20px solid var(--ita-color-primary-900)</li>
</ul>
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-100);
        color: var(--ita-color-primary-800);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        padding-bottom: 50vh;
    }
    .c-dim {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-neutral-100);
        width: 300px;
        border: 20px solid var(--ita-color-primary-200);
        margin-top: var(--ita-spacing-6);
    }
</style>
```
{:.playground title="Modifieurs pour le box-sizing"}


