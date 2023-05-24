---
description: Häufige Fragen und Antworten zum Adobe Experience Platform Auditor
seo-description: Common questions and answers about Adobe Experience Platform Auditor
seo-title: Adobe Experience Platform Auditor FAQ
title: Häufig gestellte Fragen zu Adobe Experience Platform Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
exl-id: 75ab4497-5822-4f64-9b6d-6cbf13687e8d
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 100%

---

# Häufig gestellte Fragen zu Adobe Experience Platform Auditor{#auditor-faq}

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zu Adobe Experience Platform Auditor.

* [Was ist Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Ist mein Unternehmen berechtigt, Platform Auditor zu verwenden?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Welche Adobe-Technologien werden von Platform Auditor bewertet?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Wie viele Prüfungen kann ich durchführen?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Was wird für eine Prüfung durchsucht?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Wie lange dauert eine Prüfung?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Welche Informationen enthält ein Bericht?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Wie umsetzbar sind diese Informationen?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Kann Platform Auditor Nicht-Adobe-Technologie prüfen?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Kann ich meine IP-Adressen genehmigen, um das Prüfen von Seiten zuzulassen?](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Verwendet Platform Auditor dieselben IP-Bereiche wie ObservePoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Was ist Adobe Experience Platform Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor ist ein Service der Adobe Experience Cloud, der gemeinsam mit ObservePoint – den Experten für die Validierung digitaler Implementierungen – entwickelt wurde.

Mit Platform Auditor können Kunden bis zu 500 Webseiten gleichzeitig prüfen und einen Bericht erzeugen, der zeigt, wie sie ihre Adobe Experience Cloud-Implementierungen verbessern können, sodass sie das gesamte Potenzial ihrer Adobe-Investition nutzen können.

## Bin ich berechtigt, Platform Auditor zu verwenden? {#section-f90094050d1e44929066a942833435cf}

Alle Adobe Experience Cloud-Kundenorganisationen erhalten (ab 1. Mai 2018) kostenlosen Zugriff auf Platform Auditor. Jeder Benutzer muss die Nutzungsbedingungen von Adobe/ObservePoint in der Benutzeroberfläche von Adobe Experience Cloud akzeptieren, bevor auf die Funktion zugegriffen werden kann. Wenden Sie sich an Ihren Kundenbetreuer, um die Bedingungen abzuwählen.

## Wie greife ich auf Platform Auditor zu? {#section-531ff85f94384831a89cbb4109549daf}

Nach der Anmeldung bei [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) können Sie den Platform Auditor finden, indem Sie oben in der Navigation auf **[!UICONTROL Activation]** klicken. Sie können auch direkt zu [https://auditor.adobe.com](https://auditor.adobe.com) gehen.

## Welche Adobe-Technologien werden von Platform Auditor bewertet? {#section-52833b71c05448aaae508e6070a387f5}

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

## Wie schlage ich neue Kriterien für Prüfungen vor? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Sie können in der Platform Auditor-Community Testvorschläge senden, indem Sie auf dieser Seite auf **[!UICONTROL Feedback teilen]** klicken: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Wie lange dauert eine Prüfung? {#section-5086ae27ef1f4671a9d951348654633a}

Es gibt viele Faktoren, die dazu beitragen, dass eine Prüfung abgeschlossen werden kann, unter anderem:

* Seitenladezeit

   Die ObservePoint-Engine lädt jede Seite der Prüfung in einem Browser. Je schneller eine Seite geladen wird, desto schneller erfolgt die Prüfung.
* Gleichzeitige Verbindungen

   Platform Auditor verwendet eine einzige Verbindung, um die einzelnen Seiten zu besuchen. Vollständige ObservePoint-Konten verwenden bis zu 10 Engines gleichzeitig.
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

Alle Empfehlungen von Platform Auditor sollen Ihnen dabei helfen, ein Problem bei der Implementierung von Adobe Experience Cloud-Lösungen wie DTM oder Target zu beheben. Um dies zu erleichtern, hat das Platform Auditor-Team intensiv daran gearbeitet, sehr detaillierte Anweisungen darüber zu geben, was an welcher Stelle unternommen werden muss. Sie können eine Tabelle mit allen geprüften URLs und allen Testergebnissen exportieren, um problematische Bereiche einfach zu identifizieren. Hier ein Beispiel für eine Empfehlung zur DTM-Implementierung:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom callback last</b> </p> <p>Für eine korrekte DTM-Implementierung ist die Funktion „_satellite.pageBottom()“ erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden „&lt;/body&gt;“-Tag hinzu, um die ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kann Platform Auditor Nicht-Adobe-Technologie prüfen? {#section-f6e73c56083b4815bbf901296038bcd4}

Nein. Das vollständige Angebot von ObservePoint ermöglicht es Kunden jedoch, alle Marketing-Tags und -Technologien zu prüfen und zu überwachen. Als Adobe-Kunde haben Sie Zugriff auf ein kostenloses Testkonto. Um auf Ihr Testkonto zuzugreifen, besuchen Sie die [Seite „Auditor“ von ObservePoint](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## Kann ich meine IP-Adressen genehmigen, um das Prüfen von Seiten zuzulassen, die durch Anmeldedaten geschützt sind? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Diese Funktion wird derzeit ohne das vollständige ObservePoint-Angebot nicht unterstützt.

## Verwendet Platform Auditor dieselben IP-Bereiche wie ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

Das Durchsuchen wird von ObservePoint ausgeführt, sodass dieselben IP-Adressen verwendet werden.

Weitere Informationen finden Sie in der [ObservePoint-Dokumentation](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list).
