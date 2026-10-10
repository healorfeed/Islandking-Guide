# Island King – Datenbasis (Stand 10.10.2026)

Alle Werte wurden am 10.10.2026 aus dem laufenden Spiel ausgelesen (Spielregeln, Tech-Tree, Werft, Kaserne, Burg, Inselseiten, Kampfrechner, Update-Log, Forum). Es wurde nur gelesen; der Kampfrechner verändert laut Spiel keinen Spielstand. Stand ist nach dem Kampfkonzept 2.0 vom 9.10.2026.

## Dateien

| Datei | Inhalt |
|---|---|
| `../islandking_daten.ods` | Alles in einer Tabelle: Gebäude, Forschungen, alle Stufen, Einheiten, Produktion, Kampfsims, Flottenmix |
| `rules.json` | Alle Live-Spielwerte (Faktoren, Kampf, Plünderung, Kronen, Punkte, Diamanten) |
| `units.csv` | Schiffe, Soldaten, Anlagen, Stadtmauer: Angriff, HP, Tempo, Laderaum, Kosten, Kronen, Bauzeit, Voraussetzungen |
| `requirements.csv` | Alle Voraussetzungen (Gebäude, Forschung, Einheiten) mit Stufe und Geltungsbereich |
| `levels_costs.csv` | Kosten und ungefähre Bauzeit je Stufe (Stufe 1 bis Max) für alle gemessenen Gebäude und Forschungen, aus der Formel |
| `cost_formulas.csv`, `fitted_bases.json` | Kostenformel je Gebäude/Forschung: `Kosten(L) = Basis × 1.2^(L−1)` |
| `production.csv` | Gemessene Minenförderung bei mehreren Stufen |
| `combat_sims.csv` | 42 Kampfrechner-Läufe (gleicher Ressourcenwert je Seite) und Mechanik-Proben |
| `changelog_balance.md` | Balance-relevante Update-Log-Einträge 2.8.–10.10.2026 |
| `forum_notes.md` | Zusammenfassung der relevanten Forenthreads |
| `raw/techtree_path_cumulative.txt` | Rohdaten des Tech-Trees |

Kostenreihenfolge überall: Holz, Stein, Gold, Kohle (Gebäude und Forschungen kosten keine Kohle).

## Kernergebnisse

**Wirtschaft**
1. Alle Gebäude- und Forschungskosten wachsen exakt ×1.2 je Stufe (Abweichung <0.5 %, nur Rundung). Bauzeiten wachsen ebenfalls etwa ×1.2.
2. Die Minenförderung wächst auch ×1.2 je Stufe: Holz/Stein 15 × 1.2^(L−1), Gold 14 × 1.2^(L−1), Kohle 8 × 1.2^(L−1) pro Stunde, dann × Serverfaktor 1.3, plus 20 Grundproduktion. Die Gebäudebeschreibung «+15 pro Stufe» ist veraltet.
3. Deshalb amortisiert sich jede Minenstufe gleich schnell: Sägewerk/Steinbruch nach rund 138 h (5,8 Tage), Goldmine nach rund 148 h.
4. Reihenfolge: Reichtum 20 zuerst, dann auf jeder Insel Holz/Stein/Gold auf 34 (Lager nur bedarfsdeckend, danach nur Grosslager), dann Kohlemine bis 32, dann die Militärgebäude (siehe `build_order.pdf`). Gold ist für das Militär der Engpass.

**Kampf**
5. Jede Runde feuern beide Seiten gleichzeitig ihren Gesamtangriff × Trefferquote. Der Schaden verteilt sich nach HP-Anteil der Gruppen, Restschaden bleibt stehen. Höchstens 6 Runden, danach hält der Verteidiger.
6. Daraus folgt das Quadratgesetz: Stärke ≈ Gesamtangriff × Gesamt-HP = Anzahl² × Angriff × HP. Effizienz je Einheit = √(Angriff × HP) / Kosten. Die Formel trifft den Kampfrechner sehr genau (27 Schlachtschiffe gegen 47 Fregatten: 15 Überlebende vorhergesagt, 15 im Rechner).
7. Es gibt keine Konter. Weil Angriff und HP multipliziert werden, schlägt eine Mischung aus Schlachtschiffen (Angriff) und Fregatten (HP) die reine Schlachtschiff-Flotte: Optimum rechnerisch 60–70 % des Budgets in Schlachtschiffe (+14 % Stärke). Im Rechner schlagen 17 + 17 klar 27 reine Schlachtschiffe.
8. Pro Rohstoff: Schiffe Schlachtschiff > Fregatte > schwere Galeere > leichte Galeere; Soldaten Schwertkämpfer > einfacher Soldat ≫ Musketier, Kanonier, Ritter. Küstenkanone, Katapult und Kanonenturm sind pro Rohstoff stärker als jedes Schiff.

**Punkte**
9. Jede Einheit zählt 1 Punkt, jede Gebäudestufe 2, jede Forschungsstufe 3, unabhängig von den Kosten. Ein einfacher Soldat bringt pro Mio. Rohstoffe rund 4'500 Punkte, eine Minenstufe auf hohem Niveau rund 60, ein Schlachtschiff 1,8.

## Lücken und Vorbehalte

- Für Schrift, Siedlung, Kompass, Seekarten und Schiffsklasse Transporter fehlen die Kosten.
- Haupthaus-Kosten sind aus Stufe 20 zurückgerechnet (200 je Rohstoff × 1.2^(L−1)).
- Kronen stehen nicht im Tech-Tree. Kronenpreise stammen von der Regelseite.
- Bauzeiten im Tech-Tree sind gerundet und ohne Demokratie-Bonus (−15 %), Werft-, Kasernen- und Labor-Rabatt.
- Werte der Piratenschiffe «Large Pirate Ship» und «Mighty Pirate Ship» fehlen. Wandkanonen-HP wird nicht angezeigt.
- Der Kampfrechner prüft die Truppenkapazität nicht. In den Soldaten-Läufen trug ein kleiner Frachter tausende Soldaten.
- Kampfrechner-Ergebnisse sind Erwartungswerte; die echte Trefferquote schwankt je Runde um bis zu 10 Prozentpunkte.
- Bevölkerung und Arbeiter sind in der Build-Order nicht modelliert.
