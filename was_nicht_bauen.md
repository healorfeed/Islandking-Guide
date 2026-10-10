# Island King – Was man nicht (oder nur bis zu einer Stufe) bauen sollte

Stand 10.10.2026. Grundlage: Kosten aus dem Tech-Tree (`islandking_daten.ods`), Wirkungen aus Spielregeln und Gebäudebeschreibungen. Alle Kosten wachsen ×1.2 pro Stufe. Wo eine Wirkung pro Stufe fest bleibt, bringen die oberen Stufen zwar weiterhin etwas, aber immer weniger pro Rohstoff. Entscheidend ist der Vergleich: Man baut immer das, was gerade am meisten pro Rohstoff bringt.

## Lager: Grosslager statt hoher Siedlungsstufen

Das Grosslager liefert pro Stufe 50'000 × 1.2^(L−1) Lager und kostet 240'000 × 1.2^(L−1). Das sind **0,21 Lagerplatz je Rohstoff, auf jeder Stufe gleich.**

| Gebäude | Lager je Stufe | lohnt sich bis Stufe | danach ist das Grosslager besser |
|---|---|---|---|
| Kleine Siedlung | +1'000 | ~11 | Stufe 11→50 kostet 34,6 Mio. für +40'000 Lager |
| Mittlere Siedlung | +3'000 | ~13 | |
| Große Siedlung | +8'000 | nie | nur bis Stufe 3 (Voraussetzung Grosslager) bzw. 5 (Münzprägerei) |

Vorbehalt: Ob Siedlungen zusätzlich Bevölkerung bzw. Arbeiter liefern, ist nicht gemessen. Die Beschreibungen nennen nur Lager.

## Strom: Wasserkraftwerk statt hoher Windmühle

- Windmühle: +20 Strom je Stufe, kostet 26 × 1.2^(L−1) je Strompunkt.
- Wasserkraftwerk: +100 Strom je Stufe, kostet 38 × 1.2^(L−1) je Strompunkt (plus 5 Kronen).
- Das Wasserkraftwerk ist günstiger, sobald seine Stufe 2 oder mehr unter der Windmühle liegt. Windmühle 20→40 (3,7 Mio.) lohnt sich praktisch nie.
- **Kohlekraftwerk meiden:** Es verbrennt 2 Kohle je Stufe und Stunde, und Kohle ist der Engpass für das ganze Militär.

## Forschung: tote Stufen

| Forschung | sinnvolles Ziel | warum nicht weiter |
|---|---|---|
| Kampftechniken | **12** (Küstenkanone, Katapult) | 15→45 kostet 14,6 Mio. und schaltet nur Kanonier und Ritter (40) frei, beide pro Rohstoff schwach, sowie den Kanonenturm (45), der schwächer ist als die Küstenkanone |
| Verteidigungstechniken | **10** (Spähposten, Schwertkämpfer ab 8) | 15→45 kostet 4,9 Mio. für Ritter (20) und Kanonenturm (45) |
| Kolonisation | **5** (Kolonieschiff) | Stufe 6–35 (2,7 Mio.): Wirkung unbekannt. Möglicherweise begrenzt sie die Zahl der Inseln, das ist nicht geprüft |
| Terraforming / Gaia | erst bei Platzmangel | Gaia gibt +100 Bauplätze je Stufe. Solange eine Insel genug Bauplätze hat, bringt das nichts. Jede Gaia-Stufe kostet zusätzlich 250 Kronen (= 50'000 Gold + 17'500 Kohle) |

Gut investiert sind dagegen: **Reichtum** (+3 % Produktion je Stufe), **Angriffsforschungen** (+1/2/5 % Trefferquote für alles), **Verteidigungsforschungen** (+1/2/5 % HP für Anlagen und Stadtmauer) und **Handel 20** (Laderaum ×2, Fregatte).

## Militärgebäude: nur so weit wie nötig

- **Werft:** Jede Stufe gibt nur −1 % Schiffbauzeit, aber +10 Auflegeplätze. Bis ~20 (200 Plätze) sinnvoll. Stufe 20→35 kostet 10,4 Mio., die letzte Stufe allein 1,85 Mio. für 1 % Bauzeit.
- **Kaserne:** −1,5 % Ausbildungszeit je Stufe. Stufe 1→20 kostet 1,1 Mio. Das lohnt sich nur, wenn die Ausbildungszeit wirklich begrenzt (sehr viele Soldaten pro Tag).
- **Wandkanonen:** 20'000 Angriff, aber nur in der Landung, und sie brauchen Royal Angriff 8 und Royal Verteidigung 8 (zusammen rund 50 Mio. Forschung, gut 38 Mio. davon zusätzlich, wenn Royal Angriff 5 schon steht, plus 1,9 Mio. Baukosten). Lohnt sich höchstens ganz am Ende.

## Einheiten, die man nicht bauen sollte

- **Ritter, Kanonier, Musketier:** pro Rohstoff deutlich schwächer als der Schwertkämpfer (Ritter ~11-mal).
- **Leichte Galeere, alte Piratenschiffe:** schwach, und gegen jede Anlage verloren.
- **Kleine Frachter** nur für Lieferungen. Für Beute nimmt man große Frachter.
- **Wasserblockade:** pro Rohstoff schwach im Kampf, braucht Royal 10/10. Ihr Nutzen ist allein die Hafensperre.
