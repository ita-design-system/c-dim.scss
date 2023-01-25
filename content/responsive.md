---
title: Responsive
description: Fonctionnalités responsive du composant c-dim
layout: libdoc/page-split
order: 100
separator: true
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
<!-- Avec des classes responsives -->
<div class="c-dim">c-dim tout seul n'a pas d'effet</div>
<div class="c-dim m-w-4t m-w-8t--sm m-w-12t--xs">Je suis en 4/12 par défaut<br> en 8/12 sur écran sm<br> et pleine largeur sur écran xs</div>
<div class="c-dim" m-w-10t="xs,sm">Je suis en 10/12 sur les écrans xs et sm</div>
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
{:.playground title="Exemples responsives"}