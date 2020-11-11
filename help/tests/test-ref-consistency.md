---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Adobe Experience Platform Auditor zur Konsistenz von Tags durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Adobe Experience Platform Auditor zur Konsistenz von Tags durchführt.
seo-title: Tag-Konsistenz
title: Tag-Konsistenz
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 52%

---


# Tag-Konsistenz

Diese Referenz enthält weitere Informationen zu den Tests, die Adobe Experience Platform Auditor zur Konsistenz von Tags durchführt.

Die Konsistenztests von Platform Auditor suchen auf allen gescannten Seiten nach Inkonsistenzen. Dies sind Werte oder Konfigurationen, die auf allen Seiten der Site gleich sein sollten, um die genaue Datenerfassung sicherzustellen.

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
    <!--
      1.0.1 
    --> <p><b>Analytics – Konsistente Codeversion </b> </p> <p>Gewichtung: 5 </p> <p><a href="https://docs.adobe.com/content/help/de-DE/analytics/implementation/home.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Es wurde mehr als eine Version des Analytics-Codes gefunden. </p> </td> 
   <td colname="col3"> <p>Ersetzen Sie alle Instanzen von Analytics durch die aktuelle Version. </p> </td> 
  </tr> 
 </tbody> 
</table>
