# Variantes

Componentes podem ter variantes. Elementos poder ter variantes também.

![](images/component-modifiers.png)

<br>

## Dando nomes às variantes
Nomes de classe para variantes devem ser prefixadas com um traço (`-`).

  ```scss
  .like-button {
    &.-wide { /* ... */ }
    &.-short { /* ... */ }
    &.-disabled { /* ... */ }
  }
  ```

## Elementos variantes
Elementos podem ter variantes também.

  ```scss
  .shopping-card {
    > .title { /* ... */ }
    > .title.-small { /* ... */ }
  }
  ```

## Prefixo
Traços são os prefixos comumente utilizado para variantes.

  * Previne a ambiguidade entre elementos.
  * Uma classe css pode começar apenas com uma letra, `_` ou `-`.
  * Traços são mais fáceis de digitar do que underlines.
  * Meio que lembra a forma como digitamos comandos UNIX (`gcc -O2 -Wall -emit-last`).

Como você lida com elementos complexos? Aninhe-os 
[Continue →](nested-components.md)
<!-- {p:.pull-box} -->
