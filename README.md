# 🎒 Lista Bagaje

Aplicație web simplă pentru lista de bagaje de excursie. Funcționează direct în browser, pe telefon sau pe calculator, fără cont și fără internet (după prima deschidere).

**👉 Deschide aplicația: https://ionutdragnea-glitch.github.io/lista_de_luat/**

## Ce face

- **Adaugă bagaje** — scrii în bara de jos, alegi categoria și apeși `+`.
- **Șterge bagaje** — `✕` din dreapta fiecărei linii.
- **Bifează ce ai luat** — apeși pe rând sau pe pătrățel. Bagajul rămâne vizibil, dar tăiat și estompat, ca să nu îți mai distragă atenția.
- **Contor** — cercul din antet arată câte bagaje **au mai rămas** de luat, iar sub titlu vezi „X din Y luate". Fiecare categorie are propriul contor `luate/total`.
- **Categorii** — poți adăuga categorii noi, le poți pliza (tap pe titlu) sau șterge.
- **⛺ Camping 5 zile** — listă completă, gata făcută, pentru o vacanță cu cortul într-un camping (10 categorii, peste 100 de bagaje): cort și dormit, bucătărie de camping, mâncare pentru 5 zile, îmbrăcăminte, igienă, trusă medicală, lumină și energie, scule și diverse, documente și bani, timp liber.
- **👁 Ascunde luate** — vezi doar ce mai ai de pus în bagaj.
- **↺ Debifează tot** — refolosești aceeași listă la următoarea excursie.
- **🗑 Golește lista** — pornești de la zero.

## Pe telefon

Deschide linkul, apoi:

- **Android / Chrome**: meniul `⋮` → *Adaugă la ecranul de pornire*
- **iPhone / Safari**: butonul *Share* → *Add to Home Screen*

Aplicația se instalează ca o iconiță normală, pornește pe tot ecranul și merge și offline (util în camping, unde semnalul lipsește).

## Unde se salvează datele

Totul se salvează local, în `localStorage`-ul browserului de pe dispozitivul tău. Nu există server, cont sau sincronizare — lista de pe telefon și cea de pe calculator sunt separate. Dacă ștergi datele de navigare ale browserului, lista se pierde.

## Structura proiectului

| Fișier | Rol |
| --- | --- |
| `index.html` | toată aplicația: interfață, stiluri și logică (fără dependențe externe) |
| `sw.js` | service worker pentru funcționare offline |
| `manifest.webmanifest` | configurația de instalare pe telefon (PWA) |
| `icon.svg`, `icon-*.png` | iconițele aplicației |

## Rulare locală

Deschide `index.html` direct în browser, sau pornește un server local (necesar pentru service worker):

```bash
python -m http.server 8000
# apoi http://localhost:8000
```
