# WildFlux Experience GitHub page

## Install

Requires Node.js and npm.

```bash
npm install
```

## Run

```bash
npm run dev
```

Astro will print a local URL, usually `http://localhost:4321/`.

## Build

```bash
npm run build
```

The production site is generated in `dist/`.

```bash
npm run preview
```

Previews the production build locally.

## Project Structure

```text
public/
  cover/                  Cover and content images
  icons/                  UI icons
  logo/                   Site logo files
src/
  config/
    site.ts               Site identity, home content, and menu links
  components/
    HomeMenu.astro        Home page menu
    PageHeader.astro      Reusable page title/description/back link
    SiteHeader.astro      Header logo and site name
    TaggedGallery.astro   Filterable photo gallery with lightbox
  layouts/
    BaseLayout.astro      HTML shell, metadata, global styles, header/footer
    GeneralLayout.astro   Generic Markdown page layout
  pages/
    index.astro           Home page
    articles/example.md   Example Markdown content page
    subpages-template/    Basic starter page example
  styles/
    fonts.css             Font variables
    gallery.css           Gallery and lightbox styles
    general.css           Generic Markdown page styles
    global.css            Tokens, base rules, and generic page layout
    home.css              Home page and home menu styles
    site-chrome.css       Header and footer styles
    template-page.css     Basic example page placeholder styles
```

Astro routes are file based:

- `src/pages/index.astro` becomes `/`
- `src/pages/about.astro` becomes `/about`
- `src/pages/articles/example.md` becomes `/articles/example/`

## Main Configuration

Most site-specific values are in `src/config/site.ts`:

```ts
export const site = {
  name: 'WildFlux Experience',
  title: "WildFlux Experience",
  description: 'Site de WildFlux Experience',
  lang: 'fr',
  email: 'blackfish.creation@proton.me',
  logo: '/logo/blackfish_creation_base_2.png',
  home: {
    title: "WildFlux Experience",
    intro: 'Home intro text',
    cover: {
      src: '/cover/home_cover_1.jpg',
      alt: 'Home cover description',
      width: 4206,
      height: 2804,
    },
  },
};
```

Edit `menuItems` in the same file to change the home page links.

## Layouts

Use `BaseLayout` for normal Astro pages:

```astro
---
import PageHeader from '../components/PageHeader.astro';
import BaseLayout from '../layouts/BaseLayout.astro';
---

<BaseLayout title="Page title" description="Page description">
  <main class="page">
    <PageHeader title="Page title" description="Short intro." backHref="/" />
  </main>
</BaseLayout>
```

Use `GeneralLayout` for Markdown content pages:

```md
---
layout: ../../layouts/GeneralLayout.astro
title: Article Title
description: Article description.
backHref: /
backLabel: Retour
---

Write the page content in Markdown here.

![Image description](/cover/home_cover_2.jpg)

[Example link](https://astro.build/)
```

## Components

- `SiteHeader.astro`: displays the logo and site name from `site.ts`.
- `HomeMenu.astro`: displays links from `menuItems`.
- `PageHeader.astro`: reusable page header with title, description, and back link.
- `TaggedGallery.astro`: displays an album object with tags and a lightbox.

`TaggedGallery.astro` expects this data shape:

```js
const album = {
  title: 'Album title',
  description: 'Album description',
  folder: '/album/example/',
  photos: [
    {
      file: 'photo-1.jpg',
      caption: 'Photo caption',
      tags: ['portrait', 'black-white'],
    },
  ],
};
```

Images in `public/` are served from the site root, so
`public/cover/home_cover_1.jpg` is referenced as `/cover/home_cover_1.jpg`.

## Styles

Shared styles live in:

- `src/styles/fonts.css`
- `src/styles/global.css`
- `src/styles/site-chrome.css`
- `src/styles/home.css`
- `src/styles/gallery.css`
- `src/styles/general.css`
- `src/styles/template-page.css`

Main colors and layout width are CSS variables at the top of `global.css`:

```css
:root {
  --color-text: #111111;
  --color-background: #ffffff;
  --color-muted: #555555;
  --color-surface: #f5f5f5;
  --page-width: 1440px;
  --page-gutter: 90vw;
}
```

Change these variables to adapt the visual style without rewriting components.

## Add A New Page

1. Create a new `.astro` file in `src/pages/`.
2. Wrap it with `BaseLayout`.
3. Use `PageHeader` for consistent title/intro/back-link structure.
4. Add a link in `menuItems` if it should appear on the home page.

## Add A New Markdown Page

1. Copy `src/pages/articles/example.md`.
2. Rename it, for example `src/pages/articles/my-article.md`.
3. Edit the frontmatter title and description.
4. Keep `layout: ../../layouts/GeneralLayout.astro`.
5. Write the page content in Markdown.
6. Add images to `public/cover/` or another folder in `public/`.

## Template Reuse Checklist

When copying this project for a new website:

1. Update `package.json` name.
2. Replace assets in `public/`.
3. Edit `src/config/site.ts`.
4. Adjust CSS variables in `src/styles/global.css`.
5. Add or remove pages in `src/pages/`.
6. Keep reusable layout and component files generic.
