# c-dim.scss

[Démo et documentation](https://ita-design-system.github.io/c-dim.scss/)

Composant CSS dédié aux dimensions et comportements liés à la taille des éléments.

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
            // WIDTH
            maxw-100: (
                // c-dim m-maxw-100
                max-width: 100%
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
            // HEIGHT
            maxh-100: (
                // c-dim m-maxh-100
                max-height: 100%
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
    // Nom du composant, obligatoirement flex
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
            // Exemple d'ajout d'une largeur fixe
            fixedw-1: ( // c-dim m-fw-1
                width: 100px,
                min-width: 100px,
                min-width: 100px
            )
        )
    )
);
```
