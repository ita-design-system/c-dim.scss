---
title: Hauteurs
description: Modifieurs c-dim dédiés aux hauteurs
layout: libdoc/page-split
order: 150
---
```html
<div class="c-dim">c-dim tout seul n'a pas d'effet</div>
<div class="c-dim m-h-100">m-h-100<br>height: 100%</div>
<div class="c-dim m-h-100vh">m-h-100vw<br>height: 100vh</div>
<div class="c-dim m-h-auto">m-h-auto<br>height: auto</div>
<div class="c-dim m-maxh-100">m-maxh-100<br>max-height: 100%</div>
<div class="c-dim" m-h-100vh="xs">height: 100vh sur écrans xs</div>
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
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-neutral-100);
        border: var(--ita-border-6);
        padding: var(--ita-spacing-4);
    }
</style>
```
{:.playground title="Modifieurs hauteurs"}


