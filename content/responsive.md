---
title: Responsive
description: Fonctionnalités responsive du composant c-dim
layout: libdoc/page-split
order: 100
---
Si le paramètre `responsive: true` est activé, les modifieurs du composant c-dim sont adaptables à chaque design token de taille d'écran `$briks-screen-sizes` comme suit.

## Classes responsives

Un modifieur peut être appliqué sur des design tokens de tailles d'écrans via des classes CSS

```html
<!-- Avec des classes CSS -->
<HTMLTag class="c-dim m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN"></HTMLTag>
```

## Attributs responsives

En parallèle des classes CSS, la syntaxe par attribut permet d'appliquer la même fonctionnalité d'un modifieur sur plusieurs tailles d'écran en une seule fois.

```html
L'attribut responsive du modifieur
<HTMLTag class="c-dim" m-NOM_DU_MODIFIEUR="TOKEN_TAILLE_ECRAN_1, TOKEN_TAILLE_ECRAN_2, TOKEN_TAILLE_ECRAN_3"></HTMLTag>

a le même effet que les classes CSS
<HTMLTag class="c-dim m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_1 m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_2 m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_3"></HTMLTag>
```

```html
<link rel="stylesheet" href="https://ita-design-system.github.io/c-flex.scss/content/css/c-flex.generic.css">
<!-- Avec des classes responsives -->
<div class="c-dim">c-dim tout seul n'a pas d'effet</div>
<div class="c-dim m-w-1t">1t</div>
<div class="c-dim m-w-2t">2t</div>
<div class="c-dim m-w-3t">3t</div>
<div class="c-dim m-w-4t">4t</div>
<div class="c-dim m-w-5t">5t</div>
<div class="c-dim m-w-6t">6t</div>
<div class="c-dim m-w-7t">7t</div>
<div class="c-dim m-w-8t">8t</div>
<div class="c-dim m-w-9t">9t</div>
<div class="c-dim m-w-10t">10t</div>
<div class="c-dim m-w-11t">11t</div>
<div class="c-dim m-w-12t">12t</div>
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
    .c-dim {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-primary-900);
        border: var(--ita-border-6);
        padding: var(--ita-spacing-4);
    }
</style>
```
{:.playground title="Exemples responsives"}