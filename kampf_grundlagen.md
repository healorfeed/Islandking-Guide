# Island King – Wie ein Kampf abläuft

Stand 10.10.2026 (Kampfkonzept 2.0). Quellen: Spielregeln, Update-Log vom 9.10., eigene Kampfrechner-Läufe.

## Die Rechenregel jeder Runde

- Beide Seiten feuern **gleichzeitig**. Ihr Schaden ist Gesamtangriff × Trefferquote.
- **Trefferquote:** 60 % Basis, plus 1 / 2 / 5 % je Stufe Standard / Fortgeschrittener / Royal Angriff (alles erforscht: 100 %). Sie schwankt je Runde um bis zu 10 Prozentpunkte.
- Der Schaden verteilt sich auf die gegnerischen Gruppen **im Verhältnis ihrer verbleibenden HP**. Nur ganze Einheiten fallen, der Rest bleibt als Vorschaden stehen.
- **Höchstens 6 Runden.** Steht danach auf beiden Seiten noch etwas, hat der Verteidiger gehalten.
- **Rückzug:** Hat der Angreifer in einer Phase 90 % seiner HP verloren, bricht er ab.
- **Befestigung:** Standard / Fortgeschrittene / Royal Verteidigung geben +1 / 2 / 5 % HP je Stufe, aber nur für Anlagen und Stadtmauer (max. +80 %).

Daraus folgt das **Quadratgesetz:** Stärke ≈ Gesamtangriff × Gesamt-HP. Eine doppelt so große Armee ist viermal so stark, und eine Mischung aus angriffs- und HP-starken Einheiten schlägt eine einseitige Armee gleichen Werts.

## Ein Inselangriff hat zwei Phasen

### Phase 1: Seeschlacht

| Angreifer | Verteidiger |
|---|---|
| alle Schiffe der Flotte | Schiffe im Hafen (auch aufgelegte und stationierte Gäste) |
| | See-Anlagen: Wachturm, Küstenkanone, Kanonenturm, Wasserblockade |

Ausgang:
- **Verteidiger hält** (seine Schiffe oder Anlagen stehen nach 6 Runden noch): Der Angriff ist abgewehrt. Es gibt keine Landung und keine Beute.
- **Eine Wasserblockade überlebt:** keine Landung und keine Beute, selbst wenn alles andere fällt.
- **See frei, aber keine Truppen an Bord:** Der Angreifer füllt 25 % seines Laderaums (Hafenplünderung) und fährt heim.

### Phase 2: Landung (nur wenn die See frei ist und Truppen an Bord sind)

| Angreifer | Verteidiger |
|---|---|
| Soldaten | Soldaten der Insel |
| Schiffe mit 75 % ihres Angriffs (Bombardement), sie werden dabei mitgetroffen | Land-Anlagen: Wachturm, Katapult, Kanonenturm |
| | Stadtmauer (0 Angriff, 30'000 HP) und Wandkanonen (20'000 Angriff) |

Ausgang:
- **Landsieg:** volle Plünderung. Geschützt bleiben 8 Stunden eigener Produktion je Rohstoff (mindestens 500), danach gilt 24 Stunden eine Plündersperre.
- **Landung verloren:** nur die 25 % Hafenplünderung.

### Nach dem Landsieg
- **Gebäude-Bombardement:** 10 % der verbliebenen Kraft schlagen in Gebäude ein (Schiffe mit 75 %, Soldaten voll). Jede Gebäudestufe hat HP = Baukosten / 100. Reicht die Kraft, fällt das Gebäude eine Stufe. Das sind höchstens 1 Stufe je Gebäude, 3 je Angriff und 6 je Insel und Tag. Haupthaus, Siedlungen und Verteidigungsgebäude sind ausgenommen. Der Angreifer wählt den Schwerpunkt: Produktion, Militär oder Wirtschaft.
- **Eroberung:** Sie braucht ein überlebendes Kolonieschiff und eine Garnison von 1 Soldat je Gebäudestufe der Insel (mindestens 50). Die Hauptinsel ist geschützt, solange man höchstens 3 Inseln hat.

### Nach jedem Kampf
- 40 % der zerstörten Schiffe werden als reparierbare Wracks geborgen, 40 % der gefallenen Soldaten kommen verwundet ins Lazarett. Beschädigte Schiffe gehen ins Dock. Reparatur und Heilung kosten Rohstoffe.
- **Trümmerfeld:** Sinken mindestens 5 Schiffe, kehren 6 Stunden lang später ablegende fremde Angriffe ohne Kampf um.

## Flotten entern (eigener Angriffstyp)

- Ziel sind die Schiffe im Hafen einer Insel. Voraussetzung ist Kampfschiff 10 und Soldaten an Bord.
- Ablauf: Erst feuert eine Salve der Schiffe auf Hafenschiffe und See-Anlagen. Dann kämpfen die Soldaten an Bord gegen die **Garnison der Insel, soweit sie auf die Hafenschiffe passt**.
- Bei Sieg wechselt die Hälfte der überlebenden Hafenschiffe den Besitzer, die wertvollsten zuerst.
- **Eine Flotte ohne Soldaten im Hafen ist Beute.** Schutz bieten Soldaten als Garnison oder das Auflegen in der Werft: 10 Schiffe je Werftstufe, aufgelegte Schiffe sind nicht enterbar, kämpfen bei einem Inselangriff aber mit.

## Was soll man bauen? (Strategie)

Grundsatz: Ein Krieg ist ein Abnutzungskrieg. Schaden bleibt stehen, man kann immer wieder angreifen. Es gewinnt, wer pro Rohstoff mehr vom Gegner zerstört, als er selbst verliert. Die Kennzahl dafür ist √(Angriff × HP) / Kosten.

1. **Erst Wirtschaft:** Holz, Stein und Gold auf 34, Reichtum 20, genug Lager (Grosslager). Die Kohlemine (~28) erst, wenn die Insel militärreif werden soll, denn Kohle braucht nur das Militär. Neue Inseln von einer ausgebauten Insel beliefern (siehe build_order.pdf).
2. **Dann pro Insel dauerhaft:** Schlachtschiff und Fregatte im Wechsel (bis Royal Angriff 5 nur Fregatten), alles Übrige in Küstenkanonen. Gold ist dabei der Engpass. **Schwertkämpfer nicht auf Vorrat**, sondern erst kurz vor einem Angriff ausbilden (500 je Fregatte, ~22 h): Jeder Soldat zählt 1 Punkt, und zu viele Punkte verschieben das Bashing-Fenster gegen dich. Eine kleine Garnison nur dort, wo Schiffe unaufgelegt im Hafen liegen.
3. **Flotte und Soldaten sammeln:** Alles auf die Hauptinsel verlegen und dort in der Werft auflegen (nicht enterbar, kämpft trotzdem mit). Was nicht hineinpasst, schützt die Garnison aus Schwertkämpfern.
4. **Kolonien** verteidigen sich mit Küstenkanonen und Wachtürmen, ohne eigene Flotte.
5. **Angreifen nur schwache Ziele und mit voller Macht.** Für Beute große Frachter mitnehmen, für Landung und Eroberung die Schwertkämpfer auf den Fregatten.

### Warum gesammelt und nicht verteilt? Eine Simulation

Kampfmodell nachgebaut und gegen den Kampfrechner geprüft (5 von 5 Fällen auf ±1 Einheit genau). Zwei Spieler mit je 4 ausgebauten Inseln und gleichem Budget bauen 60 Tage lang (~178 Mio. Wert je Spieler):
- **A «verteilt»:** zuerst 50 Schlachtschiffe pro Insel aufgelegt, danach Mix, Rest Küstenkanonen. Ergebnis pro Insel 50 SS + 207 KK, mobil 20 SS + 20 F.
- **B «gesammelt»:** von Anfang an SS/F 1:1 auf der Hauptinsel, Rest Küstenkanonen. Ergebnis pro Insel 277 KK, mobil 120 SS + 120 F.

| Seeschlacht | Verlust Angreifer | Verlust Verteidiger |
|---|---|---|
| B greift eine A-Kolonie an | 20 Mio. | 40 Mio. |
| A greift mit allen Schiffen eine B-Kolonie an | 13 Mio. | 20 Mio. |
| A greift mit allem die B-Hauptinsel an | 117 Mio. | 77 Mio. |
| B greift A an, nachdem A alles gesammelt hat | 98 Mio. | 54 Mio. |

- Verteilte Schiffe werden einzeln abgeholt. Gesammelte Schiffe sind auch in der Verteidigung am stärksten.
- Auf einer Kolonie bringen Küstenkanonen für denselben Wert mehr als Schlachtschiffe (Angreifer verliert 29 statt 20 Mio.).
- Gut befestigte Hauptinseln anzugreifen kostet den Angreifer mehr als den Verteidiger.

Vereinfachungen: nur Seeschlacht, keine Kohle-Grenze, Kronen als 200 Gold + 70 Kohle bewertet.
