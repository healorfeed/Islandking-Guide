# Island King – TLDR

Stand 10.10.2026, nach dem Kampfkonzept 2.0. Die Werte stammen aus dem Spiel (Spielregeln, Tech-Tree, Kampfrechner), die Auswertung ist mit Claude gemacht. Fehler sind möglich.

Die Rohdaten liegen im Ordner [`rohdaten`](rohdaten), falls jemand selbst weiterrechnen will, zum Beispiel ebenfalls mit Claude. Es fehlen noch: die Werte der anderen Stromgebäude (Kohlekraftwerk, Tretmühlen, Vulkan-Kraftwerk), wie sich Reparaturkosten genau berechnen, wie Bevölkerung und Arbeiter die Produktion beeinflussen und was Kolonisation über Stufe 5 bewirkt.

## Dateien

Alles zusammen herunterladen: oben auf GitHub «Code» → «Download ZIP».


| Datei | Inhalt |
|---|---|
| [`islandking_daten.ods`](islandking_daten.ods) | Kosten und Bauzeit jeder Stufe, Einheiten mit Kampfkraft pro Rohstoff, Minenförderung, Kampfrechner-Ergebnisse, Flottenmix-Rechner |
| [`techtree.pdf`](techtree.pdf), `techtree_1–4.png` | Was worauf aufbaut, mit Stufen |
| [`build_order.pdf`](build_order.pdf) | Reihenfolge des Ausbaus mit Kosten und Dauer |
| [`kampf_grundlagen.md`](kampf_grundlagen.md) | Ablauf von See- und Landkampf, Entern, Strategie, Simulation |
| [`was_nicht_bauen.md`](was_nicht_bauen.md) | Anfängerfallen im Detail |
| [`rohdaten/`](rohdaten) | Alle Messwerte als CSV/JSON, Übersicht in `notes.md` |

## Die Kernerkenntnisse

1. **Reichtum 20 zuerst.** +60 % auf alle Rohstoffe auf allen Inseln, nichts bringt mehr.
2. **Erst Produktion, dann Militär.** Kosten und Förderung einer Mine wachsen beide ×1.2 pro Stufe. Jede Minenstufe hat ihre Kosten nach ~6 Tagen wieder eingespielt, bis Stufe 34. Holz, Stein und Gold auf 34, dann die Kohlemine (Kohle braucht nur das Militär), dann die wenigen Militärgebäude. Schon ein dauerhafter Schiffbau braucht fast volle Minen. Der Engpass ist dabei Gold, nicht Kohle.
3. **Neue Inseln beliefern.** Eine neue Insel fördert anfangs 26 pro Stunde. Mit ~16 großen Frachtern Lieferung pro Tag erreicht sie Minen 34 nach ~17 statt ~39 Tagen. Begrenzt wird das durch Frachtraum und das Lager der neuen Insel.
4. **Kampf: Stärke ≈ Gesamtangriff × Gesamt-HP.** Beide Seiten schießen gleichzeitig, der Schaden verteilt sich nach HP. Doppelt so viele Einheiten sind etwa viermal so stark. Daraus folgt:
   - **Flotte sammeln.** Verteilte Schiffe werden einzeln abgeholt. In einer Simulation verliert der Verteiler doppelt so viel wie der Angreifer.
   - **Mischen.** Schlachtschiffe (Angriff) und Fregatten (billige HP) gemischt sind ~14 % stärker als gleich teure reine Schlachtschiffe.
5. **Die Seeschlacht entscheidet.** Gelandet wird nur, wenn die See frei ist und Truppen an Bord sind. Wer die See hält, braucht keine Landabwehr. Küstenkanonen sind dafür pro Rohstoff stärker als jedes Schiff und bekommen durch Forschung bis +80 % HP. Untätige Schiffe in der Werft auflegen: nicht enterbar, kämpfen trotzdem mit.
6. **Soldaten braucht nur der Angreifer.** Ohne Landsieg gibt es nur 25 % Beute, keine Eroberung, kein Entern. Nur der Schwertkämpfer lohnt sich. Wegen 1 Punkt je Soldat bildet man ihn erst kurz vor einem Angriff aus (500 je Fregatte).
7. **Viele Inhalte sind Anfängerfallen.** Musketier, Kanonier und Ritter sind pro Rohstoff um ein Vielfaches schwächer als der Schwertkämpfer. Kampftechniken über 12 und Verteidigungstechniken über 10 schalten fast nur diese frei (~20 Mio. Rohstoffe). Hohe Siedlungs- und Windmühlenstufen sind viel teurer als Grosslager und Wasserkraftwerk.

## Balancing-Wünsche

### 1. Punktesystem überarbeiten (wichtigster Punkt)
Jede Einheit zählt 1 Punkt, jede Gebäudestufe 2, jede Forschungsstufe 3, egal was sie kostet. Ein einfacher Soldat (205 Rohstoffe) und ein Schlachtschiff (375'000 + 500 Kronen) zählen gleich viel. Pro Rohstoff bringt der Soldat rund 1'800-mal so viele Punkte. Stufe 1 und Stufe 34 einer Mine zählen ebenfalls gleich, obwohl Stufe 34 rund 400-mal so viel kostet.

Punkte steuern aber Bashing-Schutz (1/5), Anfängerschutz (500 Punkte) und die Stationierungsgrenze bei Verbündeten. Wer in eine starke Flotte investiert, wirkt klein und darf mehr Spieler angreifen. Wer billige Einheiten sammelt, wirkt groß. Die Stationierungsgrenze rechnet schon heute mit 2'000 Rohstoffen je Punkt, die Punkte selbst tun das nicht.

**Vorschlag:** Punkte = investierte Rohstoffe / 2'000, für Gebäude, Forschung und Einheiten gleich. Optional getrennt anzeigen: Wirtschaft, Forschung, Militär.

### 2. Sackgassen überarbeiten
Musketier, Kanonier und Ritter sind so schwach, dass man sie nie bauen sollte. Damit sind auch Kampftechniken über 12 und Verteidigungstechniken über 10 fast wertlos. Wer das nicht nachrechnet, investiert Millionen in nichts.

**Vorschlag:** Die drei Soldaten über HP oder Kosten so aufwerten, dass sie eine eigene Rolle haben (z. B. Ritter als HP-Puffer, Kanonier als Schadensspitze), und die Zwischenstufen der Forschungen mit eigener Wirkung versehen.

### 3. «Winning means winning harder» entschärfen
Alles im Spiel wächst exponentiell: Minen zahlen sich auf jeder Stufe in ~6 Tagen zurück, jede neue Insel finanziert die nächste, und Kampfkraft steigt im Quadrat zur Armeegröße. Wer vorne liegt, wächst am schnellsten. Eine Allianz, die einmal davongezogen ist, holt niemand mehr ein.

**Mögliche Gegengewichte:**
- Unterhalt für große Flotten (z. B. Kohle oder Gold je Schiff und Tag)
- Steigende Kosten für jede weitere Insel (Kolonieschiff, Ausbau)
- Aufholbonus auf die Produktion für Spieler deutlich unter dem Durchschnitt
- Beute und Eroberung gegen deutlich Kleinere stärker begrenzen
