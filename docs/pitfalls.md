# Armadilhas

## Efeitos colaterais em elementos aninhados
Tenha cuidado com elementos aninhados dividindo o mesmo nome de elemento em seu container.

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Article title</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

Nesse caso, se `.article-link > .count` não tiver `>` seletor de descendente, o elemento `.vote-box .count` também será aplicado. Esta é uma das razões porque seletores de descendente são utilizados com preferência.