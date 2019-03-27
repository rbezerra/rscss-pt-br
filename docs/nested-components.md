# Componentes aninhados

![](images/component-nesting.png)

```html
<div class='article-link'>
  <div class='vote-box'>
    ...
  </div>
  <h3 class='title'>...</h3>
  <p class='meta'>...</p>
</div>
```

Algumas vezes é necesário aninhar componentes. Aqui estão algumas sugestões para quando você fizer isso.

## Variantes
Um componente pode necessitar aparecer de um certo modo quando estiver aninhado em outro componente. Evite modificar o componente interno através do componente externo.

```scss
.article-header {
  > .vote-box > .up { /* ✗ evite isso */ }
}
```

  Como alternativa, prefirar adicionar uma variante para o componente interno e aplique-a através do elemento externo.

```html
<div class='article-header'>
  <div class='vote-box -highlight'>
    ...
  </div>
  ...
</div>
```

```scss
.vote-box {
  &.-highlight > .up { /* ... */ }
}
```

## Simplificando componentes aninhados
Algumas vezes a marcação pode ficar bagunçada quando utilizamos componentes aninhados:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='search-button -red -large'></button>
</div>
```

Você pode simplificar utilizando o mecanismo `@extend` do seu pré-processador de CSS

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='submit'></button>
</div>
```

```scss
.search-form {
  > .submit {
    @extend .search-button;
    @extend .search-button.-red;
    @extend .search-button.-large;
  }
}
```

E quando repetimos elementos como nas listas? Aprenda sobre Layouts.
[Continue →](layouts.md)
<!-- {p:.pull-box} -->
