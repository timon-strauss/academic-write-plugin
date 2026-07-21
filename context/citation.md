# Zitieren in Typst

**Regel**: keine Zitate erfinden

`quelle` = Key aus der `.bib`. `supplement` wie beschrieben.

## Zitatangabe
```typst
#cite(<quelle>, supplement: "...")
```

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
- **Indirekt (Paraphrase, Standardfall):** `Vgl. ` an den Anfang des `supplement`.
- **Direkt:** kein `Vgl.`.

Seiten müssen in der Quelle stehen; Nimm **niemals** die PDF Seite!

| Quelle | Angabe im Beleg | supplement |
|--------------------|-----------------|----------|
| Quelle mit seiten | Seite | `S. N` |
| Webseite mit Abschnitten | Abschnitt | `Abschn. N]` |
| E-Book / PDF mit Kapiteln | Kapitel | `Kap. N` |
| Fließtext ohne Struktur | Absatz | `Abs. 7` |
| Norm / Standard | Abschnitt/Klausel | `Abschn. N.N` |
| Gesetz | Paragraph/Artikel | `§ N` |
| Video / Audio | Zeitstempel | `mm:ss` |
