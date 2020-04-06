---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor durchführt.
seo-title: Testreferenz
title: Testreferenz
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 78105ff6766f48f3aaccfeda281e5b4883be856a

---


# Testreferenz {#test-reference}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor durchführt.

**Aktuelle Testversion:** 1.0.5

Jeder Test wird gewichtet. Ihr Testergebnis entspricht der jeweiligen Gewichtung. Bei Bestehen eines Tests mit einer Gewichtung von fünf erhalten Sie fünf Punkte.

* 0: Zeigt Probleme auf, die Sie kennen sollten, aber sich nicht auf Ihr Ergebnis auswirken.
* 1: Empfiehlt eine Optimierung. Keine Auswirkung auf die Datengenauigkeit.
* 2: Bei Nichtbestehen dieses Tests erhalten Sie keinen Zugriff auf die neuesten Funktionen und Fehlerbehebungen in der Experience Cloud.
* 3: Tests zur Effizienz und zur Einhaltung der Best Practices bei der Implementierung.
* 4: Nichtbestehen bedeutet, dass Sie möglicherweise unzuverlässige Daten erfassen.
* 5: Nichtbestehen bedeutet, dass möglicherweise Datenverlust auftritt.

Die Tests werden entweder bestanden oder nicht bestanden. Während der Tests wird geprüft, ob die Testbedingungen erfüllt wurden oder nicht, sodass keine Abstufungsergebnisse für eine teilweise Erfüllung entstehen können. Wird bei einem Test beispielsweise die neueste Version einer Adobe-Lösung geprüft, erhalten Sie immer dasselbe Ergebnis – unabhängig davon, ob Sie nur eine oder fünf Version in Verzug sind. Die neuesten Versionen beinhalten Leistungsverbesserungen und Fehlerkorrekturen. Daher wird empfohlen, stets die neueste Version zu verwenden.

Es wird **dringend empfohlen**, Ergebnisse der Stufe 4 oder 5 zu korrigieren.

Es wird **empfohlen**, Ergebnisse der Stufen 1 bis 3 zu korrigieren.

## Welche Adobe-Technologien werden von Auditor bewertet? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID-Service (früher Marketing Cloud ID-Service)
* Target

Folgende Adobe-Lösungen sind derzeit nicht in der Testrubrik enthalten. Die Unterstützung für diese Lösungen ist für zukünftige Updates geplant.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch
