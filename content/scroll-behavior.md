---
title: Scroll behavior
description: Modifieurs c-dim dédiés au comportement durant le défilement
layout: libdoc/page-split
order: 170
---
```html
<h2>Avec m-scrollb-smooth</h2>
<a href="#a1">1</a> 
<a href="#a2">2</a>
<a href="#a3">3</a>
<ul class="c-dim m-scrollb-smooth">
    <li id="a1">1</li>
    <li id="a2">2</li>
    <li id="a3">3</li>
</ul>

<h2>Sans m-scrollb-smooth</h2>
<a href="#b1">1</a> 
<a href="#b2">2</a>
<a href="#b3">3</a>
<ul>
    <li id="b1">1</li>
    <li id="b2">2</li>
    <li id="b3">3</li>
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
        min-width: calc(var(--ita-spacing-11) * 12);
    }
</style>
```
{:.playground title="Modifieurs pour le comportement durant le défilement"}


