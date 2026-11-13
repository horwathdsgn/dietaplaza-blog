# CLAUDE.md – Diéta Pláza blog

Hugo-alapú diétás/táplálkozási blog a dietaplaza.hu címen; a webshop a shop.dietaplaza.hu-ra (Shoprenter) kerül. Cél: AEO/SEO-tartalom, amely a webshop termékeire terel. A teljes terv (ütemterv, design rendszer, frontmatter-sablon) a **DIETAPLAZA-BLOG-PROJEKT.md**-ben van.

## Stack és parancsok
- Hugo (extended) + Spruce CSS (Sass, `sass-embedded`), saját layoutok, téma nélkül.
- Fejlesztés: `npm install`, majd `npm run dev`. Ez a `bin/` mappát (helyi `sass`) a PATH elejére teszi, és draftokkal indítja a `hugo server`-t a 1313-as porton. Preview: `.claude/launch.json` → `hugo-dev`.
- Build: `npm run build`.
- **Szándékosan csak helyben fut**, mert a domain még nincs eldöntve. A GitHub Pages ki van kapcsolva, ezért
  a `.github/workflows/hugo.yml` (Hugo 0.155.2, Node 20) minden `main`-re pusholáskor elbukik. Ez várt
  viselkedés, nem hiba: ne javítsd, és ne kapcsold be a Pages-t, amíg a user nem dönt a domainről.
  Akkor a `baseURL`-t (`hugo.toml`) is a választott domainhez kell igazítani.

## Tartalom
- Szöveg írásakor vagy átírásakor (cikk, meta, képalt, kategória, CTA) **mindig a `dietaplaza-tartalomiras` skillt** kell használni: GVH-megfelelés (egészségügyi állítások), GEO/AEO, hangnem.
- Új cikk frontmatterje a projekt-doksi sablonját kövesse (SEO, Schema.org, Shoprenter termékek).
- Termék-linkek: az UTM-paramétereket a sablon fűzi hozzá (`single.html`, `product` shortcode, `params.shopUTMSource`), ezért a frontmatterbe és a shortcode-ba UTM nélküli URL kerüljön.

## Szabályok
- Branch → PR → merge, csak jóváhagyás után. Vizuális változásnál előbb élő preview.
- CSS/HTML előbb, JS csak ha szükséges.
