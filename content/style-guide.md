---
title: "Style Guide"
description: "Komponens galéria és tipográfiai minták a Dietaplaza dizájn rendszeréhez."
date: 2026-01-01T00:00:00+01:00
draft: false
author: "Dietaplaza"
sitemap:
  disable: true
seo:
  robots: "noindex, nofollow"
type: "style-guide"
layout: "single"
---

A jelen oldal a Dietaplaza tervezési rendszer komponenseit és tipográfiai elemeit mutatja be. Belső használatra készült, hogy a fejlesztők és a tartalomszerkesztők egy helyen lássák, milyen elemekből lehet építkezni.

<!--more-->

## Tipográfia

A főcímek Lora serif betűtípussal, a folyó szöveg Poppins sans-serif fontcsaláddal készül. A címek alapsúlya 500-as (medium), így megőrzik az elegáns, magazinos megjelenést.

<h1>Főcím példa</h1>

A H1 a poszt fő címeként jelenik meg, általában csak egy van belőle oldalanként. A `single.html` template automatikusan rendereli a `.post-header__title` osztállyal.

<h2>Másodlagos cím</h2>

A H2 a poszt nagyobb szekcióinak főcíme — pl. fejezetek, jelentős részegységek elválasztására.

<h3>Harmadlagos cím</h3>

Ez egy bekezdés egy harmadlagos cím alatt. A folyó szöveg sortávolsága 1.7, ami kényelmes olvasási élményt biztosít hosszabb cikkeknél is. **Vastagított rész** és *dőlt rész* is használható a szövegben.

<h4>Negyedik szintű cím</h4>

A negyedik szintű címek általában al-szekcióknak fenntartottak. Alattuk általában rövidebb bekezdés vagy lista található.

A főoldal hero és a cikk fejlécében nem a sima `h1` jelenik meg, hanem két dedikált display osztály, eltérő — nagyobb — méretekkel. Ezek **nem** használhatók a folyó szövegben.

<p class="hero__title" style="margin: 0 0 1rem;">Hero szöveg</p>

A `.hero__title` a főoldal hero szekciójához tartozik. Desktop méretben `clamp(5rem, 6vw, 6rem)` (kb. 80–96px), legnagyobb display méret a rendszerben.

<p class="post-header__title" style="margin: 0 0 1rem;">Poszt fejléc</p>

A `.post-header__title` a cikkek (és a jelen Style Guide) fejlécében jelenik meg. Desktop méretben 72px, a hero alatt, de a body H1-nél (40px) jóval nagyobb.

## Listák

Pontos lista (unordered):

- Egyszerűbb, áttekinthető pontok
- Több sornyi szöveg is fér el egy pontba, ha kell
- A behúzás és a térköz konzisztens marad

Számozott lista (ordered):

1. Első lépés
2. Második lépés a folyamatban
3. Harmadik és záró lépés

## Idézet

Standard változat — vastag, sage zöld bal szegély, bold cím-jellegű tipográfia:

> Az egészség nem minden, de minden semmi egészség nélkül. Az étrend, a mozgás és a megfelelő pihenés mind szükségesek a jólléthez.

Alternatív változat — nagy idézőjel ikonnal, könnyedebb dőlt szöveggel:

<blockquote class="blockquote-alt">
<p>Az egészség nem minden, de minden semmi egészség nélkül. Az étrend, a mozgás és a megfelelő pihenés mind szükségesek a jólléthez.</p>
</blockquote>

## Toggle

Az akkordion komponens hasznos hosszabb tartalom rendezett, helytakarékos bemutatásához. Kattintásra nyílik és csukódik, JavaScript nélkül.

<details class="toggle">
  <summary class="toggle__summary">Mit jelent a növényi alapú étrend?<span class="toggle__icon"></span></summary>
  <div class="toggle__content">
    <p>Olyan étrend, ahol a tányérod 75–100%-a növényi eredetű: zöldség, gyümölcs, hüvelyes, teljes kiőrlésű gabona, magvak és olajos magvak. Az állati eredetű ételek opcionálisak és kis mennyiségben kerülnek bele.</p>
  </div>
</details>

<details class="toggle">
  <summary class="toggle__summary">Hogyan kezdjek bele a 16/8 böjtbe?<span class="toggle__icon"></span></summary>
  <div class="toggle__content">
    <p>Indulj 12 órás étkezési ablakkal és fokozatosan csökkentsd 8 órára. A leggyakoribb forma: 12:00 és 20:00 között étkezel, ezen kívül csak vizet, teát és fekete kávét fogyasztasz.</p>
  </div>
</details>

<details class="toggle">
  <summary class="toggle__summary">Veszélyes a cukor teljes elhagyása?<span class="toggle__icon"></span></summary>
  <div class="toggle__content">
    <p>Nem — a hozzáadott cukor elhagyása biztonságos és általában rövid távon kedvező hatással jár. Az első héten jelentkezhetnek megvonási tünetek (fáradtság, fejfájás), de ezek pár nap alatt elmúlnak.</p>
  </div>
</details>

## Képek

A poszt fejlécében a `image` frontmatter mező adja meg a hero képet, az opcionális `imageCaption` pedig a kép alatt megjelenő rövid leírást. A `figure` és `figcaption` szemantikus elemekkel jelenik meg.

<figure class="post-header__image" style="width: 100%; max-width: 100%;">
  <img src="/images/posts/cukormentesites.jpg" alt="Cukor és édesség" style="aspect-ratio: 16 / 9;">
  <figcaption class="post-header__image-caption">Fotó: <a href="https://pixabay.com">Pixabay</a></figcaption>
</figure>

## Linkek és kiemelés

A folyó szövegben [hivatkozás más oldalra](#) így néz ki — aláhúzott, ugyanabban a betűszínben. Egy `kódrészlet` is megjeleníthető monospace fontkészlettel.

## Callout boxok

A callout-okkal a kulcsfontosságú információkra hívjuk fel az olvasó figyelmét. Emoji-ikont használunk balra, mellette a szöveg.

<div class="callout callout--blue">
  <div class="callout__emoji">💡</div>
  <div class="callout__text">A mediterrán étrend a kutatások szerint csökkenti a szív- és érrendszeri betegségek kockázatát.</div>
</div>

<div class="callout callout--yellow">
  <div class="callout__emoji">⚠️</div>
  <div class="callout__text">Új étrendi vagy mozgásprogram indítása előtt mindig konzultálj szakemberrel.</div>
</div>

<div class="callout callout--green">
  <div class="callout__emoji">✅</div>
  <div class="callout__text">Heti egy húsmentes nap is mérhető előnyt jelenthet az egészségedre.</div>
</div>

<div class="callout callout--red">
  <div class="callout__emoji">🚨</div>
  <div class="callout__text">Vigyázat: a túl drasztikus kalóriamegszorítás visszacsapást és hosszabb távú anyagcsere-lassulást okozhat.</div>
</div>

<div class="callout callout--grey">
  <div class="callout__emoji">📝</div>
  <div class="callout__text">Vezess naplót az étkezéseidről — a tudatosság fél siker a fogyókúrában.</div>
</div>

<div class="callout callout--accent">
  <div class="callout__emoji">🥗</div>
  <div class="callout__text">Hangsúlyos figyelmeztetés vagy Pro tip a sage zöld márkaszín kiemelésével.</div>
</div>

## Gombok

<p>
<a href="#" class="btn btn--primary">Elsődleges gomb</a>
&nbsp;
<a href="#" class="btn btn--secondary">Másodlagos gomb</a>
</p>

## Táblázat

| Tápanyag    | Forrás                  | Napi ajánlás |
| ----------- | ----------------------- | ------------ |
| B12-vitamin | Tojás, hal, dúsított tej | 2.4 µg       |
| Vas         | Hüvelyesek, leveles zöldek | 8–18 mg    |
| Kalcium     | Tejtermékek, magvak     | 1000 mg      |
| Omega-3     | Halak, lenmag, dió      | 1.1–1.6 g    |

## Termék CTA

<div class="product-cta">
  <div class="product-cta__placeholder" aria-hidden="true">🖼️</div>
  <div class="product-cta__info">
    <h3 class="product-cta__name">Példa termék</h3>
    <p class="product-cta__description">Rövid leírás a termékről, ami segít a poszt témájához kapcsolódó vásárlásra ösztönözni az olvasót.</p>
    <p class="product-cta__price">4 990 Ft</p>
    <a href="#" class="product-cta__button">Megnézem <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg></a>
  </div>
</div>

## Ikonok

Az ikonok az `assets/icons/` mappában találhatók. Beillesztés template-ben `{{ partial "icon.html" "név" }}`, markdown-ban `{{</* icon "név" */>}}` (csak NEM HTML blokkon belül). Új ikon hozzáadásához tegyél egy SVG fájlt a mappába.

<div class="icon-grid">
  <div class="icon-grid__item">
    {{< icon "instagram" >}}
    <span class="icon-grid__name">instagram</span>
  </div>
  <div class="icon-grid__item">
    {{< icon "facebook" >}}
    <span class="icon-grid__name">facebook</span>
  </div>
  <div class="icon-grid__item">
    {{< icon "youtube" >}}
    <span class="icon-grid__name">youtube</span>
  </div>
  <div class="icon-grid__item">
    {{< icon "tiktok" >}}
    <span class="icon-grid__name">tiktok</span>
  </div>
  <div class="icon-grid__item">
    {{< icon "arrow-right" >}}
    <span class="icon-grid__name">arrow-right</span>
  </div>
  <div class="icon-grid__item">
    {{< icon "plus" >}}
    <span class="icon-grid__name">plus</span>
  </div>
  <div class="icon-grid__item">
    {{< icon "search" >}}
    <span class="icon-grid__name">search</span>
  </div>
</div>

## Címkék

<ul class="tag-list">
  <li><a href="#" class="tag">mediterrán</a></li>
  <li><a href="#" class="tag">fogyókúra</a></li>
  <li><a href="#" class="tag">cukormentes</a></li>
  <li><a href="#" class="tag">receptek</a></li>
</ul>

## CTA box

A CTA box a `single.html` template által automatikusan beillesztett komponens — a poszt törzse alatt jelenik meg. Az alábbi mintapélda a stílust mutatja.

<aside class="post-cta">
  <div class="post-cta__inner">
    <h2 class="post-cta__title">Légy a Dietaplaza tagja</h2>
    <p class="post-cta__text">Iratkozz fel és kapd meg minden cikkünket egyenesen az emailedbe.</p>
    <a href="#" class="post-cta__button">Feliratkozás</a>
    <small class="post-cta__small">Már tag vagy? <a href="#">Jelentkezz be.</a></small>
  </div>
</aside>
