---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konsistenz von Tags durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor zur Konsistenz von Tags durchführt.
seo-title: Tag-Konsistenz
title: Tag-Konsistenz
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Tag-Konsistenz

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
    </draft-comment> <p><b>Analytics - Konsistente Codeversion </b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/choose-implementation-method.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Es wurde mehr als eine Version des Analytics-Codes gefunden. </p> </td> 
   <td colname="col3"> <p>Ersetzen Sie alle Instanzen von Analytics durch die aktuelle Version. </p> </td> 
  </tr> 
 </tbody> 
</table>
