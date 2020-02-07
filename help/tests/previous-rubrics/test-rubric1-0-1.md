---
description: 'null'
seo-description: 'null'
seo-title: Test rubric 1.0.1
title: Test rubric 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: 712d0768e5e5394372293bf8231c91489519bcd1

---


# Test rubric 1.0.1{#test-rubric}

## Test rubric 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Warnhinweise {#alerts}

Diese Referenz enthält weitere Informationen zu den Warnhinweisen, die Auditor für Tests anzeigt.

Warnhinweise zeigen Probleme an, die Sie kennen sollten, die sich jedoch nicht auf Ihr Ergebnis auswirken. Dies sind Best Practice-Empfehlungen, die in einigen Fällen nicht auf Ihre Implementierung zutreffen.

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
    </draft-comment> <p><b>Advertising Cloud - implementiertes korrektes Konversions-Tag</b> </p> <p>Gewicht: 0 </p> </td> 
   <td colname="col2"> <p>Überprüfen Sie, ob das richtige Konversions-Tag verwendet wird. </p> <p> <p>Warnung:  Die Verwendung der veralteten TubeMogul-Konversions-Tags kann zu Datenverlusten führen. </p> </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie Ihre Konvertierungspixel auf die neuen Konvertierungs-Tags, die nur für die Advertising Cloud verfügbar sind. </p> <p>Dies lässt sich am einfachsten mit der Advertising Cloud Launch Extension erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Verwendetes korrektes JS-Tag</b> </p> <p>Gewicht: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud sollte die neuesten JavaScript-Tags verwenden. </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie Ihr Advertising Cloud JavaScript auf die neueste Version. Die Verwendung veralteter JavaScript-Versionen kann zu Funktionsverlusten führen. </p> <p>Dies lässt sich mit der Advertising Cloud Launch Extension einfacher erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Image-only-Tag</b> </p> <p>Gewicht: 0 </p> </td> 
   <td colname="col2"> <p>Das Bildpixelformat der Advertising Cloud sollte mit einem der folgenden empfohlenen Formate übereinstimmen: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie Ihre Advertising Cloud-Pixel auf die neuen Image-only-Tags der Advertising Cloud, um sicherzustellen, dass Sie die vollständige Funktionalität der Advertising Cloud nutzen. </p> <p>Dies lässt sich am einfachsten mit der Advertising Cloud Launch Extension erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - DSP-Synchronisierung für Segmentpixel aktiviert</b> </p> <p>Gewicht: 0 </p> </td> 
   <td colname="col2"> <p>Überprüfen Sie, ob das TubeMogul-Segmentpixel eine DSP-Synchronisierungseinstellung enthält, und empfehlen Sie, die Einstellung dem Pixel hinzuzufügen. </p> <p>Die Einstellung "DSP-Synchronisierung"wird durch die Verwendung eines Abfragezeichenfolgenparameters bestimmt. </p> <p>WENN das Tag ausgelöst<span class="codeph"> wird ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;")</span> </p> <p> ODER <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> ODER <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>UND das Tag enthält den URL-Parameter <span class="codeph"> "sid=")</span> </p> <p>Überprüfen Sie dann, ob der URL-Parameter <span class="codeph"> "cs=0"</span> oder<span class="codeph"> "cs=1"</span> vorhanden ist, und empfehlen Sie, diesen Pixeln <span class="codeph"> "cs=1"</span> hinzuzufügen, damit die Übereinstimmungsraten der Zielgruppe verbessert werden können. </p> </td> 
   <td colname="col3"> <p> Fügen Sie Ihren Advertising Cloud-Pixeln den URL-Parameter <span class="codeph"> "cs=1"</span> hinzu, damit eine DSP-Synchronisierung stattfinden kann, wodurch die Übereinstimmungsraten der Zielgruppe erhöht werden. </p> <p>Dies lässt sich am einfachsten mit der Advertising Cloud Launch Extension erreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Platzierung des Rückrufs "pageBottom"</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Für das dynamische Tag-Management ist die Funktion <span class="codeph"> _satellite.pageBottom()</span> erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden Body-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> <p> <p>Hinweis: Es empfiehlt sich, dass das Tag das <i>letzte</i> Tag im <span class="codeph"> &lt;body&gt;</span>ist. Wenn es im <span class="codeph"> &lt;body&gt;</span> -Tag gefunden wird, hat es eine Chance zu funktionieren, aber da es sich nicht um eine Best Practice handelt, könnte es falsch oder mit unerwarteten oder unerwünschten Ergebnissen funktionieren. </p> </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden Tag <span class="codeph"> &lt;/body&gt;</span> hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Self-Hosting</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Die DTM-Bibliothek wird auf der Akamai-Instanz von Adobe unter <span class="filepath"> assets.adobedtm.com</span>gehostet. </p> <p> Das Self-Hosting ist der empfohlene Ansatz zum Laden von DTM, da es die Leistung von Websites durch Cache-Steuerung, Reduzierung der Skriptabhängigkeiten von Drittanbietern und bessere Steuerung des Veröffentlichungsprozesses verbessert. Die DTM-Bibliotheken können über Ihr eigenes Webhosting oder CDN gehostet und verwaltet werden. </p> </td> 
   <td colname="col3"> <p>Das Self-Hosting ist die empfohlene Vorgehensweise zum Laden von DTM auf einer Seite. Obwohl DTM-Hosting über das Akamai-CDN in den meisten Fällen funktioniert, verbessert das Self-Hosting die Seitenleistung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID-Dienst - Verwenden Sie nur einen AdobeOrg</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Bei einer normalen MCID-Implementierung sollte ein einzelner AdobeOrg verwendet werden. </p> </td> 
   <td colname="col3"> <p>Überprüfen Sie, ob für diese Implementierung mehrere AdobeOrg-IDs vorhanden sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - pageBottom-Callback-Platzierung</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>"Launch"sollte eine <span class="codeph"> pageBottom- </span>Rückruffunktion haben, die zuletzt im Hauptteil der Seite definiert wird, wenn sie synchron bereitgestellt wird </p> <p> <p>Hinweis: Es empfiehlt sich, dass das Tag das <i>letzte</i> Tag im <span class="codeph"> &lt;body&gt;</span>ist. Wenn es im <span class="codeph"> &lt;body&gt;</span> -Tag gefunden wird, hat es eine Chance zu funktionieren, aber da es sich nicht um eine Best Practice handelt, könnte es falsch oder mit unerwarteten oder unerwünschten Ergebnissen funktionieren. </p> </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden Tag <span class="codeph"> &lt;/body&gt;</span> hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - Selbstgehostet</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Die Startbibliothek wird auf der Akamai-Instanz von Adobe unter <span class="filepath"> assets.adobedtm.com</span>gehostet. </p> <p>Das Self-Hosting ist der empfohlene Ansatz zum Laden von Launch, da es die Leistung der Website durch Cache-Steuerung besser steuern, Skriptabhängigkeiten von Drittanbietern reduzieren und den Veröffentlichungsprozess besser steuern kann. Die Launch-Bibliotheken können über Ihr eigenes Webhosting oder CDN gehostet und verwaltet werden. </p> </td> 
   <td colname="col3"> <p>Obwohl das Hosting über das Akamai CDN in den meisten Fällen funktioniert, wird empfohlen, das Self-Hosting als ersten Schritt zur Verbesserung der Seitenleistung zu implementieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - sollte asynchron bereitgestellt werden</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Start sollte asynchron bereitgestellt werden, um eine optimale Leistung zu erzielen. </p> </td> 
   <td colname="col3"> <p>Fügen Sie den async-Parameter in das Inline-Skript ein, um eine ordnungsgemäße asynchrone Startfunktion sicherzustellen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Inhalt in mboxDefault</b> </p> <p>Gewicht: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung von "at.js"sollte der Inhalt in "mboxDefault"vorhanden sein. </p> </td> 
   <td colname="col3"> <p>Überprüfen Sie, ob der Inhalt verfügbar ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Konfiguration {#configuration}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konfiguration durchführt.

Konfigurationstests suchen nach bestimmten Einstellungen, Werten oder möglichen Konflikten in Ihrer Implementierung. Der Prüfer bewertet die Tags anhand anderer Regeln und empfohlener Best Practices.

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
    </draft-comment> <p><b>Advertising Cloud - Konversionsnamen verwenden nur alphanumerische Zeichen</b> </p> <p>Gewicht: 3 </p> </td> 
   <td colname="col2"> <p>Der <span class="codeph"> Parameter ev_conversion_property_name</span> sollte nur numerische und Dezimalwerte enthalten, AUSSER für den Parameter "<span class="codeph"> ev_transid</span>" (der Wert <span class="codeph"> ev_transid</span> kann Text oder numerische Werte enthalten). </p> <p>Suchen Sie nach <span class="codeph"> "everesttech.net</span> "-Pixeln, die einen URL-Parameter enthalten, der mit " <span class="codeph"> ev_</span>"beginnt. </p> <p>Beispiel: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Stellen Sie sicher, dass die Parameter der Transaktionseigenschaft nur numerische und Dezimalwerte enthalten. </p> <p> <p>Warnung:  Alle anderen Werttypen können Datenverluste verursachen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Konversionsnamen verwenden URL-sichere Zeichen</b> </p> <p>Gewicht: 3 </p> </td> 
   <td colname="col2"> <p> Umrechnungseigenschaftsnamen dürfen kein kaufmännisches und kein Fragezeichen enthalten. </p> <p> Beispiel: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass Transaktionseigenschaftsparameter kein nicht kodiertes kaufmännisches und kein Fragezeichen enthalten. Dadurch wird das URL-Format beschädigt. </p> <p> <p>Warnung: Eigenschaftenparameter, die ein nicht kodiertes kaufmännisches Und- oder Fragezeichen enthalten (z. B.: <span class="codeph"> ev_formComplete?=1</span> oder <span class="codeph"> ev_formComplete&amp;Submit=1</span>) zu einem Datenverlust führen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Transaktions-ID korrekt implementiert</b> </p> <p>Gewicht: 1 </p> </td> 
   <td colname="col2"> <p> Der Eigenschaftsname <span class="codeph"> ev_transid=</span> sollte nicht leer sein. </p> <p>Beispiel: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Der Eigenschaftsname <span class="codeph"> ev_transid=</span> sollte nicht ohne Wert (<span class="codeph"> ev_transid=</span>) belassen werden. Wenn dies ohne Wert bleibt, kann es zu Datenverlusten aufgrund von Transaktionen kommen. Weisen Sie dem Wert <span class="codeph"> ev_transid=</span> einen Wert zu oder entfernen Sie den Parameter aus dem Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instanziiert in DOM</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Adobe Analytics-Code ist entweder nicht installiert oder kann nicht ausgeführt werden. Gibt 0 zurück, wenn keine Webseite für Analytics-Code gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass das Analytics-Tag auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - einmal instanziiert</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Adobe Analytics-Code wurde mehrmals auf der Seite erkannt. . Gibt 0 zurück, wenn keine Webseite für Analytics-Code gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass nur ein Analytics-Tag auf der Seite vorhanden ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - neueste Version</b> </p> <p>Gewicht: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Analytics-Codebibliothek ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen zu nutzen und die neuesten Funktionen bereitzustellen. Gibt 0 zurück, wenn keine Webseite für Analytics-Code gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version der Analytics-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Drittanbieter-Tags werden asynchron geladen, nachdem DOM-bereit</b> </p> <p>Gewicht: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Um ein Gleichgewicht zwischen einer guten Benutzererfahrung und der Erfassung genauer Daten herzustellen, sollten Drittanbieter-Tags bei DOM-bereit ausgelöst werden. Dadurch wird sichergestellt, dass diese Verfolgungsskripten ausgeführt werden, ohne dass dadurch die Funktionalität der Site beeinträchtigt wird. </p> </td> 
   <td colname="col3"> <p>Beheben Sie dieses Problem, indem Sie alle Regeln anpassen, die Pixel von Drittanbietern ausführen, damit sie bei DOM Ready ausgelöst werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - neueste Version</b> </p> <p>Gewicht: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Code-Bibliothek des Besucher-ID-Diensts, <span class="codeph"> visitorAPI.js</span>, ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen zu nutzen und die neuesten Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version der Besucher-ID-Dienst-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - neueste Version</b> </p> <p>Gewicht: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Auf diesen Seiten wird nicht die neueste Version der Launch-Code-Bibliothek (Turbine) ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen zu nutzen und die neuesten Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p> Aktualisieren Sie die Startbibliothek, indem Sie die Startbibliothek neu erstellen und veröffentlichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - neueste Version</b> </p> <p>Gewicht: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Target-Codebibliothek ausgeführt. Codebibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen zu nutzen und die neuesten Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version der Target-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefault vor mboxCreate </b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Die ordnungsgemäße Verwendung von <span class="codeph"> mboxCreate</span> sieht in etwa so aus: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Kundeninhalt—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass Sie ein <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> -Tag einschließen, bevor Sie <span class="codeph"> mboxCreate()</span>aufrufen. "at.js"wird keinen für Sie hinzufügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Ziel - Gültiger DOCTYPE</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein ungültiger DOCTYPE wurde erkannt. In diesem Szenario werden keine Mboxes ausgelöst. </p> <p>Bei at.js muss sich der DOCTYPE im Standardmodus befinden, sonst funktioniert Target nicht. </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie den DOCTYPE auf der Seite. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag-Konsistenz {#tag-consistency}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konsistenz von Tags durchführt.

Die Konsistenztests des Prüfers suchen auf Inkonsistenzen auf allen gescannten Seiten. Dies sind Werte oder Konfigurationen, die auf allen Seiten der Site gleich sein sollten, um eine genaue Datenerfassung sicherzustellen.

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
    </draft-comment> <p><b>Analytics - Konsistente Codeversion </b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/choose-implementation-method.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Es wurde mehr als eine Version des Analytics-Codes gefunden. </p> </td> 
   <td colname="col3"> <p>Ersetzen Sie alle Instanzen von Analytics durch die aktuelle Version. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tag-Präsenz {#tag-presence}

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.

Auditor bewertet, ob das Tag vorhanden ist und ob es sich an der richtigen Stelle im Seiten-Code befindet.

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
    </draft-comment> <p><b>Advertising Cloud - Code-Präsenz</b> </p> <p>Gewicht: 5 </p> </td> 
   <td colname="col2"> <p> Das Advertising Cloud-Tag ist im DOM nicht verfügbar. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Tag Advertising Cloud mit der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Segmentpixel implementiert</b> </p> <p>Gewicht: 5 </p> </td> 
   <td colname="col2"> <p> Aktualisieren Sie Ihre Advertising Cloud-Segmentpixel auf die neuen Image-only-Tags der Advertising Cloud. Die Verwendung der nicht mehr unterstützten AMO-Segment-Tags kann zu Datenverlusten führen. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Segment-Pixel der Advertising Cloud mit der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - In DOM geladen</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das Adobe Analytics-Tag wurde nicht erkannt. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Bibliothek geladen</b> </p> <p>Gewicht: 5 </p> <p>Weitere Informationen: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="html" scope="external"> DTM-Fehlerbehebung</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Kopf- und Fußzeilencode hinzufügen</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Ein globales _satellite-Objekt wurde im DOM nicht gefunden. Das dynamische Tag-Management ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die DTM-Bibliothek auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Einbettungscode</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Produktions-Sites sollten nur eine DTM-Bibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Rückruf pageBottom vorhanden in &lt;body&gt;</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde nicht im <span class="codeph"> &lt;body&gt;</span> der Seite gefunden, was für das dynamische Tag-Management erforderlich ist. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom- </span>Aufruf überhaupt nicht auf der Seite gefunden wird oder wenn er sich im <span class="codeph"> &lt;head&gt;</span> -Tag (oder einer anderen unerwarteten Position) befindet. Sie wird nur dann übernommen, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span> -Tag gefunden wird. Wenn es sich nicht auf der Seite befindet, funktioniert es nicht und die anderen beiden <span class="codeph"> SeitenBottom</span> -Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden Tag <span class="codeph"> &lt;/body&gt;</span> hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom-Tag ausgelöst</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das DTM- <span class="codeph"> Tag "Seitenende</span> "wurde nicht erkannt. </p> <p>Dies kann vorkommen, wenn sich der Aufruf innerhalb einer <span class="codeph"> if</span> -Anweisung befindet, die in etwa <span class="codeph"> if (false) {_satellite.pageBottom()}</span>resultiert. Während es also existiert und korrekt platziert ist, wird das Tag möglicherweise nicht ausgelöst. </p> </td> 
   <td colname="col3"> <p>Installieren Sie den DTM- <span class="codeph"> pageBottom</span> -Aufruf auf jeder Seite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - Code-Präsenz</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-overview.htmlimplementation-guides.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Experience Cloud ID-Dienst-Code wurde nicht gefunden. Die Experience Cloud ID (MCID) wird dringend empfohlen, um sicherzustellen, dass Sie den größtmöglichen Nutzen aus Ihren Experience Cloud-Lösungen ziehen, und ist für das ID-Management in allen Experience Cloud-Lösungen von entscheidender Bedeutung. </p> </td> 
   <td colname="col3"> <p> Installieren Sie die neueste Version von MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - Cookie-Präsenz</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das <span class="codeph"> AMCV_</span> -Cookie wurde nicht gefunden. Sie müssen ein Besucherobjekt aus dem Code VisitorAPI.js<span class="codeph"> </span> instanziieren. </p> </td> 
   <td colname="col3"> <p> Ist dies eine DTM-Implementierung, überprüfen Sie, ob die AdobeOrg-ID korrekt in das MCID-Tool eingegeben wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - MID-Wert vorhanden</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html#concept_37156268512445F287CD4BBB2839FFAA__section_C55AF54828DC4CCE89F6118655D694C8" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der MID-Wert wurde im <span class="codeph"> AMCV_</span> -Cookie nicht gefunden. </p> </td> 
   <td colname="col3"> <p>Testen Sie erneut, um nach einer MCID-API-Latenz zu suchen. Wenn die Bedingung weiterhin besteht, wenden Sie sich an den Adobe-Kundendienst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Start - Bibliothek geladen</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein globales _satellite-Objekt wurde im DOM nicht gefunden. Launch ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die Launch-Bibliothek auf der Seite implementiert ist und nicht von nachfolgenden Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - Es stehen nicht mehrere Einbettungsskripten zur Verfügung</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Es sollten nicht mehrere Einbettungsskripte auf der Seite geladen werden. Produktions-Sites sollten nur eine Startbibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - Rückruf pageBottom vorhanden in &lt;body&gt;</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde nicht im <span class="codeph"> &lt;body&gt;</span> der Seite gefunden, was für Launch erforderlich ist. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom- </span>Aufruf überhaupt nicht auf der Seite gefunden wird oder wenn er sich im <span class="codeph"> &lt;head&gt;</span> -Tag (oder einer anderen unerwarteten Position) befindet. Sie wird nur dann übernommen, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span> -Tag gefunden wird. Wenn es sich nicht auf der Seite befindet, funktioniert es nicht und die anderen beiden <span class="codeph"> SeitenBottom</span> -Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span> -Tag hinzu, um eine ordnungsgemäße Startfunktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Start - Rückruffunktion "pageBottom"sollte bei asynchroner Bereitstellung nicht vorhanden sein</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde auf der Seite gefunden, was bei asynchroner Bereitstellung von Launch nicht der Fall sein sollte. </p> </td> 
   <td colname="col3"> <p>Entfernen Sie das<span class="codeph"> Skript _satellite.pageBottom()</span> , um eine ordnungsgemäße Startfunktion zu aktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Code-Präsenz</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Target sollte im DOM definiert werden. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Bibliothek geladen in &lt;head&gt;</b> </p> <p>Gewicht: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> Die Target-Bibliothek sollte im Tag <span class="codeph"> &lt;head&gt;</span> geladen werden. </p> </td> 
   <td colname="col3"> <p> Vergewissern Sie sich, dass die Target-Bibliothek im Tag <span class="codeph"> &lt;head&gt;</span> geladen ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

