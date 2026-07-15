# Zitieren in Typst

**Regel**: keine Zitate erfinden

`quelle` = Key aus der `.bib`. `supplement` wie beschrieben.

## Zitatangabe
```typst
#cite(<quelle>, supplement: "...")
```
- **Indirekt (Paraphrase, Standardfall):** `Vgl. ` an den Anfang des `supplement`.
  `#cite(<quelle>, supplement: "Vgl. S. 1")`
- **Direkt:** kein `Vgl.`.

## Direktes Zitat
- **<40 Wörter — inline:**
  ```typst
  #quote(block: false)[
    wörtlicher Text
    ]
    #cite(<quelle>, supplement: "...")
  ```
- **≥40 Wörter — eingerückt:**
  ```typst
  #quote(block: true)[
    wörtlicher Text
    #cite(<quelle>, supplement: "...")
  ]
  ```

## supplement

**Regel**: passendes Supplement gefunden: mich warnen; nicht ausdenken

Fundstelle als Text. Aufbau je‘ nach Quelle:
- **Mit Seite:** `S. N` — Folgeseite `S. N f.`, mehrere `S. N ff.`
- **Ohne Seite:** `Kap N.N, „Titel“, Abschn. „Abschnitt“`
- **Direktes Zitat:** zusätzlich Zeilenangabe dahinter: `S. N, Z. N-N` bzw. `Kap N.N „Titel“, Abschn. „Abschnitt“, Z. N-N`
- **Indirekt:** `Vgl. ` davor: `Vgl. S. N`
