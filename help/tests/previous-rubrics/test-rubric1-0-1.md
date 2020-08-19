---
description: Informationen zu Adobe-Auditor-Tests
seo-description: Informationen zu Adobe-Auditor-Tests
seo-title: Testrubrik 1.0.1
title: Testrubrik 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: c3ab954f45bd12758b7bfe100a30c8a9859613b9
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 99%

---


# Testrubrik 1.0.1 {#test-rubric}

## Testrubrik 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Warnhinweise {#alerts}

Diese Referenz enthält weitere Informationen zu den Warnhinweisen, die Auditor für Tests anzeigt.

Warnhinweise zeigen Probleme an, die Sie kennen sollten, aber sich nicht auf Ihr Ergebnis auswirken. Dies sind Best Practice-Empfehlungen, die in einigen Fällen nicht auf Ihre Implementierung zutreffen.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterien </th> 
   <th colname="col3" class="entry"> Empfehlung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Korrektes Konversions-Tag ist implementiert</b> </p> <p>Gewichtung: 0 </p> </td> 
   <td colname="col2"> <p>Überprüfen Sie, ob das richtige Konversions-Tag verwendet wird. </p> <p> <p>Warnung: Die Verwendung der nicht mehr unterstützten TubeMogul-Konversions-Tags kann zu Datenverlust führen. </p> </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie Ihre Konversionspixel auf die neuen „Nur-Bild“-Konversions-Tags von Advertising Cloud. </p> <p>Dies ist am einfachsten mit der Advertising Cloud Launch Extension zu erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Korrektes JS-Tag wird verwendet</b> </p> <p>Gewichtung: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud sollte die neuesten JavaScript-Tags verwenden. </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie Ihr Advertising Cloud-JavaScript auf die neueste Version. Die Verwendung veralteter JavaScript-Versionen kann zu Funktionsverlust führen. </p> <p>Dies ist mit der Advertising Cloud Launch Extension einfacher zu erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – „Nur-Bild“-Tag</b> </p> <p>Gewichtung: 0 </p> </td> 
   <td colname="col2"> <p>Das Bildpixelformat der Advertising Cloud sollte mit einem der folgenden empfohlenen Formate übereinstimmen: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie Ihre Advertising Cloud-Pixel auf die neuen „Nur-Bild“-Tags der Advertising Cloud, um sicherzustellen, dass Sie die vollständige Funktionalität der Advertising Cloud nutzen. </p> <p>Dies ist am einfachsten mit der Advertising Cloud Launch Extension zu erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – DSP-Synchronisierung für Segmentpixel ist aktiviert</b> </p> <p>Gewichtung: 0 </p> </td> 
   <td colname="col2"> <p>Überprüfen Sie, ob das TubeMogul-Segmentpixel eine DSP-Synchronisierungseinstellung enthält, und empfehlen Sie, dem Pixel die Einstellung hinzuzufügen. </p> <p>Die Einstellung „DSP-Synchronisierung“ wird durch die Verwendung eines Abfragezeichenfolgenparameters bestimmt. </p> <p>WENN das Tag ausgelöst wird für <span class="codeph">("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;")</span> </p> <p> ODER <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> ODER <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>UND das Tag den URL-Parameter <span class="codeph"> "sid=")</span> enthält, </p> <p>DANN überprüfen Sie, ob der URL-Parameter <span class="codeph"> "cs=0"</span> oder <span class="codeph"> "cs=1"</span> vorhanden ist. Wenn nicht, empfehlen Sie, diesen Pixeln <span class="codeph"> "cs=1"</span> hinzuzufügen, damit die Übereinstimmungsraten der Zielgruppe verbessert werden können. </p> </td> 
   <td colname="col3"> <p> Fügen Sie Ihren Advertising Cloud-Pixeln den URL-Parameter <span class="codeph"> "cs=1"</span> hinzu, damit eine DSP-Synchronisierung stattfinden kann, wodurch die Übereinstimmungsraten der Zielgruppe erhöht werden. </p> <p>Dies ist am einfachsten mit der Advertising Cloud Launch Extension zu erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM – Platzierung des Rückrufs „pageBottom“</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Für das Dynamic Tag Management ist die Funktion <span class="codeph">_satellite.pageBottom()</span> erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden „Body“-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> <p> <p>Hinweis: Es ist Best Practice, dass das Tag das <i>letzte</i> Tag im <span class="codeph"> &lt;body&gt;</span>ist. Wenn es im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird, kann es eventuell funktionieren, doch da es sich hierbei nicht um eine Best Practice handelt, könnte es falsch oder mit unerwarteten bzw. unerwünschten Ergebnissen funktionieren. </p> </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM – Self-Hosting</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Die DTM-Bibliothek wird auf der Akamai-Instanz von Adobe unter <span class="filepath"> assets.adobedtm.com</span> gehostet. </p> <p> Das Self-Hosting ist der empfohlene Ansatz zum Laden von DTM, da es die Leistung von Websites durch Cache-Steuerung, Reduzierung der Skriptabhängigkeiten von Drittanbietern und bessere Steuerung des Veröffentlichungsprozesses verbessert. Die DTM-Bibliotheken können über Ihr eigenes Web-Hosting oder CDN gehostet und verwaltet werden. </p> </td> 
   <td colname="col3"> <p>Das Self-Hosting ist der empfohlene Ansatz zum Laden von DTM auf einer Seite. Obwohl DTM-Hosting über das Akamai-CDN in den meisten Fällen funktioniert, verbessert das Self-Hosting die Seitenleistung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID-Service – Nur ein AdobeOrg wird verwendet</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/id-service/using/intro/id-request.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Bei einer normalen MCID-Implementierung sollte eine einzelne AdobeOrg verwendet werden. </p> </td> 
   <td colname="col3"> <p>Validieren Sie, ob für diese Implementierung mehrere AdobeOrg-IDs vorhanden sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Platzierung des Rückrufs „pageBottom“</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Launch sollte über eine <span class="codeph">pageBottom</span>-Rückruffunktion verfügen, die zuletzt im Body der Seite definiert wird, wenn sie synchron bereitgestellt wird. </p> <p> <p>Hinweis: Es ist Best Practice, dass das Tag das <i>letzte</i> Tag im <span class="codeph"> &lt;body&gt;</span>ist. Wenn es im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird, kann es eventuell funktionieren, doch da es sich hierbei nicht um eine Best Practice handelt, könnte es falsch oder mit unerwarteten bzw. unerwünschten Ergebnissen funktionieren. </p> </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Self-Hosting</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Die Launch-Bibliothek wird auf der Akamai-Instanz von Adobe unter <span class="filepath"> assets.adobedtm.com</span> gehostet. </p> <p>Das Self-Hosting ist der empfohlene Ansatz zum Laden von Launch, da es die Leistung von Websites durch Cache-Steuerung, Reduzierung der Skriptabhängigkeiten von Drittanbietern und bessere Steuerung des Veröffentlichungsprozesses verbessert. Die Launch-Bibliotheken können über Ihr eigenes Web-Hosting oder CDN gehostet und verwaltet werden. </p> </td> 
   <td colname="col3"> <p>Obwohl das Hosting über das Akamai CDN in den meisten Fällen funktioniert, wird empfohlen, das Self-Hosting als ersten Schritt zur Verbesserung der Seitenleistung zu implementieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Sollte asynchron bereitgestellt werden</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Launch sollte asynchron bereitgestellt werden, um optimale Leistung zu erzielen. </p> </td> 
   <td colname="col3"> <p>Fügen Sie den „async“-Parameter in das Inline-Skript ein, um die ordnungsgemäße asynchrone Launch-Funktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target – Inhalt in mboxDefault</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung von „at.js“ sollte der Inhalt in „mboxDefault“ vorhanden sein. </p> </td> 
   <td colname="col3"> <p>Validieren Sie, ob der Inhalt verfügbar ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Konfiguration {#configuration}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konfiguration durchführt.

Bei Konfigurationstests wird nach bestimmten Einstellungen, Werten oder möglichen Konflikten in Ihrer Implementierung gesucht. Auditor bewertet die Tags anhand anderer Regeln und empfohlener Best Practices.

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterien </th> 
   <th colname="col3" class="entry"> Empfehlung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Konversionsnamen enthalten nur alphanumerische Zeichen</b> </p> <p>Gewichtung: 3 </p> </td> 
   <td colname="col2"> <p>Der Parameter <span class="codeph"> ev_conversion_property_name</span> sollte nur numerische und Dezimalwerte enthalten, AUẞER für den Parameter <span class="codeph"> ev_transid</span> (der Wert <span class="codeph"> ev_transid</span> darf Text oder numerische Werte enthalten). </p> <p>Suchen Sie nach <span class="codeph"> everesttech.net</span>-Pixeln, die einen URL-Parameter enthalten, der mit <span class="codeph"> ev_</span> beginnt. </p> <p>Beispiel: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Stellen Sie sicher, dass die Parameter der Transaktionseigenschaft nur numerische und Dezimalwerte enthalten. </p> <p> <p>Warnung: Alle anderen Werttypen können Datenverluste verursachen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Konversionsnamen verwenden URL-geeignete Zeichen</b> </p> <p>Gewichtung: 3 </p> </td> 
   <td colname="col2"> <p> Konversionseigenschaftsnamen dürfen kein Und- und kein Fragezeichen enthalten. </p> <p> Beispiel: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass Transaktionseigenschaftsparameter kein nicht-kodiertes Und- und kein Fragezeichen enthalten. Diese Zeichen beeinträchtigen das URL-Format. </p> <p> <p>Warnung: Eigenschaftenparameter, die ein nicht-kodiertes Und- oder Fragezeichen enthalten (z. B. <span class="codeph"> ev_formComplete?=1</span> oder <span class="codeph"> ev_formComplete&amp;Submit=1</span>) können zu Datenverlust führen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Transaktions-ID ist korrekt implementiert</b> </p> <p>Gewichtung: 1 </p> </td> 
   <td colname="col2"> <p> Der Eigenschaftsname <span class="codeph"> ev_transid=</span> sollte nicht leer sein. </p> <p>Beispiel: </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Der Eigenschaftsname <span class="codeph"> ev_transid=</span> sollte nicht ohne Wert (<span class="codeph"> ev_transid=</span>) belassen werden. Andernfalls kann es zu Transaktionsdatenverlust kommen. Weisen Sie dem Wert <span class="codeph"> ev_transid=</span> einen Wert zu oder entfernen Sie den Parameter aus dem Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics – Ist in DOM instanziiert</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Adobe Analytics-Code ist entweder nicht installiert oder kann nicht ausgeführt werden. Gibt 0 zurück, wenn kein Analytics-Code auf der Webseite gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass das Analytics-Tag auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics – Ist einmal instanziiert</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Adobe Analytics-Code wurde mehrmals auf der Seite erkannt. Gibt 0 zurück, wenn kein Analytics-Code auf der Webseite gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass nur ein Analytics-Tag auf der Seite vorhanden ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics – Neueste Version</b> </p> <p>Gewichtung: 3 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Analytics-Codebibliothek ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. Gibt 0 zurück, wenn kein Analytics-Code auf der Webseite gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die aktuelle Version der Analytics-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM – Drittanbieter-Tags werden nach DOM Ready asynchron geladen</b> </p> <p>Gewichtung: 3 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/resources/load-order.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Für ein Gleichgewicht zwischen guter Benutzererfahrung und Erfassung genauer Daten sollten Drittanbieter-Tags bei DOM Ready ausgelöst werden. Dadurch wird sichergestellt, dass diese Tracking-Skripte ausgeführt werden, ohne dass dadurch die Funktionalität der Site beeinträchtigt wird. </p> </td> 
   <td colname="col3"> <p>Beheben Sie dieses Problem, indem Sie alle Regeln anpassen, die Pixel von Drittanbietern ausführen, damit diese Pixel bei DOM Ready ausgelöst werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Service – Neueste Version</b> </p> <p>Gewichtung: 2 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/tools/macid.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Codebibliothek des Besucher-ID-Services <span class="codeph"> visitorAPI.js</span> ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version der Besucher-ID-Service-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Neueste Version</b> </p> <p>Gewichtung: 2 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Auf diesen Seiten wird nicht die neueste Version der Launch-Codebibliothek (Turbine) ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p> Aktualisieren Sie die Launch-Bibliothek, indem Sie sie neu erstellen und veröffentlichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target – Neueste Version</b> </p> <p>Gewichtung: 2 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/tools/target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Target-Codebibliothek ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die aktuelle Version der Target-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target – mboxDefault vor mboxCreate </b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Die ordnungsgemäße Verwendung von <span class="codeph"> mboxCreate</span> sieht in etwa so aus: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Kundeninhalt--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass Sie ein <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span>-Tag einschließen, bevor Sie <span class="codeph"> mboxCreate()</span> aufrufen. „at.js“ fügt keins für Sie hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target – Gültiger DOCTYPE</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein ungültiger DOCTYPE wurde erkannt. In diesem Szenario werden keine mboxes ausgelöst. </p> <p>Bei „at.js“ muss sich der DOCTYPE im Standardmodus befinden, sonst funktioniert Target nicht. </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie den DOCTYPE auf der Seite. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag-Konsistenz {#tag-consistency}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Konsistenz durchführt.

Die Auditor-Konsistenztests suchen Inkonsistenzen auf allen geprüften Seiten. Dies sind Werte oder Konfigurationen, die auf allen Seiten der Site gleich sein sollten, um die genaue Datenerfassung sicherzustellen.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterien </th> 
   <th colname="col3" class="entry"> Empfehlung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics – Konsistente Codeversion </b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Es wurde mehr als eine Version des Analytics-Codes gefunden. </p> </td> 
   <td colname="col3"> <p>Ersetzen Sie alle Instanzen von Analytics durch die aktuelle Version. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag-Präsenz {#tag-presence}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.

Auditor bewertet, ob das Tag vorhanden ist und sich an der richtigen Stelle im Seitencode befindet.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterien </th> 
   <th colname="col3" class="entry"> Empfehlung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Codepräsenz</b> </p> <p>Gewichtung: 5 </p> </td> 
   <td colname="col2"> <p> Das Advertising Cloud-Tag ist im DOM nicht verfügbar. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Tag „Advertising Cloud“ mit der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud – Segmentpixel sind implementiert</b> </p> <p>Gewichtung: 5 </p> </td> 
   <td colname="col2"> <p> Aktualisieren Sie Ihre Advertising Cloud-Segmentpixel auf die neuen „Nur Bild“-Tags der Advertising Cloud. Die Verwendung der nicht mehr unterstützten AMO-Segment-Tags kann zu Datenverlust führen. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Segmentpixel der Advertising Cloud mithilfe der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics – Ist in DOM geladen</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das Adobe Analytics-Tag wurde nicht erkannt. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM – Bibliothek ist geladen</b> </p> <p>Gewichtung: 5 </p> <p>Weitere Informationen: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM-Fehlerbehebung</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Kopf- und Fußzeilencode hinzufügen</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Ein globales „_satellite“-Objekt wurde im DOM nicht gefunden. Dynamic Tag Management ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die DTM-Bibliothek auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM – Ein Einbettungscode</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Produktions-Sites sollten nur eine DTM-Bibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM – Rückruf „pageBottom“ ist in &lt;body&gt; vorhanden</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde im <span class="codeph"> &lt;body&gt;</span> der Seite nicht gefunden, ist aber dort für das Dynamic Tag Management erforderlich. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom </span>-Aufruf überhaupt nicht auf der Seite gefunden wird oder sich im <span class="codeph"> &lt;head&gt;</span>-Tag (oder an einer anderen unerwarteten Position) befindet. Der Test gilt nur als bestanden, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird. Wenn es sich überhaupt nicht auf der Seite befindet, funktioniert diese nicht und die anderen beiden <span class="codeph"> pageBottom</span>-Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM – „pageBottom“-Tag wird ausgelöst</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das DTM-Tag <span class="codeph"> pageBottom</span> wurde nicht erkannt. </p> <p>Dies kann vorkommen, wenn sich der Aufruf innerhalb einer <span class="codeph"> if</span>-Anweisung befindet, die in etwas Ähnliches wie <span class="codeph"> if (false) {_satellite.pageBottom()}</span> resultiert. Daher kann es vorkommen, dass das Tag vorhanden und richtig platziert ist, aber nicht ausgelöst wird. </p> </td> 
   <td colname="col3"> <p>Installieren Sie den DTM-Aufruf <span class="codeph"> pageBottom</span> auf jeder Seite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Service – Codepräsenz</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation/implementation-methods.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Experience Cloud ID-Service-Code wurde nicht gefunden. Es wird dringend empfohlen, dass eine Experience Cloud ID (MCID) vorhanden ist, um sicherzustellen, dass Sie Ihre Experience Cloud-Lösungen optimal nutzen. Sie ist außerdem für das ID-Management in allen Experience Cloud-Lösungen von entscheidender Bedeutung. </p> </td> 
   <td colname="col3"> <p> Installieren Sie die neueste Version von MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Service – Cookiepräsenz</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/id-service/using/implementation/implementation-guides.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das <span class="codeph"> AMCV_</span>-Cookie wurde nicht gefunden. Sie müssen ein Besucherobjekt aus dem Code <span class="codeph"> VisitorAPI.js</span> instanziieren. </p> </td> 
   <td colname="col3"> <p> Wenn es sich um eine DTM-Implementierung handelt, stellen Sie sicher, dass die AdobeOrg-ID korrekt in das MCID-Tool eingegeben wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Service – MID-Wert ist vorhanden</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/id-service/using/intro/cookies.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der MID-Wert wurde im <span class="codeph"> AMCV_</span>-Cookie nicht gefunden. </p> </td> 
   <td colname="col3"> <p>Testen Sie erneut, um nach MCID-API-Latenz zu suchen. Wenn diese Bedingung weiterhin besteht, wenden Sie sich an die Adobe-Kundenunterstützung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Launch – Bibliothek ist geladen</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein globales „_satellite“-Objekt wurde im DOM nicht gefunden. Launch ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die Launch-Bibliothek auf der Seite implementiert ist und nicht von nachfolgenden Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Nicht mehrere Einbettungsskripte angeben</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Auf der Seite sollten nicht mehrere Einbettungsskripte geladen werden. Produktions-Sites sollten nur eine Launch-Bibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Rückruf „pageBottom“ ist in &lt;body&gt; vorhanden</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde im <span class="codeph"> &lt;body&gt;</span> der Seite nicht gefunden, ist aber für Launch erforderlich. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom </span>-Aufruf überhaupt nicht auf der Seite gefunden wird oder sich im <span class="codeph"> &lt;head&gt;</span>-Tag (oder an einer anderen unerwarteten Position) befindet. Der Test gilt nur als bestanden, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird. Wenn es sich überhaupt nicht auf der Seite befindet, funktioniert diese nicht und die anderen beiden <span class="codeph"> pageBottom</span>-Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße Launch-Funktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Rückruf „pageBottom“ sollte bei asynchroner Bereitstellung nicht vorhanden sein</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde auf der Seite gefunden, was bei asynchroner Bereitstellung von Launch nicht der Fall sein sollte. </p> </td> 
   <td colname="col3"> <p>Entfernen Sie das Skript <span class="codeph">_satellite.pageBottom()</span>, um die ordnungsgemäße Launch-Funktion zu aktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target – Codepräsenz</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Target sollte im DOM definiert sein. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target – Bibliothek wird in &lt;head&gt; geladen</b> </p> <p>Gewichtung: 4 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> Die Target-Bibliothek sollte im Tag <span class="codeph"> &lt;head&gt;</span> geladen werden. </p> </td> 
   <td colname="col3"> <p> Vergewissern Sie sich, dass die Target-Bibliothek im Tag <span class="codeph"> &lt;head&gt;</span> geladen wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

