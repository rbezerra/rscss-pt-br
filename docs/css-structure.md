# Estrutura do CSS

## Um componente por arquivo
Cada componente deve ter seu próprio arquivo.

  ```scss
  /* css/components/search-form.scss */
  .search-form {
    > .button { /* ... */ }
    > .field { /* ... */ }
    > .label { /* ... */ }

    // variants
    &.-small { /* ... */ }
    &.-wide { /* ... */ }
  }
  ```

## Use glob matching
Isso facilitar incluir tudo em sass-rails e stylus:

  ```scss
  @import 'components/*';
  ```

## Evite muitos níveis de aninhamento
Não utilize mais do que 1 nível de aninhamento. é fácil se perder em muitos níveis.

  ```scss
  /* ✗ Evite: 3 níveis de aninhamento */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ Melhor: 2 níveis */
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
