# 🚀 DIETAPLAZA BLOG PROJEKT - Teljes Dokumentáció

> **Projekt:** Hugo-alapú diétás/táplálkozási blog  
> **Design:** Sage-inspired (minimal, modern)  
> **CSS Framework:** Spruce CSS  
> **Hosting:** GitHub Pages (ingyenes)  
> **Időkeret:** 4 hét (1 hónap)  
> **Létrehozva:** 2026. május 14.

---

## 📋 PROJEKT ÁTTEKINTÉS

### Célok
1. **Több tartalom gyártás** AEO/SEO optimalizálásra
2. **Modern blog platform** (jelenlegi Shoprenter blog nehézkes)
3. **Organikus forgalom növelése** (Google + AI válaszgépek)
4. **Shoprenter termékekre terelés** CTA-kkal

### Domain Stratégia
- **Blog:** `dietaplaza.hu` (főoldal - új)
- **Webshop:** `shop.dietaplaza.hu` (subdomain - jelenlegi Shoprenter áthelyezve)

### Költségek
| Tétel | Összeg |
|-------|---------|
| Hugo | 0 Ft |
| Spruce CSS | 0 Ft (open source) |
| GitHub Pages hosting | 0 Ft |
| GitHub Actions CI/CD | 0 Ft |
| SSL certificate | 0 Ft (Let's Encrypt) |
| Domain (.hu) | ~3000 Ft/év |
| **Összesen** | **~3000 Ft/év** |

---

## 🛠️ TECHNIKAI STACK

```
Hugo Framework (v0.134+)
├── Extended Version (Sass support)
├── Build: ~500ms (500 cikk)
└── Server: hugo server -D

Spruce CSS Framework
├── Sass-based (SCSS)
├── Version: Latest
├── Size: ~1400 lines
└── Modern CSS (custom properties, clamp)

GitHub Ecosystem
├── Repository: dietaplaza-blog (public)
├── Hosting: GitHub Pages
├── CI/CD: GitHub Actions
└── Deploy: Auto on push to main

Content Workflow
├── Write: Claude chat + Markdown
├── Images: Claude-generated + optimized
├── Deploy: Git push → auto build
└── Time: ~5-10 min/article
```

---

## 📅 4 HETES ÜTEMTERV

### 🗓️ HÉT 1: TECHNIKAI ALAPOK

#### Hétfő-Kedd (2 nap): Projekt Setup
```bash
□ Hugo projekt létrehozás (hugo new site dietaplaza-blog)
□ GitHub repository: dietaplaza-blog (public)
□ Git init + első commit
□ Spruce CSS letöltés és integráció
□ Hugo config.toml alapbeállítások
□ .gitignore konfiguráció
□ Lokális dev környezet tesztelés
```

**Deliverable:** Működő Hugo site lokálisan + GitHub-on

#### Szerda-Csütörtök (2 nap): Spruce CSS Integráció
```bash
□ Spruce CSS files → assets/scss/spruce/
□ Main SCSS file létrehozás (assets/scss/main.scss)
□ Config fájl (_config.scss - színek, betűk)
□ Hugo Sass pipeline beállítás
□ Spruce compile teszt
□ CSS változók dokumentálás
```

**Deliverable:** Működő Spruce CSS build pipeline

#### Péntek (1 nap): GitHub Actions + Deploy
```bash
□ .github/workflows/hugo.yml létrehozás
□ GitHub Pages aktiválás
□ Custom domain beállítás előkészítése
□ SSL certificate (auto)
□ Első deploy teszt
```

**Deliverable:** Auto-deploy működik, üres site élőben

---

### 🗓️ HÉT 2: DESIGN KIDOLGOZÁS (Sage-inspired)

#### Hétfő-Kedd (2 nap): Layout Struktúra
```bash
□ layouts/_default/baseof.html (master template)
□ layouts/partials/head.html
□ layouts/partials/header.html
□ layouts/partials/footer.html
□ layouts/partials/nav.html
□ Grid system (Sage-style)
```

#### Szerda-Csütörtök (2 nap): Homepage & Blog Grid
```bash
□ layouts/index.html (homepage)
□ Hero section
□ Blog card component (partial)
□ Grid layout (masonry-style)
□ Featured posts logic
□ Responsive design
```

#### Péntek (1 nap): Single Post Layout
```bash
□ layouts/_default/single.html
□ Hero image system
□ Article typography
□ Table of contents (TOC)
□ Reading time calculation
```

**Deliverable:** Teljes design system működik

---

### 🗓️ HÉT 3: SEO/AEO + SHOPRENTER

#### Hétfő-Kedd (2 nap): SEO Optimalizálás
```bash
□ layouts/partials/seo-meta.html
  - Open Graph tags
  - Twitter Cards
  - Canonical URLs
□ Schema.org structured data
  - Article schema
  - BreadcrumbList
  - WebSite schema
□ Sitemap.xml (auto)
□ Robots.txt
□ RSS feed config
```

#### Szerda-Csütörtök (2 nap): Shoprenter Integráció
```bash
□ layouts/shortcodes/product.html
□ Product CTA component design
□ UTM paraméter rendszer
□ Product data structure
□ Tracking setup (Google Analytics)
```

#### Péntek (1 nap): Performance
```bash
□ Image optimization pipeline
□ CSS minification
□ Lazy loading
□ PageSpeed Insights audit (target: 90+)
```

**Deliverable:** SEO-ready, gyors, Shoprenter-integrált

---

### 🗓️ HÉT 4: TARTALOM + LAUNCH

#### Hétfő-Kedd (2 nap): Tartalom Migráció
```bash
□ Shoprenter blog export
□ Markdown konverzió
□ Képek letöltés + optimalizálás
□ Frontmatter meta adatok
□ Internal linking
```

#### Szerda-Csütörtök (2 nap): Új Tartalom + Teszt
```bash
□ 3-5 új AEO-optimalizált cikk
□ SEO audit (Google Search Console)
□ Mobile teszt
□ Cross-browser teszt
□ Performance check
□ Link tesztelés
```

#### Péntek (1 nap): 🚀 LAUNCH!
```bash
□ DNS beállítások
  - dietaplaza.hu → GitHub Pages
  - shop.dietaplaza.hu → Shoprenter
□ 301 redirectek (régi → új)
□ Google Search Console átállítás
□ Google Analytics aktiválás
□ Final smoke test
□ GO LIVE! 🎉
```

**Deliverable:** Éles blog dietaplaza.hu-n

---

## 🎨 DESIGN RENDSZER (Sage-inspired)

### Színpaletta
```scss
// _config.scss
$colors: (
  'primary': #000000,      // Fekete - text
  'bg': #FFFFFF,           // Fehér - háttér
  'accent': #16A34A,       // Zöld - CTA (egészség/diéta)
  'gray-100': #F8F9FA,     // Light gray
  'gray-200': #E9ECEF,     // Border light
  'gray-300': #DEE2E6,     // Border
  'gray-600': #6C757D,     // Meta text
  'gray-800': #343A40,     // Dark text
);
```

### Tipográfia
```scss
// Font stack
$font-family-base: -apple-system, BlinkMacSystemFont, 'Segoe UI', 
                   'Helvetica Neue', Arial, sans-serif;
$font-family-heading: 'Poppins', $font-family-base;

// Font sizes (Spruce conventions)
$font-sizes: (
  'xs': 0.75rem,      // 12px
  'sm': 0.875rem,     // 14px
  'base': 1rem,       // 16px
  'lg': 1.125rem,     // 18px
  'xl': 1.25rem,      // 20px
  '2xl': 1.5rem,      // 24px
  '3xl': 1.875rem,    // 30px
  '4xl': 2.25rem,     // 36px
  '5xl': 3rem,        // 48px
);

// Line heights
$line-height-tight: 1.25;
$line-height-normal: 1.5;
$line-height-relaxed: 1.7;
```

### Spacing (Spruce spacer() function)
```scss
// 8px base grid
$spacers: (
  '0': 0,
  '1': 0.5rem,    // 8px
  '2': 1rem,      // 16px
  '3': 1.5rem,    // 24px
  '4': 2rem,      // 32px
  '5': 2.5rem,    // 40px
  '6': 3rem,      // 48px
  '8': 4rem,      // 64px
  '10': 5rem,     // 80px
  '12': 6rem,     // 96px
);
```

### Layout
```scss
// Container
.container {
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  padding-left: spacer(4);
  padding-right: spacer(4);
}

// Blog Grid (Sage-style)
.blog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: spacer(6);
  
  @include breakpoint('md') {
    gap: spacer(8);
  }
}

// Post Card
.post-card {
  border-radius: 12px;
  overflow: hidden;
  background: color('bg');
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  
  &:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
  }
}
```

### Breakpoints (Spruce)
```scss
$breakpoints: (
  'xs': 32em,    // 512px
  'sm': 48em,    // 768px
  'md': 64em,    // 1024px
  'lg': 80em,    // 1280px
  'xl': 90em,    // 1440px
  '2xl': 110em,  // 1760px
);

// Usage
@include breakpoint('md') {
  // styles for 1024px+
}
```

---

## 📁 PROJEKT STRUKTÚRA

```
dietaplaza-blog/
│
├── .github/
│   └── workflows/
│       └── hugo.yml              # GitHub Actions workflow
│
├── archetypes/
│   └── post.md                   # Új cikk template (frontmatter)
│
├── assets/
│   └── scss/
│       ├── main.scss             # Main import file
│       ├── _config.scss          # Spruce config override
│       ├── _custom.scss          # Custom styles (Sage design)
│       └── spruce/               # Spruce CSS files
│           ├── _index.scss
│           ├── _functions.scss
│           ├── _mixins.scss
│           └── ...
│
├── content/
│   ├── posts/                    # Blog cikkek
│   │   ├── _index.md
│   │   ├── ketogen-dieta-2025.md
│   │   ├── mediterran-dieta-7-nap.md
│   │   └── ...
│   ├── pages/                    # Statikus oldalak
│   │   ├── about.md
│   │   ├── contact.md
│   │   └── privacy.md
│   └── _index.md                 # Homepage content
│
├── layouts/
│   ├── _default/
│   │   ├── baseof.html           # Master template
│   │   ├── single.html           # Post layout
│   │   ├── list.html             # Archive/category layout
│   │   └── terms.html            # Taxonomy layout
│   │
│   ├── partials/
│   │   ├── head.html             # <head> section
│   │   ├── header.html           # Site header
│   │   ├── footer.html           # Site footer
│   │   ├── nav.html              # Navigation
│   │   ├── seo-meta.html         # SEO meta tags
│   │   ├── schema.html           # Schema.org JSON-LD
│   │   ├── post-card.html        # Blog card component
│   │   ├── shoprenter-cta.html   # Product CTA
│   │   └── newsletter.html       # Newsletter signup
│   │
│   ├── shortcodes/
│   │   ├── product.html          # Product embed
│   │   ├── youtube.html          # YouTube embed
│   │   └── note.html             # Info box
│   │
│   └── index.html                # Homepage template
│
├── static/
│   ├── images/                   # Képek
│   │   ├── posts/
│   │   ├── products/
│   │   └── site/
│   ├── favicon.ico
│   └── robots.txt
│
├── config.toml                   # Hugo configuration
├── .gitignore
└── README.md
```

---

## ⚙️ HUGO KONFIGURÁCIÓ

### config.toml
```toml
baseURL = "https://dietaplaza.hu/"
languageCode = "hu-HU"
title = "Dietaplaza Blog"
theme = ""  # Custom theme in layouts/

# Build settings
buildDrafts = false
buildFuture = false
canonifyURLs = true

# Pagination
paginate = 12
paginatePath = "oldal"

# Taxonomies
[taxonomies]
  category = "categories"
  tag = "tags"

# Params
[params]
  description = "Diéta, táplálkozás, egészséges életmód - szakértői tanácsok és receptek"
  author = "Dietaplaza"
  images = ["/images/site/og-default.jpg"]
  
  # Social
  facebook = "https://facebook.com/dietaplaza"
  instagram = "https://instagram.com/dietaplaza"
  
  # Shoprenter
  shopURL = "https://shop.dietaplaza.hu"
  shopUTMSource = "blog"

# Menu
[[menu.main]]
  name = "Diéták"
  url = "/categories/dietak/"
  weight = 1

[[menu.main]]
  name = "Receptek"
  url = "/categories/receptek/"
  weight = 2

[[menu.main]]
  name = "Fogyókúra"
  url = "/categories/fogyokura/"
  weight = 3

[[menu.main]]
  name = "Táplálékkiegészítők"
  url = "/categories/taplalekkiegeszitok/"
  weight = 4

[[menu.main]]
  name = "Rólunk"
  url = "/about/"
  weight = 5

# Markup
[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true  # Allow HTML in markdown
  
  [markup.highlight]
    style = "monokai"
    lineNos = false
    
  [markup.tableOfContents]
    endLevel = 3
    ordered = false
    startLevel = 2

# Output formats
[outputs]
  home = ["HTML", "RSS", "JSON"]
  section = ["HTML", "RSS"]
```

---

## 📝 FRONTMATTER SABLON

### archetypes/post.md
```yaml
---
title: "{{ replace .Name "-" " " | title }}"
description: ""
date: {{ .Date }}
lastmod: {{ .Date }}
draft: true
author: "Dietaplaza"

# Kategóriák & Tag-ek
categories: []
tags: []

# Képek
image: ""
imageAlt: ""
featured: false

# SEO
seo:
  title: ""
  description: ""
  keywords: []
  canonical: ""
  robots: "index, follow"

# Schema.org
schema:
  type: "Article"
  datePublished: "{{ dateFormat "2006-01-02" .Date }}"
  dateModified: "{{ dateFormat "2006-01-02" .Date }}"
  wordCount: 0
  author: "Dietaplaza"
  publisher: "Dietaplaza Blog"

# Shoprenter termékek (opcionális)
shoprenter_products: []
#  - name: ""
#    url: ""
#    price: ""
#    image: ""

# Social Share
og_image: ""
twitter_card: "summary_large_image"
---

Cikk bevezető...

<!--more-->

## Első fejezet

Tartalom...
```

---

## 📝 PÉLDA CIKK - Teljes Frontmatter

### content/posts/ketogen-dieta-kezdoknek-2025.md
```yaml
---
title: "Ketogén Diéta Kezdőknek 2025: Teljes Útmutató"
description: "Minden, amit a keto diétáról tudnod kell - étrend összeállítás, étkezési terv, bevásárlólista és szakértői tippek fogyáshoz."
date: 2025-02-08T10:00:00+01:00
lastmod: 2025-02-08T10:00:00+01:00
draft: false
author: "Dietaplaza"

# Kategóriák & Tag-ek
categories: ["Diéták", "Fogyókúra"]
tags: ["ketogén diéta", "keto", "alacsony szénhidrát", "zsírégetés", "fogyás"]

# Képek
image: "/images/posts/keto-dieta-2025-hero.webp"
imageAlt: "Ketogén diétás ételek - avokádó, tojás, sajt, bacon"
featured: true

# SEO
seo:
  title: "Ketogén Diéta Útmutató 2025: Fogyás Szénhidrát Nélkül | Dietaplaza"
  description: "Részletes útmutató a keto diéta kezdéséhez 2025-ben. 7 napos étrend, receptek, bevásárlólista és gyakori hibák. Tudományosan megalapozott tanácsok."
  keywords: 
    - "ketogén diéta"
    - "keto étrend"
    - "alacsony szénhidrát diéta"
    - "fogyókúra 2025"
    - "zsírégetés"
    - "keto kezdőknek"
  canonical: "https://dietaplaza.hu/posts/ketogen-dieta-kezdoknek-2025"
  robots: "index, follow"

# Schema.org
schema:
  type: "Article"
  datePublished: "2025-02-08"
  dateModified: "2025-02-08"
  wordCount: 2500
  author: "Dietaplaza"
  publisher: "Dietaplaza Blog"

# Shoprenter termékek
shoprenter_products:
  - name: "Bio MCT Olaj 500ml"
    url: "https://shop.dietaplaza.hu/bio-mct-olaj"
    price: "8990"
    image: "/images/products/mct-olaj.webp"
  - name: "Keto Protein Por - Vanília"
    url: "https://shop.dietaplaza.hu/keto-protein-vanilia"
    price: "12990"
    image: "/images/products/keto-protein.webp"
  - name: "Eritrit Természetes Édesítőszer 1kg"
    url: "https://shop.dietaplaza.hu/eritrit-edesito"
    price: "3490"
    image: "/images/products/eritrit.webp"

# Social Share
og_image: "/images/posts/keto-dieta-2025-og.jpg"
twitter_card: "summary_large_image"
---

A **ketogén diéta** (keto) az utóbbi évek egyik legnépszerűbb fogyókúrás módszere. De valóban működik? Ebben az átfogó útmutatóban megismerheted a keto diéta alapjait, a tudományos hátteret, és konkrét lépéseket kapsz a kezdéshez.

<!--more-->

## Mi a ketogén diéta?

A ketogén diéta egy nagyon alacsony szénhidrát-, magas zsír- és közepes fehérjetartalmú étrend...

[... további tartalom ...]

## 7 napos étkezési terv kezdőknek

### 1. nap
**Reggeli:** Tojásrántotta avokádóval és baconnel
**Ebéd:** Csirkemell saláta olívaolajjal
**Vacsora:** Lazac zöldségekkel sütve

[... további napok ...]

## Ajánlott keto termékek

A keto diéta sikeréhez elengedhetetlenek bizonyos táplálékkiegészítők:

{{< product 
    name="Bio MCT Olaj 500ml"
    url="https://shop.dietaplaza.hu/bio-mct-olaj"
    price="8990"
    image="/images/products/mct-olaj.webp"
    description="Gyors energia keto diétához"
>}}

[... további termékek ...]

## Gyakran Ismételt Kérdések (GYIK)

**Mennyit lehet fogyni keto diétával?**
Az első héten 2-4 kg fogyás normális (főleg vízvesztés), utána heti 0.5-1 kg reális cél...

[... további kérdések ...]
```

---

## 🔧 GITHUB ACTIONS WORKFLOW

### .github/workflows/hugo.yml
```yaml
name: Deploy Hugo site to GitHub Pages

on:
  push:
    branches:
      - main
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

defaults:
  run:
    shell: bash

jobs:
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.134.0
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0
      
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v4
      
      - name: Build with Hugo
        env:
          HUGO_CACHEDIR: ${{ runner.temp }}/hugo_cache
          HUGO_ENVIRONMENT: production
        run: |
          hugo \
            --gc \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

---

## 🎨 SPRUCE CSS INTEGRÁCIÓ

### assets/scss/main.scss
```scss
// Spruce CSS Framework import
@use 'spruce' as *;

// Config override
@use 'config' with (
  // Colors
  $colors: (
    'primary': #000000,
    'bg': #FFFFFF,
    'accent': #16A34A,
    'gray-100': #F8F9FA,
    'gray-300': #DEE2E6,
    'gray-600': #6C757D,
  ),
  
  // Fonts
  $font-family-base: (-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif),
  $font-family-heading: ('Poppins', -apple-system, BlinkMacSystemFont, sans-serif),
);

// Custom styles (Sage design)
@use 'custom';
```

### assets/scss/_config.scss
```scss
// Spruce CSS configuration overrides
// Import this file in main.scss

// Colors
$colors: (
  'primary': #000000,
  'bg': #FFFFFF,
  'accent': #16A34A,
  'gray-100': #F8F9FA,
  'gray-200': #E9ECEF,
  'gray-300': #DEE2E6,
  'gray-600': #6C757D,
  'gray-800': #343A40,
) !default;

// Typography
$font-family-base: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif !default;
$font-family-heading: 'Poppins', $font-family-base !default;

// Spacing (8px grid)
$spacers: (
  '0': 0,
  '1': 0.5rem,
  '2': 1rem,
  '3': 1.5rem,
  '4': 2rem,
  '5': 2.5rem,
  '6': 3rem,
  '8': 4rem,
  '10': 5rem,
  '12': 6rem,
) !default;

// Breakpoints
$breakpoints: (
  'xs': 32em,
  'sm': 48em,
  'md': 64em,
  'lg': 80em,
  'xl': 90em,
  '2xl': 110em,
) !default;
```

### assets/scss/_custom.scss
```scss
// Custom styles for Dietaplaza (Sage-inspired design)

// Container
.container {
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  padding-left: spacer(4);
  padding-right: spacer(4);
}

// Blog Grid (Sage-style)
.blog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: spacer(6);
  
  @include breakpoint('md') {
    gap: spacer(8);
  }
}

// Post Card
.post-card {
  border-radius: 12px;
  overflow: hidden;
  background: color('bg');
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  
  &:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
  }
  
  &__image {
    width: 100%;
    height: 240px;
    object-fit: cover;
  }
  
  &__content {
    padding: spacer(4);
  }
  
  &__meta {
    display: flex;
    gap: spacer(2);
    margin-bottom: spacer(2);
    font-size: font-size('sm');
    color: color('gray-600');
  }
  
  &__title {
    margin: 0 0 spacer(2);
    font-size: font-size('xl');
    line-height: $line-height-tight;
    
    a {
      color: color('primary');
      text-decoration: none;
      
      &:hover {
        color: color('accent');
      }
    }
  }
  
  &__excerpt {
    margin: 0;
    font-size: font-size('base');
    line-height: $line-height-normal;
    color: color('gray-600');
  }
}

// Hero Section
.hero {
  padding: spacer(12) 0;
  text-align: center;
  background: linear-gradient(135deg, color('gray-100') 0%, color('bg') 100%);
  
  &__title {
    font-size: font-size('5xl');
    margin-bottom: spacer(4);
  }
  
  &__description {
    font-size: font-size('xl');
    color: color('gray-600');
    max-width: 600px;
    margin: 0 auto spacer(6);
  }
}

// Newsletter
.newsletter {
  padding: spacer(8) 0;
  background: color('gray-100');
  text-align: center;
  
  &__form {
    max-width: 500px;
    margin: spacer(4) auto 0;
    display: flex;
    gap: spacer(2);
  }
  
  &__input {
    flex: 1;
    padding: spacer(3);
    border: 1px solid color('gray-300');
    border-radius: 8px;
  }
  
  &__button {
    padding: spacer(3) spacer(5);
    background: color('accent');
    color: white;
    border: none;
    border-radius: 8px;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.2s;
    
    &:hover {
      background: darken(color('accent'), 10%);
    }
  }
}

// Shoprenter Product CTA
.product-cta {
  display: flex;
  align-items: center;
  gap: spacer(4);
  padding: spacer(4);
  margin: spacer(6) 0;
  background: color('gray-100');
  border-radius: 12px;
  border-left: 4px solid color('accent');
  
  &__image {
    width: 120px;
    height: 120px;
    object-fit: cover;
    border-radius: 8px;
  }
  
  &__info {
    flex: 1;
  }
  
  &__name {
    margin: 0 0 spacer(1);
    font-size: font-size('lg');
    font-weight: 600;
  }
  
  &__price {
    margin: 0 0 spacer(2);
    font-size: font-size('2xl');
    font-weight: 700;
    color: color('accent');
  }
  
  &__button {
    display: inline-block;
    padding: spacer(2) spacer(4);
    background: color('accent');
    color: white;
    text-decoration: none;
    border-radius: 8px;
    font-weight: 600;
    transition: background 0.2s;
    
    &:hover {
      background: darken(color('accent'), 10%);
    }
  }
}
```

---

## 📦 SHOPRENTER INTEGRÁCIÓ

### layouts/shortcodes/product.html
```html
{{- $name := .Get "name" -}}
{{- $url := .Get "url" -}}
{{- $price := .Get "price" -}}
{{- $image := .Get "image" -}}
{{- $description := .Get "description" | default "" -}}

{{- $utmSource := site.Params.shopUTMSource | default "blog" -}}
{{- $utmCampaign := .Page.File.ContentBaseName -}}
{{- $trackingURL := printf "%s?utm_source=%s&utm_campaign=%s" $url $utmSource $utmCampaign -}}

<div class="product-cta">
  {{ if $image }}
  <img src="{{ $image }}" alt="{{ $name }}" class="product-cta__image" loading="lazy">
  {{ end }}
  
  <div class="product-cta__info">
    <h4 class="product-cta__name">{{ $name }}</h4>
    
    {{ if $price }}
    <p class="product-cta__price">{{ $price }} Ft</p>
    {{ end }}
    
    {{ if $description }}
    <p class="product-cta__description">{{ $description }}</p>
    {{ end }}
    
    <a href="{{ $trackingURL }}" 
       class="product-cta__button"
       target="_blank"
       rel="noopener">
      Megnézem a shopon →
    </a>
  </div>
</div>
```

### Használat cikkben:
```markdown
## Ajánlott termékek

{{< product 
    name="Bio MCT Olaj 500ml"
    url="https://shop.dietaplaza.hu/bio-mct-olaj"
    price="8990"
    image="/images/products/mct-olaj.webp"
    description="Gyors energia keto diétához"
>}}
```

---

## 📊 SEO & SCHEMA.ORG

### layouts/partials/seo-meta.html
```html
<!-- Primary Meta Tags -->
<title>{{ if .IsHome }}{{ site.Title }}{{ else }}{{ .Title }} | {{ site.Title }}{{ end }}</title>
<meta name="title" content="{{ if .IsHome }}{{ site.Title }}{{ else }}{{ .Title }} | {{ site.Title }}{{ end }}">
<meta name="description" content="{{ with .Params.seo.description }}{{ . }}{{ else }}{{ .Summary | truncate 155 }}{{ end }}">
<meta name="keywords" content="{{ with .Params.seo.keywords }}{{ delimit . ", " }}{{ end }}">
<meta name="author" content="{{ with .Params.author }}{{ . }}{{ else }}{{ site.Params.author }}{{ end }}">

<!-- Canonical URL -->
<link rel="canonical" href="{{ with .Params.seo.canonical }}{{ . }}{{ else }}{{ .Permalink }}{{ end }}">

<!-- Robots -->
<meta name="robots" content="{{ with .Params.seo.robots }}{{ . }}{{ else }}index, follow{{ end }}">

<!-- Open Graph / Facebook -->
<meta property="og:type" content="{{ if .IsPage }}article{{ else }}website{{ end }}">
<meta property="og:url" content="{{ .Permalink }}">
<meta property="og:title" content="{{ .Title }}">
<meta property="og:description" content="{{ with .Params.description }}{{ . }}{{ else }}{{ .Summary | truncate 155 }}{{ end }}">
<meta property="og:image" content="{{ with .Params.og_image }}{{ . | absURL }}{{ else }}{{ with .Params.image }}{{ . | absURL }}{{ else }}{{ site.Params.images | index 0 | absURL }}{{ end }}{{ end }}">
<meta property="og:site_name" content="{{ site.Title }}">
<meta property="og:locale" content="hu_HU">

<!-- Twitter Card -->
<meta name="twitter:card" content="{{ with .Params.twitter_card }}{{ . }}{{ else }}summary_large_image{{ end }}">
<meta name="twitter:url" content="{{ .Permalink }}">
<meta name="twitter:title" content="{{ .Title }}">
<meta name="twitter:description" content="{{ with .Params.description }}{{ . }}{{ else }}{{ .Summary | truncate 155 }}{{ end }}">
<meta name="twitter:image" content="{{ with .Params.og_image }}{{ . | absURL }}{{ else }}{{ with .Params.image }}{{ . | absURL }}{{ else }}{{ site.Params.images | index 0 | absURL }}{{ end }}{{ end }}">

<!-- Article specific -->
{{ if .IsPage }}
<meta property="article:published_time" content="{{ .Date.Format "2006-01-02T15:04:05Z07:00" }}">
<meta property="article:modified_time" content="{{ .Lastmod.Format "2006-01-02T15:04:05Z07:00" }}">
<meta property="article:author" content="{{ with .Params.author }}{{ . }}{{ else }}{{ site.Params.author }}{{ end }}">
{{ range .Params.categories }}
<meta property="article:section" content="{{ . }}">
{{ end }}
{{ range .Params.tags }}
<meta property="article:tag" content="{{ . }}">
{{ end }}
{{ end }}
```

### layouts/partials/schema.html
```html
{{ if .IsPage }}
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "{{ with .Params.schema.type }}{{ . }}{{ else }}Article{{ end }}",
  "headline": "{{ .Title }}",
  "description": "{{ with .Params.description }}{{ . }}{{ else }}{{ .Summary | truncate 155 }}{{ end }}",
  "image": "{{ with .Params.image }}{{ . | absURL }}{{ else }}{{ site.Params.images | index 0 | absURL }}{{ end }}",
  "datePublished": "{{ .Date.Format "2006-01-02T15:04:05Z07:00" }}",
  "dateModified": "{{ .Lastmod.Format "2006-01-02T15:04:05Z07:00" }}",
  "author": {
    "@type": "Person",
    "name": "{{ with .Params.author }}{{ . }}{{ else }}{{ site.Params.author }}{{ end }}"
  },
  "publisher": {
    "@type": "Organization",
    "name": "{{ site.Title }}",
    "logo": {
      "@type": "ImageObject",
      "url": "{{ "images/logo.png" | absURL }}"
    }
  },
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "{{ .Permalink }}"
  }
  {{ with .Params.schema.wordCount }}
  ,"wordCount": {{ . }}
  {{ end }}
}
</script>
{{ end }}

<!-- Breadcrumb Schema -->
{{ if not .IsHome }}
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Főoldal",
      "item": "{{ site.BaseURL }}"
    }
    {{ if .Section }}
    ,{
      "@type": "ListItem",
      "position": 2,
      "name": "{{ .Section | humanize | title }}",
      "item": "{{ .Section | absURL }}"
    }
    {{ end }}
    {{ if .IsPage }}
    ,{
      "@type": "ListItem",
      "position": 3,
      "name": "{{ .Title }}",
      "item": "{{ .Permalink }}"
    }
    {{ end }}
  ]
}
</script>
{{ end }}
```

---

## 📚 PÉLDA CIKK TÉMÁK

### Kategóriák
1. **Diéták**
   - Ketogén diéta
   - Paleo
   - Intermittent Fasting
   - Mediterrán diéta
   - DASH diéta

2. **Fogyókúra**
   - Kalória deficit
   - Makrók számítása
   - Fogyás fenntarthatóan
   - Plató áttörése

3. **Egészséges életmód**
   - Alvás optimalizálás
   - Stresszkezelés
   - Vízfogyasztás
   - Alkohol és diéta

4. **Receptek**
   - Alacsony kalóriás vacsorák
   - Keto desszertek
   - Protein shake-ek
   - Meal prep ötletek

5. **Táplálékkiegészítők**
   - Vitaminok
   - Protein porok
   - MCT olaj
   - Probiotikumok

6. **Sportteljesítmény**
   - Edzés előtti étkezés
   - Fehérje bevitel
   - Szénhidrát ciklus
   - Regeneráció

### 50+ Cikk Ötlet
```
✓ "Ketogén Diéta Kezdőknek 2025: Teljes Útmutató"
✓ "Intermittent Fasting 16/8: Útmutató és Étkezési Terv"
✓ "Mediterrán Diéta: 7 Napos Menü Receptekkel"
✓ "10 Alacsony Kalóriás Vacsora Recept 30 Perc Alatt"
✓ "Fehérje Bevitel Számítása: Hány Gramm Kell Neked?"
✓ "Cukormentesítés: 30 Napos Kihívás Lépésről-Lépésre"
✓ "Vitamin D Hiány: Tünetek, Okok és Megoldás"
✓ "Egészséges Snackek Munkaidőre: 15 Ötlet"
✓ "Prebiotikumok vs Probiotikumok: Mi a Különbség?"
✓ "Makrók Kiszámítása Fogyáshoz: Kalkulátor és Útmutató"
✓ "Keto Grocery Lista: Mit Vásárolj és Mit Kerülj"
✓ "Paleo Diéta: Mire Jó és Mire Nem?"
✓ "DASH Diéta: Vérnyomáscsökkentés Természetesen"
✓ "Meal Prep Kezdőknek: 1 Nap = 5 Nap Étel"
✓ "Protein Shake Receptek: 10 Ízletes Variáció"
✓ "MCT Olaj: Mi Ez és Hogyan Használd?"
✓ "Omega-3 Zsírsavak: Miért Fontosak?"
✓ "Magnesium Hiány: Figyelmeztető Jelek"
✓ "Alkohol és Fogyás: Lehet Inni Diéta Alatt?"
✓ "Alvás és Fogyás: Miért Kritikus a Pihenés?"
✓ "Stressz és Súlygyarapodás: Az Összefüggés"
✓ "Víz vs Egyéb Italok: Mit Igyál?"
✓ "Éhgyomri Kardió: Működik vagy Mítosz?"
✓ "Edzés Előtti Étkezés: Mit Egyél és Mikor?"
✓ "Edzés Utáni Regeneráció: Táplálkozás és Pihenés"
✓ "Szénhidrát Ciklus: Mikor és Miért?"
✓ "Kreatín Kiegészítő: Használat és Hatások"
✓ "BCAA vs Teljes Protein: Melyik Jobb?"
✓ "Glutamin: Szükséges vagy Felesleges?"
✓ "Tesztoterone Boost Természetesen: 10 Tipp"
```

---

## 🔄 TARTALOM WORKFLOW - CLAUDE-DAL

### Lépések új cikk írásához:

```
1. TÉMA MEGHATÁROZÁS
   Te: "Claude, írj egy SEO-optimalizált cikket X témában"
   
2. OUTLINE KÉSZÍTÉS
   Claude: Tartalmi vázlat jóváhagyásra
   
3. CIKK ÍRÁSA
   Claude: 
   - Markdown fájl generálás
   - Frontmatter (SEO meta)
   - Tartalmi szekciók
   - GYIK rész (FAQ schema)
   - Shoprenter termék CTA-k
   
4. KÉPEK
   Claude:
   - Hero image AI-generálás vagy kiválasztás
   - Termékképek linkelése
   - Alt text SEO-ra
   - Optimalizálás (WebP, méret)
   
5. SEO/AEO ELLENŐRZÉS
   Claude:
   - Keywords check
   - Meta description 155 karakter
   - Schema.org markup
   - Internal linkek
   - Readability score
   
6. GIT COMMIT
   Claude (Claude Code-ban):
   - git add content/posts/uj-cikk.md
   - git add static/images/...
   - git commit -m "Új cikk: [Cím]"
   - git push origin main
   
7. AUTO DEPLOY
   GitHub Actions:
   - Hugo build
   - Deploy to GitHub Pages
   - ~2-3 perc → ÉLŐBEN
```

### Időtartam:
- **Cikk írás:** 3-5 perc
- **Képek:** 2-3 perc
- **Review + push:** 1-2 perc
- **Deploy:** 2-3 perc
- **TOTAL:** ~10-15 perc új cikkenként

---

## 🚀 LAUNCH CHECKLIST

### Pre-Launch (4 hét munka után)

```bash
□ Minden oldal betöltődik hibátlanul
□ Mobile teszt (iPhone, Android)
□ Desktop teszt (Chrome, Firefox, Safari)
□ PageSpeed Insights: 90+ (mobile & desktop)
□ SEO audit: green lights
□ Schema.org validation
□ Broken links check
□ Image optimization check
□ SSL certificate működik
□ Google Search Console beállítva
□ Google Analytics tracking kód
□ Sitemap.xml submit GSC-be
□ Robots.txt ellenőrzés
□ 301 redirectek tesztelése
□ Shoprenter linkek működnek
□ UTM paraméterek tracking
□ Newsletter form működik
□ Social share gombok működnek
```

### DNS Átállítás (Launch Day)

```bash
# Shoprenter DNS records
A record: shop.dietaplaza.hu → [Shoprenter IP]

# GitHub Pages DNS records
A record: dietaplaza.hu → 185.199.108.153
A record: dietaplaza.hu → 185.199.109.153
A record: dietaplaza.hu → 185.199.110.153
A record: dietaplaza.hu → 185.199.111.153

# CNAME (ha van www)
CNAME: www.dietaplaza.hu → yourusername.github.io

# TTL: 3600 (1 óra)
# Propagáció: 24-48 óra
```

### Post-Launch (Első 7 nap)

```bash
□ Traffic monitoring (Google Analytics)
□ Search Console errors check
□ 404 errors monitoring
□ Shoprenter conversion tracking
□ User feedback gyűjtés
□ Performance monitoring
□ SEO ranking changes
□ Social media mentions
```

---

## 📊 TELJESÍTMÉNY CÉLOK

### PageSpeed Insights
- **Mobile:** 90+
- **Desktop:** 95+

### Core Web Vitals
- **LCP:** < 2.5s (Largest Contentful Paint)
- **FID:** < 100ms (First Input Delay)
- **CLS:** < 0.1 (Cumulative Layout Shift)

### SEO Metrics
- **Meta description:** 145-155 karakter
- **Title tag:** 50-60 karakter
- **H1:** 1 db/oldal
- **Internal links:** 3-5 db/cikk
- **External links:** 2-3 db/cikk (authority sites)
- **Image alt text:** minden képen

### Tartalom Metrics
- **Cikk hossz:** 1500-3000 szó
- **Bekezdések:** 2-4 mondat max
- **Readability:** Flesch Reading Ease 60+
- **Képek:** 2-5 db/cikk
- **Shoprenter CTA:** 1-3 db/cikk

---

## 🔗 HASZNOS LINKEK

### Fejlesztői Eszközök
- **Hugo Docs:** https://gohugo.io/documentation/
- **Spruce CSS Docs:** https://sprucecss.com/docs/
- **GitHub Pages:** https://pages.github.com/
- **GitHub Actions:** https://docs.github.com/actions

### SEO Eszközök
- **Google Search Console:** https://search.google.com/search-console
- **Google Analytics:** https://analytics.google.com/
- **PageSpeed Insights:** https://pagespeed.web.dev/
- **Schema Markup Validator:** https://validator.schema.org/

### Design Inspiráció
- **Sage Theme Demo:** https://sage.storiedthemes.com/
- **Hugo Themes:** https://themes.gohugo.io/

---

## 📝 JEGYZETEK & MEGJEGYZÉSEK

### Spruce CSS Specifikus Megjegyzések
- Hugo Extended verzió szükséges a Sass fordításhoz
- `hugo version` parancs ellenőrzés: "extended" szerepeljen
- Spruce CSS fájlokat ne módosítsd közvetlenül
- Custom stílusok: `assets/scss/_custom.scss`

### GitHub Pages Limitek
- **Repo méret:** 1 GB max
- **Bandwidth:** 100 GB/hó
- **Build limit:** 10 build/óra
- **Minden limit túl bőséges egy bloghoz**

### Spruce CSS Hasznos Mixinek
```scss
// Breakpoint
@include breakpoint('md') { ... }

// Spacer
margin-bottom: spacer(4);

// Color
background: color('accent');

// Font size
font-size: font-size('xl');
```

### Hugo Shortcodes Készítés
```html
<!-- layouts/shortcodes/note.html -->
<div class="note note--{{ .Get "type" }}">
  {{ .Inner }}
</div>
```

```markdown
<!-- Használat -->
{{< note type="info" >}}
Ez egy info doboz
{{< /note >}}
```

---

## ✅ KÖVETKEZŐ LÉPÉSEK

1. **Claude Code megnyitás**
2. **Ez a dokumentum átmásolása** a projekt mappába
3. **Hugo projekt inicializálás** (hét 1, nap 1)
4. **Spruce CSS integráció** (hét 1, nap 3-4)
5. **Design fejlesztés** (hét 2)
6. **SEO + Shoprenter** (hét 3)
7. **Tartalom + Launch** (hét 4)

---

**Készítette:** Claude (Anthropic)  
**Verzió:** 1.0  
**Utolsó frissítés:** 2026. május 14.  
**Projekt státusz:** 🟢 Kezdésre kész

---

*Ez a dokumentum tartalmazza az összes szükséges információt a Dietaplaza Hugo blog projekt megvalósításához. Claude Code-ban folytatva a munka minden kontextus rendelkezésre áll.*
