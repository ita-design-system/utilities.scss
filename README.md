# utilities.scss

[Documentation](https://ita-design-system.github.io/utilities.scss/)

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
        names-and-values: 
        // names-and-values: (
        //     NOM_1: my-color(TOKEN_COULEUR),
        //     NOM_2: my-font-size(TOKEN_TAILLE_DE_TYPO),
        //     ...
        //     NOM_3: VALEUR_3
        //     ...
        // ),
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
    UTILITAIRES GÉNÉRIQUES
    v0.2.0
    Configuration des utilitaires génériques CSS ITADS
    https://github.com/ita-design-system/utilities.scss
*/
$briks-utilities: (
    background: (
        enabled: true,
        prefix: 'bg-',
        names-and-values: (
            none: none
        ),
        // pseudo-classes: (hover, active),
        responsive: true
    ),
    background-color: (
        enabled: true,
        prefix: 'bc-',
        names-and-values: (
            0: transparent
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border: (
        enabled: true,
        prefix: 'b-',
        names-and-values: (
            0: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-top: (
        enabled: true,
        prefix: 'bt-',
        names-and-values: (
            0: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-right: (
        enabled: true,
        prefix: 'br-',
        names-and-values: (
            0: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-bottom: (
        enabled: true,
        prefix: 'bb-',
        names-and-values: (
            0: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-left: (
        enabled: true,
        prefix: 'bl-',
        names-and-values: (
            0: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-radius: (
        enabled: true,
        prefix: 'brad-',
        names-and-values: (
            0: 0
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-top-left-radius: (
        enabled: true,
        prefix: 'bradtl-',
        names-and-values: (
            0: 0
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-top-right-radius: (
        enabled: true,
        prefix: 'bradtr-',
        names-and-values: (
            0: 0
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-bottom-right-radius: (
        enabled: true,
        prefix: 'bradbr-',
        names-and-values: (
            0: 0
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    border-bottom-left-radius: (
        enabled: true,
        prefix: 'bradbl-',
        names-and-values: (
            0: 0
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    box-shadow: (
        enabled: true,
        prefix: 'bs-',
        names-and-values: (
            0: none
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    color: (
        enabled: true,
        prefix: 'c-',
        names-and-values: (
            0: transparent
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    cursor: (
        enabled: true,
        prefix: 'cur-',
        names-and-values: (
            pointer: pointer
        ),
        // pseudo-classes: (hover),
        responsive: true
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
        responsive: true
    ),
    pointer-events: (
        enabled: true,
        prefix: 'pe-',
        names-and-values: (
            none: none,
            auto: auto
        ),
        // pseudo-classes: (hover),
        responsive: true
    ),
    visibility: (
        enabled: true,
        prefix: 'v-',
        names-and-values: (
            hidden: hidden
        ),
        // pseudo-classes: (hover),
        responsive: true
    )
);
``` 

## Extensions

Il est possible d'étendre les fonctionnalités des utilitaires en ajoutant simplement un point d'entrée avec une déclaration `$briks-utilities` à la typologie identique mais avec des propriétés par défaut et des modifieurs qui surchargent ou ajoutent des propriétés CSS.
