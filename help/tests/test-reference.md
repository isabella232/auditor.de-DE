---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor durchführt.
seo-title: Test-Referenz
title: Test-Referenz
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# Test-Referenz{#test-reference}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor durchführt.

**Aktuelle Testversion:** 1.0.5

Jeder Test wird gewichtet. Ihr Testergebnis entspricht der zugewiesenen Gewichtung. Wenn Sie einen Test mit einem Gewicht von fünf bestehen, erhalten Sie fünf Punkte.

* 0: Warnt Sie auf Probleme, die Sie kennen sollten, die sich jedoch nicht auf Ihr Ergebnis auswirken.
* 1: Empfiehlt eine Optimierung. Keine Auswirkung auf die Datengenauigkeit.
* 2: Wenn Sie diesen Test nicht durchführen, haben Sie keinen Zugriff auf die neuesten Funktionen und Fehlerbehebungen in der Experience Cloud.
* 3: Tests zur Effizienz und zur Einhaltung der Best Practices bei der Implementierung.
* 4: Fehler bedeutet, dass Sie möglicherweise unzuverlässige Daten erfassen.
* 5: Fehler bedeutet, dass möglicherweise Datenverlust auftritt.

Tests sind erfolgreich/fehlgeschlagen. Sie prüfen, ob die Prüfbedingungen eingehalten wurden oder nicht, sodass keine partiellen Ergebnisse für die teilweise Erfüllung vorliegen. Wenn der Test z. B. die neueste Version einer Adobe-Lösung prüft und Sie nur eine Version hinter sich haben, erhalten Sie das gleiche Ergebnis wie bei fünf Versionen. Die neuesten Versionen beinhalten Leistungsverbesserungen und Fehlerkorrekturen, daher wird empfohlen, die neueste Version zu verwenden.

Es wird **dringend empfohlen**, Ergebnisse der Stufe 4 oder 5 zu korrigieren.

Es wird **empfohlen**, Ergebnisse der Stufen 1 bis 3 zu korrigieren.

## Welche Adobe-Technologien werden von Auditor bewertet? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID-Dienst (früher Marketing Cloud ID-Dienst)
* Target

Die folgenden Adobe-Lösungen sind derzeit nicht in der Testrubrik enthalten. Die Unterstützung für diese Lösungen ist für zukünftige Updates geplant.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## Testkategorien {#section-630181db21ef4eec9ce6a13a0482bb55}

Diese Test-Referenz unterteilt die Tests in die folgenden Kategorien:
