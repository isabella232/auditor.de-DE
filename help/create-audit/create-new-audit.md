---
description: Neue Prüfung in Auditor erstellen
seo-description: Neue Prüfung in Auditor erstellen
seo-title: Neue Prüfung in Auditor erstellen
title: Neue Prüfung in Auditor erstellen
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Create a new audit{#create-a-new-audit}

>[!NOTE]
>
>Benutzer sind auf eine Prüfung beschränkt, die gleichzeitig ausgeführt wird. Es tritt ein Fehler auf, wenn Sie versuchen, eine Prüfung mit denselben Einstellungen wie die ausgeführte zu starten. Sie können den Link in der Fehlermeldung verwenden, wenn Sie die derzeit ausgeführte Prüfung abbrechen möchten, damit Sie eine neue Prüfung erstellen können.

Falls gewünscht, verwenden Sie den Link unten auf der Seite, um auf ein kostenloses, voll ausgestattetes Testkonto mit ObservePoint zuzugreifen.

1. Klicken Sie in der Liste &quot;Prüfer&quot;auf **[!UICONTROL Neue Prüfung]**.

   The [!DNL New Audit] screen opens.

   ![](assets/config.png)

1. (Erforderlich) Benennen Sie die Prüfung.

   Der Name kann aus bis zu 250 Zeichen bestehen.
1. (Erforderlich) Geben Sie die Start-URL an.

   Das Protokoll ist beim Festlegen der Start-URL erforderlich. Die Start-URL ist die Seite, auf der die Prüfung beginnt zu krabbeln. Nach dem Start durchsucht Auditor bis zu 500 Seiten, wobei Links folgen, die an der Start-URL beginnen. Weitere Informationen finden Sie unter Filter [einschließen und ausschließen](../create-audit/filters.md#concept-23531490bb124981ba807ed1806e3257) . Die Start-URL kann bis zu 250 Zeichen lang sein.

   >[!NOTE]
   >
   >In einigen Fällen kann es bis zu 48 Stunden dauern, bis eine 500-Seiten-Überprüfung abgeschlossen ist.

1. Geben Sie eine oder mehrere E-Mail-Adressen für Benachrichtigungen zu dieser Prüfung an.

   Sie können mehrere E-Mails angeben, indem Sie jede Adresse durch ein Komma trennen. Der Anforderer wird standardmäßig benachrichtigt. E-Mail-Adressen werden in Echtzeit validiert. Wenn Sie eine ungültige Adresse eingeben, werden Sie auf dem Bildschirm benachrichtigt.

   Jede E-Mail ist auf maximal 250 Zeichen beschränkt, einschließlich des Domänenendpunkts (z. B. .com).
1. Geben Sie Filter einschließen an.

   Dieses Feld kann exakte URLs, teilweise URLs oder reguläre Ausdrücke enthalten. Verwenden Sie dieses Feld für Kriterien, denen jede URL entsprechen soll. Durchgekrackte URLs, die nicht mit den Kriterien &quot;Filter einschließen&quot;übereinstimmen, werden nicht in die Prüfergebnisse aufgenommen.

   Sie können Ordner eingeben, in die die Prüfung durchgeführt werden soll. Oder Sie können eine domänenübergreifende oder selbstverweisende Prüfung durchführen, bei der Sie die Prüfung in einer Domäne starten und in einer anderen enden müssen. Geben Sie zu diesem Zweck die Domänen ein, die Sie durchlaufen möchten. für komplexe URL-Muster verwenden Sie einen regulären Ausdruck.

   >[!NOTE]
   >
   >Wenn Sie eine Seite in Ihren Filtern einschließen, sie jedoch nicht mit Ihrer Startseiten-URL verbunden ist oder Auditor 500 Seiten scannt, bevor die Seite erreicht wird, wird die Seite nicht gescannt und wird nicht in die Testergebnisse aufgenommen.

   Die Einschlussfilter sind auf 1.000 Zeichen pro Zeile beschränkt.

   Weitere Informationen finden Sie unter Liste [einschließen](../create-audit/filters.md#section-7626060a56a24b658f8c05f031ac3f5f) .
1. Geben Sie Filter ausschließen an.

   Die Ausschlussliste verhindert, dass URLs geprüft werden. Verwenden Sie exakte URLs, teilweise URLs oder reguläre Ausdrücke, genau wie in der Liste &quot;Einschließen&quot;.

   Eine gängige Praxis besteht darin, einen Link zum Abmelden auszuschließen, wenn die Prüfung eine Benutzersitzung hat (z. B.: `/logout`, d. h. jede URL, die die Zeichenfolge enthält `/logout`).

   Die Ausschlussfilter sind auf 1.000 Zeichen pro Zeile beschränkt.

   Weitere Informationen finden Sie unter Liste [ausschließen](../create-audit/filters.md#section-00aa5e10c878473b91ba0844bebe7ca9) .
1. (Optional) Bei Bedarf können Sie die Filter zum Einschließen und Ausschließen testen und Ihre URLs testen.

   Geben Sie die Filter und URLs ein und klicken Sie dann auf **[!UICONTROL Übernehmen]** , um den Test auszuführen.

   ![](assets/test-advanced-filters.png)

1. Klicken Sie auf **[!UICONTROL Bericht ausführen]**.
