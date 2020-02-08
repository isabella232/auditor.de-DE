---
description: Filter einschließen beschränken, welche Links eine Prüfung von der Start-URL durchsuchen kann. Filter ausschließen verhindert, dass eine Prüfung Links durchsuchen kann.
seo-description: Filter einschließen beschränken, welche Links eine Prüfung von der Start-URL durchsuchen kann. Filter ausschließen verhindert, dass eine Prüfung Links durchsuchen kann.
seo-title: Filter einschließen und ausschließen
title: Filter einschließen und ausschließen
uuid: 477fc38c-7351-42dd-8209-2fb7549ee34c
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Filter einschließen und ausschließen{#include-and-exclude-filters}

Filter einschließen beschränken, welche Links eine Prüfung von der Start-URL durchsuchen kann. Filter ausschließen verhindert, dass eine Prüfung Links durchsuchen kann.

<!--
Content from ObservePoint (https://help.observepoint.com/articles/2872121-include-and-exclude-filters) with their permission. Modified slightly for style and Auditor emphasis.
-->

Filter einschließen und Filter ausschließen enthalten Richtlinien für Prüfungen. Wenn Sie die Filter &quot;Einschließen&quot;und &quot;Ausschließen&quot;leer lassen, kann eine Prüfung alle Links durchsuchen, auf die sie zutrifft, beginnend mit Links in der Start-URL.

![](assets/filter.png)

Indem Sie Filter einschließen, Filter ausschließen oder eine Kombination aus beiden anwenden, erhalten Sie Anweisungen, welche Links ein Audit durchsuchen kann.

Jedes Element im Feld &quot;Filter einschließen&quot;beschränkt die Überprüfung auf die Seiten, die mit diesem Element übereinstimmen. Jedes Element in einem Feld zum Ausschließen von Filtern verhindert, dass Seiten, die diesem Element entsprechen, gescannt werden.

Die Filter &quot;Einschließen&quot;und &quot;Ausschließen&quot;können vollständige URLs, teilweise URLs oder reguläre Ausdrücke sein, die einer gültigen Seite entsprechen.

## Rangfolge {#section-e9d42419dd3f459bb20e7a33c6104f12}

1. **Die Start-URL** hat Vorrang vor allem anderen und wird während einer Prüfung immer besucht, auch wenn eine URL mit einem Element in den Ausschließen-Filtern übereinstimmt. Die Start-URL wird immer vor anderen URLs aufgerufen.

   ![](assets/startingpage.png)

   Im obigen Bild erkennt ein Audit Links aus der `document.links` Eigenschaft der Startseite. Diese Links können von der Prüfung eingesehen werden.

1. **Einschließende URLs** müssen von einer Startseite aus verknüpft werden, da sie andernfalls nicht erkannt werden können und nicht besucht werden.

   ![](assets/includefilter.png)

   In der Abbildung oben werden die zulässigen URLs durch Hinzufügen eines Filters &quot;Einschließen&quot;auf die URLs beschränkt, die mit dem Filter übereinstimmen. Jetzt können nur noch fünf Links von der Prüfung überprüft werden.

1. **URLs** ausschließen, Links von der Berechtigung ausschließen.

   ![](assets/excludefilter.png)

   In der Abbildung oben wird durch Hinzufügen eines Filters &quot;Ausschließen&quot;verhindert, dass URLs von den entsprechenden Links entfernt werden. Jetzt können nur noch drei Links von der Prüfung überprüft werden.

## Starten der URL {#section-ccb46abcd96f4a8ab171245015d2b724}

Auditor benötigt eine einzelne Seite für die Start-URL. Die Start-URL wird immer vor anderen URLs aufgerufen. Alle auf der Startseite entdeckten Links sind zum Besuch berechtigt, vorbehaltlich der Filter Einschließen und Ausschließen. Wenn ein Ausschlusselement mit einer Start-URL übereinstimmt, wird es ignoriert.

## Filter einschließen {#section-7626060a56a24b658f8c05f031ac3f5f}

Die Filter &quot;Einschließen&quot;beschränken, welche Links während einer Prüfung überprüft werden dürfen. Filter einschließen können:

* Vollständig qualifizierte URLs
* Teil-URL
* Reguläre Ausdrücke, die mit vollständigen oder teilweisen URLs übereinstimmen
* Jede Kombination der oben genannten

Das Hinzufügen von URLs oder regulären Ausdrücken zum Filter &quot;Einschließen&quot;gewährleistet nicht, dass diese spezifischen URLs bei der Prüfung gescannt werden. Die Prüfung prüft die Links auf der Start-URL und navigiert dann durch die entsprechenden Links. Die Prüfung führt diesen Prozess der Überprüfung und Navigation fort, bis die Grenze von 500 gescannten URLs erreicht ist oder bis keine weiteren zulässigen Links gefunden wurden.

>[!NOTE]
>
>In einigen Fällen kann es bis zu 48 Stunden dauern, bis eine 500-Seiten-Überprüfung abgeschlossen ist.

Standardmäßig werden bei einer Prüfung alle Subdomänen der Start-URL überprüft. Sofern nicht explizit durch Angabe eines Einschlussfilters überschrieben, verwendet die Prüfung den folgenden Regex-Include-Filter:

`^https?://([^/:\?]*\.)?mysite.com`

Dadurch ist jeder Link, der auf der Startseite der URL gefunden wurde, zum Besuch berechtigt. Entspricht jeder Seite in einer Subdomäne der Start-URL.

Die Verwendung des standardmäßigen Filters &quot;Einschließen&quot;bietet einen breiten Bereich, in dem ein Audit durchsucht werden kann. Wenn Sie sich in bestimmten Abschnitten oder Seiten einloggen möchten, geben Sie in diesem Feld eine bestimmte Anleitung für Ihre Prüfung ein, indem Sie Filter hinzufügen. Ersetzen Sie in diesem Fall den Standardwert durch die Ordner, die überprüft werden sollen. Sie können auch Filter zum Einschließen verwenden, um domänenübergreifende Prüfungen durchzuführen, bei denen Sie die Prüfung in einer Domäne starten und in einer anderen enden müssen. Geben Sie dazu die Domänen ein, die Sie durchlaufen möchten. In jedem Fall müssen Filter-URLs mit einschließen auf einer geprüften Seite gefunden werden.

Die Filter einschließen können exakte URLs, teilweise URLs oder reguläre Ausdrücke enthalten. Wenn die Start-URL beispielsweise [!DNL http://mysite.com]lautet, können die folgenden Seiten standardmäßig gescannt werden (beachten Sie die fett gedruckten Zeichen):

```
http://mysite.com
http
<b>s</b>://mysite.com
http://
<b>www</b>.mysite.com/home
http://
<b>dev</b>.mysite.com/home
http://
<b>my</b>.mysite.com/products/products_and_services.html
```

Für komplexe URL-Muster verwenden Sie den [ObservePoint-Test](http://regex.observepoint.com/)für reguläre Ausdrücke.

Weitere Informationen zu häufigen Anwendungsfällen für die Musterzuordnung finden Sie im Dokument [Common Regulular Expressions for ObservePoint](https://help.observepoint.com/articles/2872116-common-regular-expressions-for-observepoint) .

## Filter ausschließen {#section-00aa5e10c878473b91ba0844bebe7ca9}

Die Filter &quot;Ausschließen&quot;verhindern, dass URLs geprüft werden. Sie können exakte URLs, teilweise URLs oder reguläre Ausdrücke verwenden. Jede URL, die mit einem Element in den Ausschließen-Filtern übereinstimmt, wird nicht besucht. Wenn Ihre Start-URL in den Ausschließen-Filtern enthalten ist, wird sie nicht ausgeschlossen. Die Start-URL wird immer von einer Prüfung gescannt.

## Testen von Filtern und URLs {#section-3cfa125b1756411395a64701e128efa0}

Sie können Ihre Filter und URLs in Auditor testen.

Klicken Sie beim Erstellen der Prüfung auf Erweiterte Filter **[!UICONTROL testen]**. Geben Sie Ihre Filter und URLs ein und klicken Sie dann auf **[!UICONTROL Übernehmen]**.

![](assets/test-advanced-filters.png)

## ObservePoint-Dokumentation {#section-79cdc8e850d047969b6d2badf6bbd6f9}

Dieser Artikel wurde in Zusammenarbeit mit ObservePoint entwickelt. Aktuelle Informationen finden Sie in der [ObservePoint-Dokumentation](https://help.observepoint.com/articles/2872121-include-and-exclude-filters).
