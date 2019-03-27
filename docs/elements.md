# Elementos

Elementos são coisas dentro do seu componente.

![](images/component-elements.png)

## Dando nome aos elementos
Cada componente pode ter elementos. Eles devem ter classes que são formados por apenas **uma palavra**.

```scss
.search-form {
  > .field { /* ... */ }
  > .action { /* ... */ }
}
```

## Seletores de elementos
Prefira utilizar o `>` seletor de elemento filho onde for possível. Isso previne que você sofra com componentes aninhados, e tenha uma perfomance melhor do que utilziar um seletor descendente

```scss
.article-card {
  .title     { /* ok */ }
  > .author  { /* ✓ melhor */ }
}
```

## Múltiplas palavras
Para as vezes em que for necessário duas ou mais palavras, concatene-as sem traços ou undescores.

```scss
.profile-box {
  > .firstname { /* ... */ }
  > .lastname { /* ... */ }
  > .avatar { /* ... */ }
}
```

## Evitando seletores de tag
Use nomes de classe sempre que possível. Seletores de tag são bons, mas eles podem conter uma menor penalidade na perfomance e podem não ser muito legíveis

```scss
.article-card {
  > h3    { /* ✗ evite */ }
  > .name { /* ✓ melhor */ }
}
```

Nem todos os elementos devem sempre parece iguais. Variantes podem ajudar
[Continue →](variants.md)
<!-- {p:.pull-box} -->
