# Småsteg

Prototyp av en app för coachning i vardagens exekutiva förmågor, för vuxna med t.ex. ADHD, autism, förvärvad hjärnskada eller stressrelaterad utmattning. Appen är ett stöd och ersätter inte vård.

## Kör

Öppna `index.html` i en webbläsare. Allt ligger i den filen, och inget byggsteg behövs. Typsnitten hämtas från Google Fonts.

## Status

| Steg | Innehåll | Status |
|---|---|---|
| 1 | Designriktning, onboarding (5 frågor), Idag med energiincheckning och dagsplan, sessionsspelare | Klart |
| 2 | Utforska (8 kategorier), kategorisidor, programsida med paus och passlängd, komplett program ”Planera och prioritera”, 16 enskilda strategier | Klart för återkoppling |
| 3 | Just nu-övningar, Framsteg, Vart kan jag vända mig?, Om appen, Inställningar | Platshållare finns |

## Struktur i `index.html`

| Del | Var | Vad |
|---|---|---|
| Designtokens | `<style>`, `:root` | Färger (ljust och mörkt tema), typsnitt, radier, rörelse |
| Innehåll | `<script type="application/json" id="innehall">` | Kategorier, livsområden, program, strategier, Just nu, reflektion. Varje session och strategi har fältet `granskning` med den princip den bygger på. Strategier har `livsomraden` som etiketter. |
| Illustrationer | `SCENES`, `MINI` | Inline-SVG, en scen per kategori |
| Lagring | `load()` / `save()` | `localStorage`, nyckeln `smasteg:v1`. Allt går via två funktioner så att synk kan läggas till senare. |
| Vyer | `VIEWS` | En funktion per skärm |
| Handlingar | `ACT` | Klick hanteras via `data-act` på elementen |

Innehållet är **inte granskat** av arbetsterapeut.
