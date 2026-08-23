# Easy &amp; Delicious

A personal index of easy, delicious recipes — direct links, time-saving hacks with
modifications, and original recipes.

**Live site:** https://veronicamontgomerya.github.io/easy-delicious-recipes

## What's here

- `index.html` — the entire site. One self-contained page: no build step, no
  dependencies, no framework. Fonts come from Google Fonts; everything else is inline.

## Editing

Open `index.html` in any editor. Each recipe is one `<article class="recipe">` block with
two data attributes that drive the filter bar:

```html
<article class="recipe" data-course="vegetarian" data-hack="true">
```

- `data-course` — `vegetarian`, `poultry`, or `dessert`
- `data-hack` — `true` if the recipe has a time-saving hack, otherwise `false`

To add a recipe, copy an existing `<article>` block into the right `<section>`, change the
content, and update the count in the masthead tally.

The left rail label uses `data-kind` on the `.kind` span: `shortcut`, `original`, or
`as-written`.

## Publishing changes

Committing to `main` republishes the site automatically:

```sh
git add index.html
git commit -m "Add a recipe"
git push
```

GitHub Pages redeploys within a minute or so.
