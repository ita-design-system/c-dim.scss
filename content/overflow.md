---
title: Overflow
description: Modifieurs c-dim dédiés à la gestion des dépassements
layout: libdoc/page-split
order: 130
---
```html
<div class="c-dim m-o-hidden">m-o-hidden <br>Pas de barre de défilement si dépassement du contenu. Ut et tempor tempor labore clita justo tempor. Sanctus voluptua clita et dolore labore elitr sit dolor sanctus, takimata no.</div>
<div class="c-dim m-o-auto">m-o-auto <br>Barres de défilement automatiques en cas de dépassement du contenu. Ut et tempor tempor labore clita justo tempor. Sanctus voluptua clita et dolore labore elitr sit dolor sanctus, takimata no.</div>
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
        /* indispensable pour illustrer le dépassement */
        white-space: nowrap;
    }
</style>
```
{:.playground title="Modifieurs pour l'overflow"}


