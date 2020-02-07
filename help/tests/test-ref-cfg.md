---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konfiguration durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konfiguration durchführt.
seo-title: Konfiguration
title: Konfiguration
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Konfiguration

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
    </draft-comment> <p><b>Start - neueste Version</b> </p> <p>Gewicht: 2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
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

