---
description: Häufige Fragen und Antworten zum Adobe Experience Platform Auditor
seo-description: Häufige Fragen und Antworten zum Adobe Experience Platform Auditor
seo-title: Häufig gestellte Fragen zu Adobe Experience Platform Auditor
title: Häufig gestellte Fragen zu Adobe Experience Platform Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 71%

---


# Häufig gestellte Fragen zu Adobe Experience Platform Auditor{#auditor-faq}

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zu Adobe Experience Platform Auditor.

* [Was ist Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Ist meine Firma berechtigt, Platform Auditor zu verwenden?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Welche Adoben werden vom Plattformprüfer bewertet?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Wie viele Prüfungen kann ich durchführen?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Was wird für eine Prüfung durchsucht?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Wie lange dauert eine Prüfung?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Welche Informationen enthält ein Bericht?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Wie umsetzbar sind diese Informationen?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Kann der Plattformprüfer die Nicht-Adobe-Technologie prüfen?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Kann ich meine IP-Adressen genehmigen, um das Prüfen von Seiten zuzulassen…](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Verwendet Platform Auditor dieselben IP-Bereiche wie Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Was ist Adobe Experience Platform Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor ist ein Dienst der Adobe Experience Cloud, der gemeinsam mit ObservePoint, Experten für die Validierung digitaler Implementierungen, entwickelt wurde.

Mit Platform Auditor können Kunden bis zu 500 Webseiten gleichzeitig scannen und einen Bericht erhalten, der zeigt, wie sie ihre Adobe Experience Cloud-Implementierungen verbessern können, damit sie den vollen Nutzen aus ihrer Adobe ziehen können.

## Am I eligible to use Platform Auditor? {#section-f90094050d1e44929066a942833435cf}

Alle Adobe Experience Cloud-Kundenorganisationen erhalten kostenlosen Zugriff auf Platform Auditor (ab 1. Mai 2018). Jeder Benutzer muss die Nutzungsbedingungen von Adobe/ObservePoint in der Benutzeroberfläche von Adobe Experience Cloud akzeptieren, bevor auf die Funktion zugegriffen werden kann. Wenden Sie sich an Ihren Kundenbetreuer, um die Bedingungen abzuwählen.

## How do I access Platform Auditor? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Platform Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. Sie können auch direkt zu [https://auditor.adobe.com](https://auditor.adobe.com) gehen.

## Which Adobe technologies does Platform Auditor grade? {#section-52833b71c05448aaae508e6070a387f5}

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
* Adobe Experience Platform Launch

## Wie viele Prüfungen kann ich durchführen? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Die Zahl der Prüfungen, die Sie durchführen können, ist nicht beschränkt. Benutzer können jeweils nur eine Prüfung zur selben Zeit durchführen. Wenn Sie versuchen, eine Prüfung mit denselben Einstellungen wie die bereits ausgeführte zu starten, tritt ein Fehler auf.

## Was wird für eine Prüfung durchsucht? {#section-6d068ed69ece4a1bb6d0c34454550c45}

Die ObservePoint-Technologie durchsucht derzeit URLs, die in Dokumentlinks enthalten sind. In Schaltflächen, Paginierungs-Widgets und anderen solchen Seitenelementen gefundene Links werden nicht durchsucht.

## How do I suggest new criteria for Platform Auditor tests? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Platform Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Wie lange dauert eine Prüfung? {#section-5086ae27ef1f4671a9d951348654633a}

Es gibt viele Faktoren, die dazu beitragen, dass eine Prüfung abgeschlossen werden kann, unter anderem:

* Seitenladezeit

   Die ObservePoint-Engine lädt jede Seite der Prüfung in einem Browser. Je schneller eine Seite geladen wird, desto schneller erfolgt die Prüfung.
* Gleichzeitige Verbindungen

   Platform Auditor verwendet eine einzelne Verbindung, um jede Seite zu besuchen. Vollständige ObservePoint-Konten verwenden bis zu 10 Engines gleichzeitig.
* Netzwerkstille

   Nachdem jede Seite geladen wurde, wartet die Prüfung auf eine Netzwerkstille von sieben Sekunden, bevor die nächste Seite aufgerufen wird. Wenn eine Seite viele Netzwerkanforderungen sendet, die nach dem Laden der Seite auftreten, tritt nach 60 Sekunden ein Timeout für die Wartezeit auf.
* Erneute Seitenverbindungsversuche

   Wenn eine Seite oder ein Tag nicht gefunden werden kann, speichert die Prüfung diese URL und kehrt später in der Prüfung dazu zurück. Die Prüfung besucht eine Seite bis zu dreimal, um sicherzustellen, dass der Fehler nicht durch ein vorübergehendes Problem verursacht wurde.
* Verarbeitung

   Nachdem eine Prüfung ausgeführt wurde, werden alle erfassten Daten verarbeitet und durch die Regeln gefiltert. Diese Verarbeitung nimmt sehr viel Zeit in Anspruch, allerdings nicht so viel wie die Prüfung selbst.

>[!NOTE]
>
>Platform Auditor führt jeweils eine einzige Prüfung aus. Vollständige ObservePoint-Konten können viele Prüfungen nacheinander ausführen.

## Welche Informationen enthält ein Bericht? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Bei jeder Prüfung wird ein Bericht generiert, der anzeigt, welche URLs geprüft, welche Probleme auf diesen Webseiten gefunden wurden und wie die gefundenen Probleme zu beheben sind.

Die Ergebnisse von Prüfungen werden in drei Kategorien unterteilt:

* Konfiguration
* Tag-Konsistenz
* Tag-Präsenz

Zusätzlich zu diesen drei Kategorien enthält der Bericht Warnungen mit Informationen, die Sie kennen sollten, die jedoch nicht unbedingt sofortiges Handeln erfordern.

Die Empfehlungen, die in diese Kategorien fallen, werden dann in drei weitere Kategorien unterteilt:

* Dringend empfohlen
* Empfohlen
* Bestanden

## Wie umsetzbar sind diese Informationen? {#section-9308c1ea882048b781087ae6d2eee9f0}

Alle Empfehlungen von Platform Auditor sollen Ihnen dabei helfen, ein Problem bei der Implementierung von Adobe Experience Cloud-Lösungen wie DTM oder Zielgruppe zu beheben. Um dies zu erleichtern, hat das Plattformprüfungsteam intensiv daran gearbeitet, sehr detaillierte Anweisungen darüber zu geben, was dort getan werden muss. Sie können eine Tabelle mit allen geprüften URLs und allen Testergebnissen exportieren, um problematische Bereiche einfach zu identifizieren. Hier ein Beispiel für eine Empfehlung zur DTM-Implementierung:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom callback last</b> </p> <p>Für eine korrekte DTM-Implementierung ist die Funktion „_satellite.pageBottom()“ erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden „&lt;/body&gt;“-Tag hinzu, um die ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Can Platform Auditor audit non-Adobe technology? {#section-f6e73c56083b4815bbf901296038bcd4}

Nein. Das vollständige Angebot von ObservePoint ermöglicht es Kunden jedoch, alle Marketing-Tags und -Technologien zu prüfen und zu überwachen. Als Adobe-Kunde haben Sie Zugriff auf ein kostenloses Testkonto. To access your trial account visit [ObservePoint’s Platform Auditor Page](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## Kann ich meine IP-Adressen genehmigen, um das Prüfen von Seiten zuzulassen, die durch Anmeldedaten geschützt sind? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Diese Funktion wird derzeit ohne das vollständige ObservePoint-Angebot nicht unterstützt.

## Does Platform Auditor use the same IP ranges as ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

Das Durchsuchen wird von ObservePoint ausgeführt, sodass dieselben IP-Adressen verwendet werden.

Weitere Informationen finden Sie in der [ObservePoint-Dokumentation](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list).
