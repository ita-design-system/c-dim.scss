---
title: Avec c-flex
description: Modifieurs c-dim dédiés aux items flexbox du composant c-flex
layout: libdoc/page-split
order: 600
---
```html
<!-- Pour les besoins de la démo, ajout du CSS du composant générique c-flex -->
<link rel="stylesheet" href="https://ita-design-system.github.io/c-flex.scss/content/css/c-flex.generic.css">

<p>Les modifieurs de tantièmes (m-w-*t) du composants c-dim sont compatibles avec la propriété gap de flexbox et ce, quelle que soit sa valeur. Pour modifier le gap, remplacer la variable css <strong>--ita-gap</strong> par la valeur souhaitée sur le conteneur c-flex comme dans l'exemple qui suit.</p>

<!-- Contrôle du gap pour la démo -->
<input type="radio" name="gap" id="gap-0" checked>
<label for="gap-0">Pas de gap</label>
<input type="radio" name="gap" id="gap-1">
<label for="gap-1">Valeur de gap 1</label>
<input type="radio" name="gap" id="gap-2">
<label for="gap-2">Valeur de gap 2</label>

<div class="c-flex">
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
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-900);
        color: var(--ita-color-primary-200);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        padding-bottom: 50vh;
    }
    .c-flex {
        margin-top: 1rem
    }
    .c-dim, .c-flex > span {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-primary-900);
        border: var(--ita-border-6);
        padding: var(--ita-spacing-2);
    }
    #gap-1:checked ~ .c-flex {
        --ita-gap: var(--ita-spacing-2)
    }
    #gap-2:checked ~ .c-flex {
        --ita-gap: var(--ita-spacing-4)
    }
    label + input {
        margin-left: 1rem
    }
</style>
```
{:.playground title="Modifieurs compatibles c-flex"}


