#### [Carta](https://github.com/BearToCode/carta) Plugin: Newline Break

This plugin adds support for hard breaks without needing spaces or escapes (turns carriage returns into `<br>`s).

Markdown already has two ways to include hard breaks, namely trailing spaces and
escapes (note that `␠` represents a normal space):

```markdown
lorem␠␠
ipsum

lorem\
ipsum
```

Both will turn into `<br>`s.
If you control who authors content or can document how markdown works,
it's recommended to use escapes instead.

#### Install

```bash
  npm install --save @warren-bank/cartamd-plugin-newline-break
```

#### [Usage](https://beartocode.github.io/carta/api/extension) with [Svelte](https://svelte.dev/)

```html
  <script lang="ts">
    import {Carta, MarkdownEditor} from 'carta-md'
    import {newline_break} from '@warren-bank/cartamd-plugin-newline-break'

    import 'carta-md/default.css'

    const carta = new Carta({
      extensions: [
        newline_break()
      ]
    })

    let value
  </script>

  <MarkdownEditor bind:value {carta} />
```

#### Legal:

* copyright: [Warren Bank](https://github.com/warren-bank)
* license: [GPL-2.0](https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt)
