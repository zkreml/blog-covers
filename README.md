# blog-covers

Cover obrázky pro články na [blog.oscloud.cz](https://blog.oscloud.cz).

## Styl

Tmavý (Catppuccin Mocha), JetBrains Mono, dot-grid textura na pozadí, terminálová
kartička vpravo ukazující nějakou akci/příkaz k dané službě, vlevo "hero" grafika
(stack naklopených dlaždic + kulatý ikonický prvek uprostřed), badge pod ním,
title + subtitle dole. Rozměr 1200×630 (OG cover).

Barevná paleta se mění podle služby (např. zelená pro fotky/Ente, modro-fialová
pro Matrix/mxchat), zbytek layoutu zůstává stejný.

## Struktura

Jedna složka na článek/službu:

```
<služba>/
  <služba>-cover.html
  <služba>-cover.png
```

Např.:

```
ente/
  ente-cover.html
  ente-cover.png
mxchat/
  mxchat-cover.html
  mxchat-cover.png
```

## Render HTML → PNG

```
wkhtmltoimage --width 1200 --height 630 --quality 95 <soubor>.html <soubor>.png
```

## Použití

PNG se nahrává jako cover obrázek k příslušnému článku v blog.sh (`cover.image`
resp. dle aktuální šablony blog.sh). HTML se drží v repu jako zdroj pro budoucí
úpravy nebo přegenerování.
