# Layouts

![](images/layouts.png)

## Evite propriedades de posicionamento
Componentes devem ser feitos de um modo que sejam reutilizáveis em vários contextos. Evite colocar essas propriedades nos componentes:

  * Posicionamento (`position`, `top`, `left`, `right`, `bottom`)
  * Floats (`float`, `clear`)
  * Margens (`margin`)
  * Dimensões (`width`, `height`) *

## Dimensões fixas

Exceto quanto aos elementos que possuem alturas e larguras fixas, como avatares e logos.

## Defina o posicionamento nos elementos pai

Se você precisa defini-los, tente definir em qualquer contexto em que eles estejam. Nesse exemplo abaixo, note que as larguras e floats são aplicadas
no componente *lista* e não no componente mesmo.

  ```css
  .article-list {
    & {
      @include clearfix;
    }

    > .article-card {
      width: 33.3%;
      float: left;
    }
  }

  .article-card {
    & { /* ... */ }
    > .image { /* ... */ }
    > .title { /* ... */ }
    > .category { /* ... */ }
  }
  ```

Como aplicar margens fora de um layout? Tente utilizar Helpers.
[Continue →](helpers.md)
<!-- {p:.pull-box} -->
