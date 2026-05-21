# Language Guide

The MASAIC website supports English and Japanese.

## How Language Switching Works

The language switcher uses `i18n.js` and stores the selected language in `localStorage`.

Two patterns are used:

1. `data-i18n` for short text such as navigation labels.
2. `data-lang-content` for larger blocks of translated content.

## Pattern 1: `data-i18n`

Use `data-i18n` for simple reusable text.

```html
<a href="index.html" data-i18n="nav.home">Home</a>
```

Add the matching key in `i18n.js`:

```javascript
const translations = {
    en: {
        'nav.home': 'Home'
    },
    ja: {
        'nav.home': 'ホーム'
    }
};
```

## Pattern 2: `data-lang-content`

Use this for longer page sections.

```html
<div data-lang-content="en">
    <h2>About MASAIC</h2>
    <p>English content goes here.</p>
</div>

<div data-lang-content="ja" style="display: none;">
    <h2>MASAICについて</h2>
    <p>Japanese content goes here.</p>
</div>
```

## Required Scripts

Every page that uses language switching should include:

```html
<script src="i18n.js"></script>
<script src="script.js"></script>
```

## Language Switcher Markup

```html
<div class="language-switcher">
    <button class="lang-btn active" data-lang="en">EN</button>
    <button class="lang-btn" data-lang="ja">日本語</button>
</div>
```

## Testing

1. Start a local server.
2. Open the page in a browser.
3. Click `EN` and `日本語`.
4. Refresh the page and confirm the selected language is preserved.

```bash
python -m http.server 8000
```

## Notes

- Keep English and Japanese content structurally aligned.
- Use `data-i18n` for repeated short labels.
- Use `data-lang-content` for full sections, cards, and long descriptions.
- Test mobile layout after adding translated text, because Japanese strings can change line breaks.
