---
description: Nachdem Sie einen Test ausgeführt haben, zeigt die Scorecard Informationen zu einem Audit an.
seo-description: Nachdem Sie einen Test ausgeführt haben, zeigt die Scorecard Informationen zu einem Audit an.
seo-title: Scorecard
title: Scorecard
uuid: a765cd6a-d3d6-4438-9621-d7899385a518
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Scorecard{#scorecard}

Nachdem Sie einen Test ausgeführt haben, zeigt die Scorecard Informationen zu einem Audit an.

Klicken Sie auf der Seite &quot;Prüfer&quot;auf den Namen Ihrer Prüfung, um die Ergebnisse Ihres Tests anzuzeigen.

![](assets/report.png)

Verwenden Sie die Scorecard, um zu sehen, wie die Prüfung in den folgenden Kategorien bewertet wurde:

* Gesamtbewertung
* Tag-Präsenz

   Wertet aus, ob das Tag vorhanden ist und ob es sich an der richtigen Stelle im Seiten-Code befindet.
* Tag-Konsistenz

   Wertet aus, ob die Tags über URLs hinweg konsistent sind.
* Konfiguration

   Wertet die Tags mit anderen Regeln und empfohlenen Best Practices aus.
* Warnhinweis

   Warnhinweise zeigen Probleme an, die Sie kennen sollten, die sich jedoch nicht auf Ihr Ergebnis auswirken.

Ihr Ergebnis hängt vom Gewicht jedes Tests ab und davon, ob Sie bestehen oder nicht. Wenn Sie den Test bestehen, erhöht sich Ihr Ergebnis um die Anzahl der Punkte, die der Teststärke entsprechen.

* 0: Warnt Sie auf Probleme, die Sie kennen sollten, die sich jedoch nicht auf Ihr Ergebnis auswirken.
* 1: Empfiehlt eine Optimierung. Keine Auswirkung auf die Datengenauigkeit.
* 2: Wenn Sie diesen Test nicht durchführen, haben Sie keinen Zugriff auf die neuesten Funktionen und Fehlerbehebungen in der Adobe Experience Cloud.
* 3: Tests zur Effizienz und zur Einhaltung der empfohlenen Best Practices bei der Implementierung.
* 4: Fehler bedeutet, dass Sie möglicherweise unzuverlässige Daten erfassen.
* 5: Fehler bedeutet, dass möglicherweise Datenverlust auftritt.

Die Scorecard listet alle Probleme der Stufe 4 oder 5 als **dringend empfohlen** auf.

Die Scorecard listet alle Probleme der Stufen 1 bis 3 **auf, die Sie beheben** sollten.

Klicken Sie auf **[!UICONTROL Bericht herunterladen]**, um eine Excel- oder PDF-Datei herunterzuladen, die die Informationen der Prüfung enthält.

Neben dem Ergebnis für jede Kategorie werden in der Scorecard alle empfohlenen oder empfohlenen Korrekturen sowie die Elemente aufgelistet, die den Test bestanden haben. Klicken Sie auf die einzelnen Ausgaben, um weitere Details im Feld auf der rechten Seite anzuzeigen. Klicken Sie erneut auf , um einen Drilldown durchzuführen und Empfehlungen zur Behebung des Problems anzuzeigen. Die folgende Tabelle zeigt die Details zu einer empfohlenen Ausgabe in der oben gezeigten Wertungsliste:

![](assets/report-issue-details.png)

Klicken Sie oben im Bildschirm auf die Kategorien, um die in den einzelnen Kategorien gefundenen Probleme anzuzeigen.

## Welche Seiten waren Teil des Tests? {#section-fd38ffeb868648e89c34c5772fa65f46}

Sie können Listen der URLs anzeigen, die Ihren Test bestanden oder fehlgeschlagen haben.

Klicken Sie in der Scorecard auf einen Testnamen oder auf den Link Alle **[!UICONTROL anzeigen]** unter jeder Kategorieüberschrift. Damit gelangen Sie zu den Details der Tests. Für jeden Test sehen Sie die Testbeschreibung und eine Liste aller URLs, die fehlgeschlagen sind und bestanden haben. Diese Informationen sind auch in heruntergeladenen Berichten enthalten.
