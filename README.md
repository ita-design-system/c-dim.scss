# c-dim.scss

[Démo et documentation](https://ita-design-system.github.io/c-dim.scss/)

Composant CSS dédié aux dimensions et comportements liés à la taille des éléments.

## Scope

Liste des propriétés CSS utilisées par le composant

* align-self
* aspect-ratio
* box-sizing
* flex-grow
* height
* justify-self
* margin
* margin-block
* margin-block-end
* margin-block-start
* margin-bottom
* margin-inline
* margin-inline-end
* margin-inline-start
* margin-left
* margin-right
* margin-top
* max-block-size
* max-height
* max-inline-size
* max-width
* min-block-size
* min-height
* min-inline-size
* min-width
* object-fit
* object-position
* order
* overflow
* overflow-anchor
* overflow-block
* overflow-clip-margin
* overflow-inline
* overflow-wrap
* overflow-x
* overflow-y
* overscroll-behavior
* overscroll-behavior-block
* overscroll-behavior-inline
* overscroll-behavior-x
* overscroll-behavior-y
* padding
* padding-block
* padding-block-end
* padding-block-start
* padding-bottom
* padding-inline
* padding-inline-end
* padding-inline-start
* padding-left
* padding-right
* padding-top
* scroll-behavior
* scroll-margin
* scroll-margin-block
* scroll-margin-block-end
* scroll-margin-block-start
* scroll-margin-bottom
* scroll-margin-inline
* scroll-margin-inline-end
* scroll-margin-inline-start
* scroll-margin-left
* scroll-margin-right
* scroll-margin-top
* scroll-padding
* scroll-padding-block
* scroll-padding-block-end
* scroll-padding-block-start
* scroll-padding-bottom
* scroll-padding-inline
* scroll-padding-inline-end
* scroll-padding-inline-start
* scroll-padding-left
* scroll-padding-right
* scroll-padding-top
* scroll-snap-align
* scroll-snap-stop
* scroll-snap-type
* scroll-timeline
* scroll-timeline-axis
* scroll-timeline-name
* width

## Typologie d'un composant générique

```scss
// SCSS map
$briks-components-generic: ( 
    // SCSS map | Nom du composant
    NOM_DU_COMPOSANT: ( 
        // Boolean | Composant activé true ou false
        enabled: true, 
        // Boolean | Responsive activé true ou false
        responsive: true, 
        // SCSS map | Liste des propriétés du composant par défaut
        defaults: (), 
        // SCSS map | Liste des modifieurs
        modifiers: () 
    )
);
```

## Configuration

Organisation et description du fichier de configuration [_sass/_dim_generic.scss](_sass/_dim_generic.scss).

```scss
/*
    C-DIM
    v0.1.0
    Composant générique CSS ITADS
    https://github.com/ita-design-system/c-dim.scss
*/
// SCSS map
$briks-components-generic: ( 
    // Nom du composant
    dim: ( 
        // Composant activé true ou false
        enabled: true, 
        // Responsive activé true ou false
        responsive: true, 
        // Liste des propriétés c-dim par défaut
        defaults: (
            // Valeur de tantième par défaut #[FIX] https://github.com/ita-design-system/c-dim.scss/issues/1
            --ita-fraction: '-',
            // Nombre total de tantièmes (ici des douzièmes de 100%)
            --ita-total-amount-of-fractions: 12,
            // Calcul intermédiaire pour la largeur finale qui tient compte du gap
            --ita-item-default-width: calc(100% * var(--ita-fraction) / var(--ita-total-amount-of-fractions)),
            --ita-item-offset: calc(var(--ita-fraction) * var(--ita-gap, 0px) * ((var(--ita-total-amount-of-fractions) / var(--ita-fraction)) - 1) / var(--ita-total-amount-of-fractions)),
            // Calcul de la width permettant de s'adapter à n'importe quelle valeur de gap
            width: calc(var(--ita-item-default-width) - var(--ita-item-offset)),
            // Indispensable pour le calcul des tantièmes
            box-sizing: border-box
        ),
        // Rendu: 
        // .c-dim {
            // --ita-fraction: -,
            // --ita-total-amount-of-fractions: 12;
            // --ita-item-default-width: calc(100% * var(--ita-fraction) / var(--ita-total-amount-of-fractions));
            // --ita-item-offset: calc(var(--ita-fraction) * var(--ita-gap, 0px) * ((var(--ita-total-amount-of-fractions) / var(--ita-fraction)) - 1) / var(--ita-total-amount-of-fractions));
            // width: calc(var(--ita-item-default-width) - var(--ita-item-offset));
            // box-sizing: border-box;
        // }
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
            // BOX SIZING
            bsizing-content: (
                // c-dim m-bsizing-content
                box-sizing: content-box
            ),
            // MARGIN
            m-auto: (
                // c-dim m-m-auto
                margin: auto
            ),
            m-0: (
                // c-dim m-m-0
                margin: 0
            ),
            mt-0: (
                // c-dim m-mt-0
                margin-top: 0
            ),
            mr-0: (
                // c-dim m-mr-0
                margin-right: 0
            ),
            mb-0: (
                // c-dim m-mb-0
                margin-bottom: 0
            ),
            ml-0: (
                // c-dim m-ml-0
                margin-left: 0
            ),
            // PADDING
            p-0: (
                // c-dim m-p-0
                padding: 0
            ),
            pt-0: (
                // c-dim m-pt-0
                padding-top: 0
            ),
            pr-0: (
                // c-dim m-pr-0
                padding-right: 0
            ),
            pb-0: (
                // c-dim m-pb-0
                padding-bottom: 0
            ),
            pl-0: (
                // c-dim m-pl-0
                padding-left: 0
            ),
            // OVERFLOW
            o-auto: (
                // c-dim m-o-auto
                overflow: auto
            ),
            o-hidden: (
                // c-dim m-o-hidden
                overflow: hidden
            ),
            // FLEXBOX
            // Les modifieurs suivants sont compatibles uniquement avec les items flexbox
            // https://developer.mozilla.org/fr/docs/Web/CSS/flex-grow
            grow: (
                // c-dim m-grow
                flex-grow: 1
            ),
            order--1: (
                // c-dim m-order--1
                order: -1
            ),
            // WIDTH
            maxw-100: (
                // c-dim m-maxw-100
                max-width: 100%
            ),
            maxw-80vw: (
                // c-dim m-maxw-80vw
                max-width: 80vw
            ),
            maxw-100vw: (
                // c-dim m-maxw-100vw
                max-width: 100vw
            ),
            w-100vw: (
                // c-dim m-w-100vw
                width: 100vw
            ),
            w-100: (
                // c-dim m-w-100
                width: 100%
            ),
            w-auto: (
                // c-dim m-w-auto
                width: auto
            ),
            w-initial: (
                // c-dim m-w-initial
                width: initial
            ),
            // HEIGHT
            maxh-100: (
                // c-dim m-maxh-100
                max-height: 100%
            ),
            maxh-80vh: (
                // c-dim m-maxh-80vh
                max-height: 80vh
            ),
            maxh-100vh: (
                // c-dim m-maxh-100vh
                max-height: 100vh
            ),
            h-100vh: (
                // c-dim m-h-100vh
                height: 100vh
            ),
            h-100: (
                // c-dim m-h-100
                height: 100%
            ),
            h-auto: (
                // c-dim m-h-auto
                height: auto
            ),
            h-initial: (
                // c-dim m-h-initial
                height: initial
            ),
            // TANTIÈMES
            // Ici 12 tantièmes (douzièmes)
            // Il doit y avoir autant de modifieurs que de tantièmes sur defaults (--ita-total-amount-of-fractions)
            // Permet de s'adapter à n'importe quel gap
            w-1t: (
                // c-dim m-w-1t
                --ita-fraction: 1
            ),
            w-2t: (
                // c-dim m-w-2t
                --ita-fraction: 2
            ),
            w-3t: (
                // c-dim m-w-3t
                --ita-fraction: 3
            ),
            w-4t: (
                // c-dim m-w-4t
                --ita-fraction: 4
            ),
            w-5t: (
                // c-dim m-w-5t
                --ita-fraction: 5
            ),
            w-6t: (
                // c-dim m-w-6t
                --ita-fraction: 6
            ),
            w-7t: (
                // c-dim m-w-7t
                --ita-fraction: 7
            ),
            w-8t: (
                // c-dim m-w-8t
                --ita-fraction: 8
            ),
            w-9t: (
                // c-dim m-w-9t
                --ita-fraction: 9
            ),
            w-10t: (
                // c-dim m-w-10t
                --ita-fraction: 10
            ),
            w-11t: (
                // c-dim m-w-11t
                --ita-fraction: 11
            ),
            w-12t: (
                // c-dim m-w-12t
                --ita-fraction: 12
            ),
            // SCROLL BEHAVIOR
            scrollb-smooth: (
                scroll-behavior: smooth
            ),
            // SCROLL SNAP ALIGN
            scrollsa-start: (
                scroll-snap-align: start
            ),
            scrollsa-center: (
                scroll-snap-align: center
            ),
            // SCROLL SNAP TYPE
            scrollst-x-mandatory: (
                scroll-snap-type: x mandatory
            ),
            scrollst-y-mandatory: (
                scroll-snap-type: y mandatory
            )
        )
    )
);
``` 

## Extensions

Il est possible d'étendre les fonctionnalités du composant en ajoutant simplement un point d'entrée avec une déclaration `$briks-components-generic` à la typologie identique mais avec des propriétés par défaut et des modifieurs qui surchargent ou ajoutent des propriétés CSS.

Par exemple :

```scss
/*
    C-DIM EXTENSION
    Extension du composant générique c-dim
    https://github.com/ita-design-system/c-dim.scss
    Ce fichier doit servir à étendre ou surcharger les fonctionnalités
    du composant c-dim selon les besoins du projet
*/
$briks-components-generic: (
    // Nom du composant, obligatoirement dim
    dim: ( 
        // Extension activée true ou false
        enabled: true, 
        // Responsive activée true ou false pour l'extension
        responsive: true, 
        // Valeurs par défaut de l'extension
        defaults: (),
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
            // Exemple d'ajout d'une largeur minimum
            minw-1: ( // c-dim m-minw-1
                min-width: 100px
            ),
            minw-2: ( // c-dim m-minw-2
                min-width: 200px
            )
        )
    )
);
```
