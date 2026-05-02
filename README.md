# velavokr.github.io

Source of [velavokr.github.io](https://velavokr.github.io). A small, static site for English translations of Russian engineering articles, plus the occasional original note.

## Layout

```
.
├── index.html                    # landing page (entry list)
├── translations/
│   └── <target-lang>/
│       └── <source-domain>/
│           └── <source-id>-<slug>.html
└── .nojekyll                     # serve files as-is, no Jekyll processing
```

For example, an English translation of a Habr article with id `924198` lives at
`translations/en/habr.ru/924198-yandex-lavka-search.html`.

## Adding a translation

1. Drop the self-contained translation HTML into the matching `translations/<lang>/<source-domain>/` folder.
2. Add an `<li class="entry">` entry to `index.html` (date, title link, subtitle, tags, original-source line).

Each translation page is fully self-contained (inline CSS, inline/SVG diagrams) — no shared assets, no build step.

## Local preview

Any static file server works. Examples:

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## License

Site code: MIT. Translations: see the per-page colophon — each one credits the original author and links back to the source.
