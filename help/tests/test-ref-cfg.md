---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Adobe Experience Platform Auditor für die Konfiguration durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Adobe Experience Platform Auditor für die Konfiguration durchführt.
seo-title: Konfiguration
title: Konfiguration
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 100%

---


# Konfiguration

Diese Referenz enthält weitere Informationen zu den Tests, die Adobe Experience Platform Auditor für die Konfiguration durchführt.

Bei Konfigurationstests wird nach bestimmten Einstellungen, Werten oder möglichen Konflikten in Ihrer Implementierung gesucht. Platform Auditor bewertet die Tags anhand anderer Regeln und empfohlener Best Practices.

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
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud – Konversionsnamen enthalten nur alphanumerische Zeichen</b> </p> <p>Gewichtung: 3 </p> </td> 
   <td colname="col2"> <p>Der Parameter <span class="codeph"> ev_conversion_property_name</span> sollte nur numerische und Dezimalwerte enthalten, AUẞER für den Parameter <span class="codeph"> ev_transid</span> (der Wert <span class="codeph"> ev_transid</span> darf Text oder numerische Werte enthalten). </p> <p>Suchen Sie nach <span class="codeph"> everesttech.net</span>-Pixeln, die einen URL-Parameter enthalten, der mit <span class="codeph"> ev_</span> beginnt. </p> <p>Beispiel: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Stellen Sie sicher, dass die Parameter der Transaktionseigenschaft nur numerische und Dezimalwerte enthalten. </p> <p> <p>Warnung: Alle anderen Werttypen können Datenverluste verursachen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud – Konversionsnamen verwenden URL-geeignete Zeichen</b> </p> <p>Gewichtung: 3 </p> </td> 
   <td colname="col2"> <p> Konversionseigenschaftsnamen dürfen kein Und- und kein Fragezeichen enthalten. </p> <p> Beispiel: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass Transaktionseigenschaftsparameter kein nicht-kodiertes Und- und kein Fragezeichen enthalten. Diese Zeichen beeinträchtigen das URL-Format. </p> <p> <p>Warnung: Eigenschaftenparameter, die ein nicht-kodiertes Und- oder Fragezeichen enthalten (z. B. <span class="codeph"> ev_formComplete?=1</span> oder <span class="codeph"> ev_formComplete&amp;Submit=1</span>) können zu Datenverlust führen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud – Transaktions-ID ist korrekt implementiert</b> </p> <p>Gewichtung: 1 </p> </td> 
   <td colname="col2"> <p> Der Eigenschaftsname <span class="codeph"> ev_transid=</span> sollte nicht leer sein. </p> <p>Beispiel: </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Der Eigenschaftsname <span class="codeph"> ev_transid=</span> sollte nicht ohne Wert (<span class="codeph"> ev_transid=</span>) belassen werden. Andernfalls kann es zu Transaktionsdatenverlust kommen. Weisen Sie dem Wert <span class="codeph"> ev_transid=</span> einen Wert zu oder entfernen Sie den Parameter aus dem Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics – Ist in DOM instanziiert</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Adobe Analytics-Code ist entweder nicht installiert oder kann nicht ausgeführt werden. Gibt 0 zurück, wenn kein Analytics-Code auf der Webseite gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass das Analytics-Tag auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics – Ist einmal instanziiert</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Adobe Analytics-Code wurde mehrmals auf der Seite erkannt. Gibt 0 zurück, wenn kein Analytics-Code auf der Webseite gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass nur ein Analytics-Tag auf der Seite vorhanden ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics – Neueste Version</b> </p> <p>Gewichtung: 3 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Analytics-Codebibliothek ausgeführt. Code-Bibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. Gibt 0 zurück, wenn kein Analytics-Code auf der Webseite gefunden wurde. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die aktuelle Version der Analytics-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM – Drittanbieter-Tags werden nach DOM Ready asynchron geladen</b> </p> <p>Gewichtung: 3 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/resources/load-order.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Für ein Gleichgewicht zwischen guter Benutzererfahrung und Erfassung genauer Daten sollten Drittanbieter-Tags bei DOM Ready ausgelöst werden. Dadurch wird sichergestellt, dass diese Tracking-Skripte ausgeführt werden, ohne dass dadurch die Funktionalität der Site beeinträchtigt wird. </p> </td> 
   <td colname="col3"> <p>Beheben Sie dieses Problem, indem Sie alle Regeln anpassen, die Pixel von Drittanbietern ausführen, damit diese Pixel bei DOM Ready ausgelöst werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-Service – Neueste Version</b> </p> <p>Gewichtung: 2 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/tools/macid.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Codebibliothek des Besucher-ID-Services <span class="codeph"> visitorAPI.js</span> ausgeführt. Code-Bibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version der Besucher-ID-Service-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch – Neueste Version</b> </p> <p>Gewichtung: 2 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Auf diesen Seiten wird nicht die neueste Version der Platform Launch-Code-Bibliothek (Turbine) ausgeführt. Code-Bibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p> Aktualisieren Sie die Platform Launch-Bibliothek, indem Sie sie neu erstellen und veröffentlichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target – Neueste Version</b> </p> <p>Gewichtung: 2 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Auf Ihren Seiten wird nicht die neueste Version der Target-Codebibliothek ausgeführt. Code-Bibliotheken, die Experience Cloud-Technologien nutzen, werden ständig aktualisiert und optimiert, um Leistungsverbesserungen und neueste Funktionen bereitzustellen. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die aktuelle Version der Target-Bibliothek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target – mboxDefault vor mboxCreate </b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Die ordnungsgemäße Verwendung von <span class="codeph"> mboxCreate</span> sieht in etwa so aus: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Kundeninhalt--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Stellen Sie sicher, dass Sie ein <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span>-Tag einschließen, bevor Sie <span class="codeph"> mboxCreate()</span> aufrufen. „at.js“ fügt keins für Sie hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target – Gültiger DOCTYPE</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/help/de-DE/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein ungültiger DOCTYPE wurde erkannt. In diesem Szenario werden keine mboxes ausgelöst. </p> <p>Bei „at.js“ muss sich der DOCTYPE im Standardmodus befinden, sonst funktioniert Target nicht. </p> </td> 
   <td colname="col3"> <p>Aktualisieren Sie den DOCTYPE auf der Seite. </p> </td> 
  </tr> 
 </tbody> 
</table>

