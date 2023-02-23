---
title: Scroll snap
description: Modifieurs c-dim dédiés aux accroches durant le défilement
layout: libdoc/page-split
order: 170
---
```html
<h2>Avec m-scrollst-x-mandatory sur ul et m-scrollsa-start sur li</h2>
<ul class="c-dim m-scrollst-x-mandatory" id="snap-x">
    <li class="c-dim m-scrollsa-start">1</li>
    <li class="c-dim m-scrollsa-start">2</li>
    <li class="c-dim m-scrollsa-start">3</li>
</ul>
<h2>Avec m-scrollst-x-mandatory sur ul et m-scrollsa-center sur li</h2>
<ul class="c-dim m-scrollst-x-mandatory" id="snap-x-center">
    <li class="c-dim m-scrollsa-center">1</li>
    <li class="c-dim m-scrollsa-center">2</li>
    <li class="c-dim m-scrollsa-center">3</li>
</ul>

<h2>Avec m-scrollst-y-mandatory sur ul et m-scrollsa-start sur li</h2>
<ul class="c-dim m-scrollst-y-mandatory" id="snap-y">
    <li class="c-dim m-scrollsa-start">1</li>
    <li class="c-dim m-scrollsa-start">2</li>
    <li class="c-dim m-scrollsa-start">3</li>
</ul>
<h2>Avec m-scrollst-y-mandatory sur ul et m-scrollsa-center sur li</h2>
<ul class="c-dim m-scrollst-y-mandatory" id="snap-y-center">
    <li class="c-dim m-scrollsa-center">1</li>
    <li class="c-dim m-scrollsa-center">2</li>
    <li class="c-dim m-scrollsa-center">3</li>
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
    }
    ul {
        display: flex;
        width: 100%;
        gap: var(--ita-spacing-6);
        background-color: var(--ita-color-primary-200);
        color: var(--ita-color-neutral-100);
        padding: var(--ita-spacing-0);
        list-style: none;
        overflow: auto;
    }
    li {
        background-color: var(--ita-color-primary-500);
        padding: var(--ita-spacing-10);
        font-size: var(--ita-font-size-10);
        min-width: 100vw;
    }
    #snap-y {
        flex-direction: column;
        height: var(--ita-spacing-13);
        text-align: center
    }
    #snap-y-center {
        flex-direction: column;
        height: var(--ita-spacing-13);
        text-align: center
    }
    #snap-y-center li {
        padding: var(--ita-spacing-11) 0;
    }
    #snap-x-center .m-scrollsa-center {
        text-align: center;
    }
</style>
```
{:.playground title="Modifieurs pour les accroches durant le défilement"}


