# Improved Siegeengines

**Version**: 1.0.29

Die Belagerungsgeräte der KI verschwenden sich im Originalspiel selbst: Katapulte rollen bis direkt vor Mauern, die sie aus der Ferne hätten treffen können, Belagerungszelte wandern in langen Spielen immer weiter weg, bis Triboke nichts mehr erreichen, Belagerungstürme stehen untätig herum und warten auf eine aus KI-Sicht passende Mauer, und tragbare Schilde laufen Rehen hinterher. Dieses Modul behebt jedes dieser Probleme.

Alle folgenden Punkte lassen sich einzeln ein- oder ausschalten. Verändert werden die Belagerungsgeräte der KI – mit Ausnahme des Andockens und Mitfahrens auf Belagerungstürmen sowie der Öl-Baumeister, die auch dem Spieler zugutekommen.

## Funktionen

**Katapulte und Triboke wählen eigene Ziele.** Ein KI-Katapult oder -Tribok sucht rundum innerhalb seiner vollen Wurfweite nach der nächsten feindlichen Mauer, dem nächsten Turm oder Torhaus und feuert von seinem Standort aus. Zivile Gebäude werden erst beschossen, wenn keine Befestigung mehr in Reichweite ist. Es fährt nur näher heran, wenn gar nichts in Reichweite liegt. (Die spielinterne Suche prüft nur eine Richtung auf einmal und ignoriert bereits angeschlagene Mauern, weshalb Katapulte früher bis direkt vor die Mauer fuhren.)

**Katapulte und Triboke halten unterwegs zum Schießen an.** Das Originalspiel sucht nur im Stillstand nach Zielen, sodass KI-Katapulte bei Überfällen, auf dem Marsch oder beim Vorrücken an allem in Reichweite vorbeifuhren. Nun schaut sich ein fahrendes KI-Katapult oder ein Tribok regelmäßig rundum um und hält zum Feuern an, sobald eine feindliche Mauer, ein Turm, ein Torhaus oder ein Gebäude in Reichweite kommt.

**Weiter zum nächsten Gegner.** Ein Katapult oder Tribok zielt nur auf den Spieler, gegen den seine Armee geschickt wurde. Sobald dieser besiegt ist (sein Lord ist tot), beschießt es jeden anderen Feind in Reichweite, statt untätig stehen zu bleiben.

**Andere Feinde in Reichweite.** Ist nichts vom eigentlich belagerten Spieler in Reichweite, beschießt ein Katapult oder Tribok Mauern und Gebäude anderer Feinde in Reichweite, statt an ihnen vorbeizurollen. Ziele des belagerten Spielers behalten stets Vorrang; bereits zerstörte Gebäude werden nie anvisiert.

**Kein Schießen mehr auf Ruinen.** Ein auf ein Gebäude zielendes Belagerungsgerät – eine Feuerballiste auf ein brennbares Ziel oder ein manuell beordertes Katapult – feuerte nach der Zerstörung weiter auf den leeren Platz und wechselte nie das Ziel, weil das Spiel nur die Gebäudenummer prüfte. Nun wird ein zerstörtes Ziel aufgegeben und ein neues gewählt. Das gilt auch für Feuerballisten.

**Bessere Treffgenauigkeit.** Im Originalspiel weichen Steine eines KI-Katapults bis zu 12 Felder zu kurz und 6 zur Seite ab, sodass auf lange Distanz die meisten ins freie Feld vor der Mauer fallen. Die Streuung wird halbiert und auf das Ziel zentriert (einstellbar; 100 % belässt das Originalverhalten). Deine eigenen Geräte bleiben unverändert.

**Zeltplätze werden wiederverwendet.** Sobald die Truppe des Platzes weg ist, nichts mehr darauf steht und kein feindlicher Soldat ein Gerät dort angreifen kann, darf die KI dort wieder ein neues Zelt errichten. Im Originalspiel blieb jeder Platz für den Rest des Spiels gesperrt.

**Zelte für Fernkampfgeräte nach Reichweite.** Zelte für Katapulte, Triboke und Feuerballisten werden so platziert, dass das Gerät die Burg erreicht: 0 bis 10 Felder (einstellbar) innerhalb der Reichweite ab feindlichen Mauern, Türmen und Torhäusern, damit auch Ziele im Burginneren getroffen werden.

**Baumeister erreichen immer ihr Zelt.** Ist der Eingang eines Zelts blockiert, wandert er auf eine freie Seite; Baumeister, die aufgegeben haben oder feststecken, werden erneut geschickt, unterstützt von untätigen Baumeistern in der Nähe. Ein völlig eingemauertes Zelt erhält seine Baumeister, sobald sich ein Weg öffnet.

**Belagerungstürme docken an mehr Mauern an.** Findet das Spiel keinen Anlegeplatz, dockt ein Turm mit der Ecke an einer diagonalen Mauer oder bis zu drei Felder weiter entlang derselben Mauer an.

**KI-Belagerungstürme suchen selbst eine Mauer.** Ein untätiger KI-Turm fährt zur nächsten erreichbaren feindlichen Mauer (im Umkreis von 100 Feldern). Gibt es keine oder kommt er nicht durch, begleitet er die Armee wie ein großer Schild – erst mit Patrouillen, sonst mit dem Belagerungsschutz, sonst mit der Hauptarmee, sonst mit einer zufälligen Fernkampfgruppe und zuletzt mit den Reservetruppen.

**Fußsoldaten fahren auf Belagerungstürmen mit.** Wähle Fußsoldaten und klicke auf einen deiner Belagerungstürme: Bis zu 9 steigen oben auf und fahren mit; Bogenschützen und andere Fernkämpfer schießen sogar während der Fahrt und sind oben so geschützt wie auf einem angedockten Turm. Während der Fahrt sind sie nicht auswählbar; sie sterben mit dem Turm oder stehen nach dem Andocken darauf. Wähle den Turm und klicke zum Aussteigen: Der erste Klick setzt die Passagiere ab, der zweite die Baumeister. KI-Türme nehmen eigene Fernkämpfer im Umkreis von 3 Feldern mit.

**Schilde begleiten eigene Truppen.** KI-Schilde rücken gleichmäßig verteilt zu Grabenaushebern, den angreifenden Fernkampf-Belagerungsgeräten (nie zu den heimischen Verteidigungsgeräten) und den Fernkämpfern aus. Reservetruppen erhalten erst Schilde, wenn sonst niemand mehr da ist; ohne Truppen wartet ein Schild an Ort und Stelle.

**Öl-Baumeister gießen nur auf Boden.** Baumeister – auch deine – gießen Öl nur dort aus, wo es brennen kann: auf offenem Boden, niemals auf Mauern, Treppen oder Türmen, wo es früher wirkungslos verpuffte. Selbstständig gießen sie nur auf Feinde auf solchem Boden. Auf ungeeignetes Gelände geschickt, gießt der Baumeister auf den nächsten Boden im 45-Grad-Winkel oder behält das Öl mit „unmöglicher Ort“.

**Öl breitet sich nach Menge aus.** Ein Ölkessel bedeckt eine feste Anzahl Felder (standardmäßig 41) ab dem Zielpunkt. Auf offenem Boden entspricht das exakt dem Originalspiel; in engen Durchgängen wirkt es wie mehrere Kessel hintereinander. Brennbare Gebäude (von Hütten bis Waffenkammer, Kirche und Kathedrale) verlieren dort bis zu ein Drittel ihrer Lebenspunkte; Mauern, Türme, Torhäuser und Bergfriede bleiben unversehrt.

## Gut zu wissen

* Früher übernahm Smarter Walls das diagonale Andocken. Nutze Smarter Walls ab Version 1.0.16 zusammen mit diesem Modul – ältere Versionen ändern dieselbe Spielstelle und geraten sich in die Quere.
* Im Mehrspielermodus benötigt jeder dieses Modul mit denselben Einstellungen.
* In Spielständen wird nichts gespeichert.
