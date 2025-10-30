# Hra na agenta - Jednoduchá HTML verzia

Toto je zjednodušená verzia aplikácie "Hra na agenta" v jednom súbore, ktorá sa dá hostiť na GitHub Wiki alebo akomkoľvek statickom webhostingu.

## Čo je súčasťou

- **index.html** - Kompletná samostatná aplikácia so všetkými funkciami:
  - Herné inštrukcie
  - Generátor protokolu stanice so šifrovacími kolieskami
  - Generátor protokolu riadiacej stanice
  - Albertiho šifrovanie
  - Funkcia tlače
  - Všetky štýly a JavaScript sú vnorené

## Funkcie

✅ Nevyžaduje sa žiadny proces zostavovania
✅ Žiadne závislosti
✅ Funguje offline
✅ Dá sa hostiť na GitHub Wiki
✅ Protokoly optimalizované pre tlač
✅ Plne responzívny dizajn
✅ Generuje protokoly staníc so šifrovacími kolieskami
✅ Generuje vnútorné šifrovacie kolieska na vystrihnutie a montáž
✅ Albertiho šifrovanie s nastaviteľnými kľúčmi
✅ Generátor protokolu riadiacej stanice s automatickým generovaním slov

## Ako používať

### Možnosť 1: Otvorte lokálne
Jednoducho dvakrát kliknite na `index.html` a otvorí sa vo vašom webovom prehliadači.

### Možnosť 2: Hostovanie na GitHub Wiki

1. Prejdite na Wiki vášho GitHub repozitára
2. Vytvorte novú stránku
3. Kliknite na "Edit" a prepnite do režimu editora "HTML"
4. Skopírujte a vložte celý obsah súboru `index.html`
5. Uložte stránku

### Možnosť 3: Hostovanie na GitHub Pages

1. Skopírujte `index.html` do svojho repozitára
2. Povoľte GitHub Pages v nastaveniach repozitára
3. Nastavte zdroj na vetvu obsahujúcu súbor
4. Prístup cez `https://om0wt.github.io/om8jota/index.html`

### Možnosť 4: Akýkoľvek webový server

Nahrajte `index.html` na akúkoľvek webhostingovú službu. Súbor je úplne samostatný.

## Použitie

1. **Inštrukcie** záložka - Prečítajte si herné inštrukcie

2. **Protokol stanice** záložka - Generovanie protokolov staníc na tlač
   - **Protokol Stanice** podzáložka:
     - Nastavte počet kópií
     - Kliknite na "Tlačiť protokol" pre tlač
   - **Vnútorné Kotúče** podzáložka:
     - Nastavte veľkosť kolieska (ovplyvňuje, koľko sa zmestí na stranu)
     - Nastavte počet vnútorných koliesok na vygenerovanie
     - Kliknite na "Tlačiť kotúče" pre tlač
     - Vystrihnite kolieska a vložte ich do protokolov staníc

3. **Protokol riadiacej stanice** záložka - Generovanie protokolu riadiacej stanice
   - Nastavte počet staníc
   - Zadajte šifrovací kľúč (2 písmená, napr. "xA")
   - Zadajte výslednú frázu (slová oddelené medzerami)
   - Voliteľne zadajte kontrolné slová pre 2. riadok
   - Kliknite na "Generovať protokol" pre vygenerovanie
   - Kliknite na "Tlačiť" pre tlač

## Technické detaily

- Čisté HTML5, CSS3 a vanilla JavaScript
- Žiadne externé závislosti
- Veľkosť súboru: ~41KB (1112 riadkov)
- Kompatibilné so všetkými modernými prehliadačmi
- Optimalizované pre tlač so samostatnými režimami na výšku/na šírku
- Generovanie šifrovacích koliesok založené na SVG
- Dynamický výpočet rozloženia stránky pre optimálnu tlač

