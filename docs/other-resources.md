# Outros Recursos

 * [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss#49) ("Inverted Triangle CSS") é um ótimo complemento à qualquer estrutura rscss.
 * [rsjs](http://ricostacruz.com/rsjs/) ("Reasonable Standard of JavaScript Structure") é um documento em construção para estruturar JavaScript em sites básicos.

Outras Soluções
---------------

### BEM
[BEM] é legal, mas pode irritar com sua sintaxe não convencional. RSCSS basicamente segue as convenções BEM, mas com uma sintaxe diferente.

```html
<!-- BEM -->
<form class='site-search site-search--full'>
  <input  class='site-search__field' type='text'>
  <button class='site-search__button'></button>
</form>
```

```html
<!-- rscss -->
<form class='site-search -full'>
  <input  class='field' type='text'>
  <button class='button'></button>
</form>
```

## Terminologias

Os mesmos conceitos existem de formas similares em outras ideologias de estruturação de CSS.

| RSCSS      | BEM         | SMACSS         |
| ---        | ---         | ---            |
| Componente | Bloco       | Módulo         |
| Elemento   | Elemento    | Sub-Componente |
| Layout     | ?           | Layout         |
| Variante   | Modificador | Sub-Módulo & Estado |

[BEM]: http://bem.info/
[Smacss]: https://smacss.com/
