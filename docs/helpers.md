# Helpers

Para classes de uso geral que sobrescrevem valores, coloque-as em um arquivo separado e no nome comece com um underline. Elas são normalmente marcadas com *!important*. Use-as com *muita* moderação.

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## Dando nome aos helpers
Utilize o underline como prefixo para o nome destas classes. Isso fará com que seja fácil diferenciá-las dos modificadores definidos no componente. Underlines também deixam o código esquisito o que tem um efeito colateral intencional: utilizar muitos helpers deve ser desencorajado.

  ```html
  <div class='order-graphs -slim _unmargin'>
  </div>
  ```

## Organizar Helpers
Coloque todos os helpers em um arquivo chamado `helpers`. Em vez de separá-los em vários arquivos, é preferível manter o número de helpers o menor possível.
