---
description: Diese Referenz enthält weitere Informationen zu den Warnhinweisen, die Auditor für Tests anzeigt.
seo-description: Diese Referenz enthält weitere Informationen zu den Warnhinweisen, die Auditor für Tests anzeigt.
seo-title: Warnhinweise
title: Warnhinweise
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: ht
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# Warnhinweise {#alerts}

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
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
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
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM – Platzierung des Rückrufs „pageBottom“</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Für das Dynamic Tag Management ist die Funktion <span class="codeph">_satellite.pageBottom()</span> erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> <p> <p>Hinweis: Es ist Best Practice, dass das Tag das <i>letzte</i> Tag im <span class="codeph"> &lt;body&gt;</span>ist. Wenn es im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird, kann es eventuell funktionieren, doch da es sich hierbei nicht um eine Best Practice handelt, könnte es falsch oder mit unerwarteten bzw. unerwünschten Ergebnissen funktionieren. </p> </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM – Self-Hosting</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/de_DE/dtm/deployment.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Die DTM-Bibliothek wird auf der Akamai-Instanz von Adobe unter <span class="filepath"> assets.adobedtm.com</span> gehostet. </p> <p> Das Self-Hosting ist der empfohlene Ansatz zum Laden von DTM, da es die Leistung von Websites durch Cache-Steuerung, Reduzierung der Skriptabhängigkeiten von Drittanbietern und bessere Steuerung des Veröffentlichungsprozesses verbessert. Die DTM-Bibliotheken können über Ihr eigenes Web-Hosting oder CDN gehostet und verwaltet werden. </p> </td> 
   <td colname="col3"> <p>Das Self-Hosting ist der empfohlene Ansatz zum Laden von DTM auf einer Seite. Obwohl DTM-Hosting über das Akamai-CDN in den meisten Fällen funktioniert, verbessert das Self-Hosting die Seitenleistung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID-Service – Nur ein AdobeOrg wird verwendet</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/de_DE/mcvid/mcvid_id_request.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Bei einer normalen MCID-Implementierung sollte eine einzelne AdobeOrg verwendet werden. </p> </td> 
   <td colname="col3"> <p>Validieren Sie, ob für diese Implementierung mehrere AdobeOrg-IDs vorhanden sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch – Platzierung des Rückrufs „pageBottom“</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Weitere Informationen</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Launch sollte über eine <span class="codeph">pageBottom</span>-Rückruffunktion verfügen, die zuletzt im Body der Seite definiert wird, wenn sie synchron bereitgestellt wird. </p> <p> <p>Hinweis: Es ist Best Practice, dass das Tag das <i>letzte</i> Tag im <span class="codeph"> &lt;body&gt;</span>ist. Wenn es im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird, kann es eventuell funktionieren, doch da es sich hierbei nicht um eine Best Practice handelt, könnte es falsch oder mit unerwarteten bzw. unerwünschten Ergebnissen funktionieren. </p> </p> </td> 
   <td colname="col3"> <p>Für Launch ist die Funktion <span class="codeph"> _satellite.pageBottom()</span> für synchrone Bereitstellungen erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße Launch-Funktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Self-Hosting</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Erste Schritte mit Launch</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> Asynchrone Launch-Bereitstellung</a> </p> </td> 
   <td colname="col2"> <p>Die Launch-Bibliothek wird auf der Akamai-Instanz von Adobe unter <span class="filepath"> assets.adobedtm.com</span> gehostet. </p> <p>Das Self-Hosting ist der empfohlene Ansatz zum Laden von Launch, da es die Leistung von Websites durch Cache-Steuerung, Reduzierung der Skriptabhängigkeiten von Drittanbietern und bessere Steuerung des Veröffentlichungsprozesses verbessert. Die Launch-Bibliotheken können über Ihr eigenes Web-Hosting oder CDN gehostet und verwaltet werden. </p> </td> 
   <td colname="col3"> <p>Obwohl das Hosting über das Akamai CDN in den meisten Fällen funktioniert, wird empfohlen, das Self-Hosting als ersten Schritt zur Verbesserung der Seitenleistung zu implementieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch – Sollte asynchron bereitgestellt werden</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Launch sollte asynchron bereitgestellt werden, um optimale Leistung zu erzielen. </p> </td> 
   <td colname="col3"> <p>Fügen Sie den „async“-Parameter in das Inline-Skript ein, um die ordnungsgemäße asynchrone Launch-Funktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target – Inhalt in mboxDefault</b> </p> <p>Gewichtung: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung von „at.js“ sollte der Inhalt in „mboxDefault“ vorhanden sein. </p> </td> 
   <td colname="col3"> <p>Validieren Sie, ob der Inhalt verfügbar ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

