# utilities.scss

[Démo et documentation](https://ita-design-system.github.io/utilities.scss/)

Utilitaires génériques. 

## Typologie d'un utilitaire générique

```scss
// SCSS map
$briks-utilities: (
    // Propriété CSS de l'utilitaire
    // Syntaxe CSS exacte par ex. "background-image"
    PROPRIÉTÉ_CSS: (
        // Composant activé true ou false
        enabled: true,
        // Utilitaire responsive true ou false
        responsive: true,
        // Préfixe de l'utilitaire qui suit le préfixe u-
        // SCSS String
        prefix: 'PREFIXE-',
        // Liste des noms associés aux valeurs
        // SCSS map
        // Compatible avec
        // $briks-colors
        // $briks-font-families
        // $briks-font-sizes
        // $briks-borders
        // $briks-border-radius
        // $briks-shadows
        names-and-values: $briks-colors, // Exemple
        // ou noms => valeurs personnalisées
        // names-and-values: (
        //     NOM_1: VALEUR_1,
        //     NOM_2: VALEUR_2,
        //     NOM_3: VALEUR_3
        //     ...
        // ),
        // Optionnel: ajout de de noms associés / valeurs
        additional-names-and-values: (
            //     NOM_1: VALEUR_1,
            //     NOM_2: VALEUR_2,
            //     NOM_3: VALEUR_3
        ),
        // Optionnel: Prise en charge des pseudo-classes
        // Ajout d'une liste de pseudo-classes
        // Par ex. (hover, active, focus)
        pseudo-classes: (PSEUDO_CLASSE_1, PSEUDO_CLASSE_2, ...)
    )
)
```

## Configuration

Organisation et description du fichier de configuration [_sass/_utilities_generic.scss](_sass/_utilities_generic.scss).

```scss
/*
    UTILITIES
    v0.1.0
    Utilitaires génériques CSS ITADS
    https://github.com/ita-design-system/utilities.scss
*/
$briks-utilities: (
    background-color: (
        enabled: true,
        prefix: 'bc-',
        names-and-values: $briks-colors,
        // pseudo-classes: (hover),
        // additional-names-and-values: (
        //     'transparent': transparent
        // ),
        responsive: false
    ),
    border: (
        enabled: true,
        prefix: 'b-',
        names-and-values: $briks-borders,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    border-top: (
        enabled: true,
        prefix: 'bt-',
        names-and-values: $briks-borders,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    border-right: (
        enabled: true,
        prefix: 'br-',
        names-and-values: $briks-borders,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    border-bottom: (
        enabled: true,
        prefix: 'bb-',
        names-and-values: $briks-borders,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    border-left: (
        enabled: true,
        prefix: 'bl-',
        names-and-values: $briks-borders,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    border-radius: (
        enabled: true,
        prefix: 'brad-',
        names-and-values: $briks-border-radius,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    box-shadow: (
        enabled: true,
        prefix: 'bs-',
        names-and-values: $briks-shadows,
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    color: (
        enabled: true,
        prefix: 'c-',
        names-and-values: $briks-colors,
        // pseudo-classes: (hover),
        // additional-names-and-values: (
        //     'transparent': transparent
        // ),
        responsive: false
    ),
    cursor: (
        enabled: true,
        prefix: 'cur-',
        names-and-values: (
            pointer: pointer
        ),
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    display: (
        enabled: true,
        prefix: 'd-',
        names-and-values: (
            block: block,
            inline-block: inline-block,
            none: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    list-style: (
        enabled: true,
        prefix: 'ls-',
        names-and-values: (
            none: none
        ),
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    ),
    pointer-events: (
        enabled: true,
        prefix: 'pe-',
        names-and-values: (
            none: none,
            auto: auto
        ),
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: true
    ),
    visibility: (
        enabled: true,
        prefix: 'v-',
        names-and-values: (
            hidden: hidden
        ),
        // pseudo-classes: (hover),
        // additional-names-and-values: (),
        responsive: false
    )
);
``` 

## Extensions

Il est possible d'étendre les fonctionnalités des utilitaires en ajoutant simplement un point d'entrée avec une déclaration `$briks-utilities` à la typologie identique mais avec des propriétés par défaut et des modifieurs qui surchargent ou ajoutent des propriétés CSS.
