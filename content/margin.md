---
title: Margin
description: Modifieurs c-dim dédiés aux marges
layout: libdoc/page-split
order: 350
---
```html
<div class="c-dim m-m-auto" id="foo">m-m-auto <br>Permet de center un élément d'une largeur spécifique dans son conteneur.</div>

<article>
    <div>Contenu</div>
    <blockquote class="c-dim m-m-0">m-m-0<br>margin: 0</blockquote>
    <div>Contenu</div>
</article>
<article>
    <div>Contenu</div>
    <blockquote class="c-dim m-mt-0">m-mt-0<br>margin-top: 0</blockquote>
    <div>Contenu</div>
</article>
<article>
    <div>Contenu</div>
    <blockquote class="c-dim m-mr-0">m-mr-0<br>margin-right: 0</blockquote>
    <div>Contenu</div>
</article>
<article>
    <div>Contenu</div>
    <blockquote class="c-dim m-mb-0">m-mb-0<br>margin-bottom: 0</blockquote>
    <div>Contenu</div>
</article>
<article>
    <div>Contenu</div>
    <blockquote class="c-dim m-ml-0">m-ml-0<br>margin-left: 0</blockquote>
    <div>Contenu</div>
</article>
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-100);
        color: var(--ita-color-primary-800);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        min-height: 100vh;
    }
    article {
        background-color: var(--ita-color-primary-200)
    }
    article + article {
        margin-top: var(--ita-spacing-4)
    }
    .c-dim {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-neutral-100);
        padding: var(--ita-spacing-4);
    }
    #foo {
        /* indispensable pour illustrer le margin auto */
        max-width: 44ch;
    }
</style>
```
{:.playground title="Modifieurs pour le margin"}


