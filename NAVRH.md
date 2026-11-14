# Mačko bomba – návrh (první prototyp)

Hra vzniká postupně podle diktátu a kreslených obrázků. Originální fotky kreseb
jsou v `kresby/`, vyřezané herní obrázky (průhledné pozadí) v `img/`.

Technika: HTML5 hra (`index.html`), běží v mobilním prohlížeči na šířku,
ovládá se dotykem, dá se „Přidat na plochu“ a hraje se jako aplikace.

## Obrázky a jejich role

| # | Kresba | Herní obrázek | Co to je | Co dělá ve hře |
|---|--------|---------------|----------|----------------|
| 1 | `kresby/01-logo.jpg` | `img/logo.png` | Logo „MACKO BOMBA“ | Značka hry, úvodní animace (logo vyskočí a pohupuje se) |
| 2 | `kresby/02-emanuel.jpg` | `img/emanuel.png` | Jednooký motýlek **Emanuel** | Létá nad herním polem a mává křídly |
| 3 | `kresby/03-macko.jpg` | `img/macko.png` | Medvěd **Macko** | Chodí po cestě a krade vajíčka; když narazí do Emy, ubere jí život |
| 4 | `kresby/04-ema.jpg` | `img/ema.png` | Hráčka **Ema** | Hlavní postava – chodí po cestě a sbírá vajíčka |
| 5 | `kresby/05-kure.jpg` | `img/kure.png` | Kuřátko | Pobíhá a zobe; kdo ho chytí, má 10 s bonus **×3 body** |
| 6 | `kresby/06-vejce1.jpg` | `img/vejce1*.png` | Vajíčko s prasklinou | Hlavní vajíčko ke sbírání, 10 bodů; 6 barev (žlutá, růžová, modrá, zelená, oranžová, fialová) |
| 7 | `kresby/07-vejce2.jpg` | `img/vejce2*.png` | Puntíkaté vajíčko | Druhý typ vajíčka, 10 bodů; stejných 6 barev |
| 8 | `kresby/08-jahoda.jpg` | `img/jahoda.png` | **Jahůdka** | Bonus +20 bodů |
| 9 | `kresby/09-herni-pole.jpg` | `img/cesta.png`, `img/hodiny.png` | Herní pole – cesta, hodiny, ikonky | Cesta natažená přes obrazovku, po ní se chodí; hodiny vlevo nahoře odpočítávají čas |
| 10 | `kresby/10-ohradka.jpg` | `img/ohradka.png` | Ohrádka | Stojí kolem cesty, pohupuje se; zpoza ní vyskakují vajíčka, kuřátko a jahůdky |

## Pravidla a mechaniky (aktuální stav)

- **Úvod:** logo vyskočí, Ema a Macko přijdou z krajů, Emanuel létá. „Ťukni a hraj!“
- **Ovládání:** ťukni nebo táhni prstem po cestě – Ema tam dojde.
- **Kolo trvá 90 s**, hodiny vlevo nahoře ukazují zbývající čas.
- **Životy:** 3 srdíčka. Když Macko narazí do Emy, ubere jedno.
- **Body:** vajíčko 10, jahůdka 20, kuřátko = 10 s všechno ×3.
- Zpoza ohrádek vyskakují věci, chvíli leží na cestě a pak (blikáním) zmizí.
- **Macko** jde vždy k nejbližšímu vajíčku a sní ho („Ham!“). Postupně zrychluje.
- **Konec:** vyprší čas nebo dojdou životy → přehled bodů a rekord (uloží se v telefonu).

### Doplnil jsem sám (k potvrzení)
- Macko bere životy, když narazí do Emy.
- Bonus ×3 od kuřátka trvá 10 sekund.
- Délka kola 90 s, 3 životy, Macko se postupně zrychluje.
- Hra je na šířku (podle kresby herního pole).

## Otevřené otázky

- Dělá Emanuel ve hře ještě něco jiného, než že létá (např. upouští vajíčka, nebo pomáhá)?
- Má hra mít víc úrovní (rychlejší Macko, víc ohrádek…)?
- Ikonky v kresbě herního pole (horní obdélník s mašlí) – co přesně znamenají?
