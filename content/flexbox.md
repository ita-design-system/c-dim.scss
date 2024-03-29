---
title: Avec flexbox
description: Modifieurs c-dim dédiés aux items flexbox
layout: libdoc/page-split
order: 160
---
```html
<!-- Pour les besoins de la démo, ajout du CSS du composant générique c-dis -->
<link rel="stylesheet" href="https://ita-design-system.github.io/c-dis.scss/content/css/c-dis.generic.css">

<p>Les modifieurs de tantièmes (m-w-*t) du composants c-dim sont compatibles avec la propriété gap de flexbox et ce, quelle que soit sa valeur. Pour modifier le gap, remplacer la variable css <strong>--ita-gap</strong> par la valeur souhaitée sur le conteneur c-flex comme dans l'exemple qui suit.</p>

<!-- Contrôle du gap pour la démo -->
<input type="radio" name="gap" id="gap-0" checked>
<label for="gap-0">Pas de gap</label>
<input type="radio" name="gap" id="gap-1">
<label for="gap-1">Valeur de gap 1</label>
<input type="radio" name="gap" id="gap-2">
<label for="gap-2">Valeur de gap 2</label>

<div class="c-dis m-flex m-wrap">
    <div class="c-dim m-w-12t">Ces éléments sont des items flexbox</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-3t">3t</div>
    <div class="c-dim m-w-3t">3t</div>
    <div class="c-dim m-w-3t">3t</div>
    <div class="c-dim m-w-3t">3t</div>
    <div class="c-dim m-w-4t">4t</div>
    <div class="c-dim m-w-4t">4t</div>
    <div class="c-dim m-w-4t">4t</div>
    <div class="c-dim m-w-5t">5t</div>
    <div class="c-dim m-w-5t">5t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-6t">6t</div>
    <div class="c-dim m-w-6t">6t</div>
    <div class="c-dim m-w-7t">7t</div>
    <div class="c-dim m-w-5t">5t</div>
    <div class="c-dim m-w-8t">8t</div>
    <div class="c-dim m-w-4t">4t</div>
    <div class="c-dim m-w-9t">9t</div>
    <div class="c-dim m-w-3t">3t</div>
    <div class="c-dim m-w-10t">10t</div>
    <div class="c-dim m-w-2t">2t</div>
    <div class="c-dim m-w-11t">11t</div>
    <div class="c-dim m-w-1t">1t</div>
    <div class="c-dim m-w-12t">12t</div>
    <div class="c-dim m-w-6t">6t</div>
    <div class="c-dim">item</div>
    <div class="c-dim m-grow">m-grow<br>Étend l'élément <br>en fonction de la <br>place disponible.</div>
    <div class="c-dim m-w-12t">12t</div>
    <div class="c-dim m-grow">m-grow</div>
    <div class="c-dim m-w-3t">3t</div>
    <div class="c-dim m-w-2t">2t</div>
</div>

<p>Le modifieur m-order--1 (order: -1) permet de placer l'élément spécifié au début de l'axe principal.</p>
<div class="c-dis m-flex">
    <div>1</div>
    <div>2</div>
    <div class="c-dim m-order--1">3</div>
</div>
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
    .c-dis {
        margin-top: 1rem
    }
    .c-dim, .c-dis > span {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-neutral-100);
        border: 1px solid var(--ita-color-primary-200);
        padding: var(--ita-spacing-2);
    }
    #gap-1:checked ~ .c-dis {
        --ita-gap: var(--ita-spacing-2)
    }
    #gap-2:checked ~ .c-dis {
        --ita-gap: var(--ita-spacing-4)
    }
    label + input {
        margin-left: 1rem
    }
</style>
```
{:.playground title="Modifieurs compatibles c-flex"}


