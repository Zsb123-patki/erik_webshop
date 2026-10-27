# Mágnespont webshop

Egytermékes webshop a SmallRig 5460 MagSafe telefontartóhoz. Személyes átvétel: 1039 Budapest, Királyok útja 194.

Statikus oldal, build lépés nélkül: `index.html` + `img/` mappa. Bármilyen statikus tárhelyre feltölthető (Netlify, Vercel, Cloudflare Pages, saját szerver).

## Tartalom

- Termékblokk galériával, mennyiségválasztóval és kosárral
- Műszaki adatsor, használati példák, felszerelés három lépésben
- Négyféle termékleírás fülekre bontva (Röviden, Edzéshez, Otthonra, Műszaki adatok)
- Helyőrző a bolt valódi Google-értékeléseinek
- Bolt és Google Maps térkép, útvonaltervezés
- Kapcsolat: telefonszám, visszahívás-kérő űrlap
- GYIK, mobilos ragadós vásárlósáv, világos és sötét mód

## Beállítás

Minden bolti adat az `index.html` script részének elején, a `STORE` és `PRODUCT` objektumban van:

| Mező | Mire való |
| --- | --- |
| `STORE.name` | A bolt neve (most munkanév: Mágnespont) |
| `STORE.phoneDisplay`, `STORE.phoneE164` | Telefonszám megjelenítve és hívás-linkhez |
| `STORE.address`, `STORE.mapsQuery` | Cím és a térkép keresőkifejezése |
| `STORE.orderEndpoint` | URL, ahová a rendelés POST-tal, JSON-ként megy |
| `STORE.contactEndpoint` | URL, ahová a visszahívás-kérés megy |
| `PRODUCT.price`, `COURIER_FEE` | Termékár és futárdíj forintban (most helykitöltő: 8 990 Ft és 1 690 Ft) |

Amíg az `orderEndpoint` és a `contactEndpoint` üres, az űrlapok nem küldenek semmit, és a telefonszámot ajánlják.

## Megjegyzések

- **Google Maps:** a saját domainen a térkép beágyazva jelenik meg. Előnézetben (claude.ai, `file://`) vázlatos térkép látszik.
- **Értékelések:** az oldalon „Minta helye” jelölésű üres helyek vannak. Ide a bolt valódi Google-értékelései kerüljenek (Places API vagy értékelés-widget).
- **Képek:** a hangulatfotók Figma AI-jal generált illusztrációk. A `product.webp` az eredeti termékfotó.
- **Design:** a szerkeszthető Figma-terv: https://www.figma.com/design/qua1IVF3I6xOFHC13K7fFl

A SmallRig a gyártó védjegye.
