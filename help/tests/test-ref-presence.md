---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.
seo-title: Tag-Präsenz
title: Tag-Präsenz
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: ht
source-git-commit: a76ecb232c29d83ef82b14be460d9ce60f5e8662
workflow-type: ht
source-wordcount: '943'
ht-degree: 100%

---


# Tag-Präsenz

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
   <td colname="col1"> <p><b>Advertising Cloud – Codepräsenz</b> </p> <p>Gewichtung: 5 </p> </td> 
   <td colname="col2"> <p> Das Advertising Cloud-Tag ist im DOM nicht verfügbar. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Tag „Advertising Cloud“ mit der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud – Segmentpixel sind implementiert</b> </p> <p>Gewichtung: 5 </p> </td> 
   <td colname="col2"> <p> Aktualisieren Sie Ihre Advertising Cloud-Segmentpixel auf die neuen „Nur Bild“-Tags der Advertising Cloud. Die Verwendung der nicht mehr unterstützten AMO-Segment-Tags kann zu Datenverlust führen. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Segmentpixel der Advertising Cloud mithilfe der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics – Ist in DOM geladen</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das Adobe Analytics-Tag wurde nicht erkannt. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM – Bibliothek ist geladen</b> </p> <p>Gewichtung: 5 </p> <p>Weitere Informationen: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM-Fehlerbehebung</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Kopf- und Fußzeilencode hinzufügen</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Ein globales „_satellite“-Objekt wurde im DOM nicht gefunden. Dynamic Tag Management ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die DTM-Bibliothek auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM – Ein Einbettungscode</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Produktions-Sites sollten nur eine DTM-Bibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM – Rückruf „pageBottom“ ist in &lt;body&gt; vorhanden</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde im <span class="codeph"> &lt;body&gt;</span> der Seite nicht gefunden, ist aber dort für das Dynamic Tag Management erforderlich. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom </span>-Aufruf überhaupt nicht auf der Seite gefunden wird oder sich im <span class="codeph"> &lt;head&gt;</span>-Tag (oder an einer anderen unerwarteten Position) befindet. Der Test gilt nur als bestanden, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird. Wenn es sich überhaupt nicht auf der Seite befindet, funktioniert diese nicht und die anderen beiden <span class="codeph"> pageBottom</span>-Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM – „pageBottom“-Tag wird ausgelöst</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das DTM-<code> pageBottom</code>-Tag wurde nicht erkannt. </p> <p>Dies kann vorkommen, wenn sich der Aufruf in einer <code> if</code>-Anweisung befindet, deren Ergebnis in etwa <code> if (false) {_satellite.pageBottom()}</code>entspricht. Daher kann es vorkommen, dass das Tag vorhanden und richtig platziert ist, aber nicht ausgelöst wird. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die DTM-<code> pageBottom</code>-Anweisung auf jeder Seite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Service – Codepräsenz</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/id-service/using/intro/overview.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Experience Cloud ID-Service-Code wurde nicht gefunden. Es wird dringend empfohlen, dass eine Experience Cloud ID (MCID) vorhanden ist, um sicherzustellen, dass Sie Ihre Experience Cloud-Lösungen optimal nutzen. Sie ist außerdem für das ID-Management in allen Experience Cloud-Lösungen von entscheidender Bedeutung. </p> </td> 
   <td colname="col3"> <p> Installieren Sie die neueste Version von MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Service – Cookiepräsenz</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/dtm/using/tools/macid.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
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
      1.0.5 
    </draft-comment> <p><b> Launch – Bibliothek ist geladen</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein globales „_satellite“-Objekt wurde im DOM nicht gefunden. Launch ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die Launch-Bibliothek auf der Seite implementiert ist und nicht von nachfolgenden Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch – Nicht mehrere Einbettungsskripte angeben</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Auf der Seite sollten nicht mehrere Einbettungsskripte geladen werden. Produktions-Sites sollten nur eine Launch-Bibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch – Rückruf „pageBottom“ ist in &lt;body&gt; vorhanden</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde im <span class="codeph"> &lt;body&gt;</span> der Seite nicht gefunden, ist aber für Launch erforderlich. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom </span>-Aufruf überhaupt nicht auf der Seite gefunden wird oder sich im <span class="codeph"> &lt;head&gt;</span>-Tag (oder an einer anderen unerwarteten Position) befindet. Der Test gilt nur als bestanden, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span>-Tag gefunden wird. Wenn es sich überhaupt nicht auf der Seite befindet, funktioniert diese nicht und die anderen beiden <span class="codeph"> pageBottom</span>-Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span>-Tag hinzu, um eine ordnungsgemäße Launch-Funktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch – Rückruf „pageBottom“ sollte bei asynchroner Bereitstellung nicht vorhanden sein</b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
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
   <td colname="col1"> <p><b>Target – Bibliothek wird in &lt;head&gt; geladen</b> </p> <p>Gewichtung: 4 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Die Target-Bibliothek sollte im Tag <span class="codeph"> &lt;head&gt;</span> geladen werden. </p> </td> 
   <td colname="col3"> <p> Vergewissern Sie sich, dass die Target-Bibliothek im Tag <span class="codeph"> &lt;head&gt;</span> geladen wird. </p> </td> 
  </tr> 
 </tbody> 
</table>
