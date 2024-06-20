---
title: Besta Outlook fyrir viðskiptainnhólfið
description: Kynntu þér hvað hægt er að gera til að bæta upplifun með fyrirtækjainnhólfi í Microsoft Outlook.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in'
ms.date: 12/06/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="optimize-outlook-for-your-business-inbox"></a>Besta Outlook fyrir viðskiptainnhólfið

Í þessari grein er fjallað um ýmislegt sem hægt er að gera til að hámarka upplifunina með fyrirtækjainnhólfi í Microsoft Outlook. 

## <a name="update-outlook"></a>Uppfæra Outlook

Uppfæra í Outlook útgáfu 2012 eða nýrri.

> [!NOTE]
> Ef ekki er hægt að uppfæra Outlook í útgáfu 2012 eða nýrri þarf að tryggja að a.m.k. sé uppfært í útgáfu 1905. Það kemur í veg fyrir að Outlook-viðbótin geti keyrt með eldri Internet Explorer íhlutum

### <a name="how-to-check-your-version-of-outlook"></a>Hvernig á að athuga útgáfu þína af Outlook

Hvort sem þú notar Office 2019 eða Microsoft 365 skaltu fylgja þessum leiðbeiningum frá notendaþjónustu Microsoft til að athuga hvaða útgáfu af Outlook þú ert með:  

[Um Office: Hvaða útgáfu af Office er ég að nota?](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a>Hvernig á að uppfæra Outlook

Ef þú vilt uppfæra Outlook í nýjustu útgáfuna skaltu fylgja þessum leiðbeiningum frá Notendaþjónustu Microsoft eða hafa samband við kerfisstjóra:

[Setja upp Office-uppfærslur](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a>Setja upp Microsoft Edge WebView2

Gakktu úr skugga um að Microsoft Edge WebView2 sé uppsett í tækinu.

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a>Hvernig á að athuga hvort Microsoft Edge WebView2 sé uppsett

Gerðu eftirfarandi til að athuga hvort Microsoft Edge WebView2 sé uppsett á tölvu:

Úr upphafsvalmyndinni:

1. Veldu **Upphafsvalmynd** ![Upphafsvalmynd Windows.](media/windows-start-icon.png "Windows upphafstákn") > **Stillingar** ![Windows-stillingar](media/windows-settings-icon.png "Stillingatákn Windows") > **Forrit og eiginleikar**.
2. Farðu í leitargluggann og sláðu inn **WebView2**. Ef Microsoft Edge WebView2 hefur verið sett upp sést færsla sem nefnist **Microsoft Edge WebView2 Runtime**.

Í stjórnborðinu:

1. Í leitarglugganum við hliðina á **Byrja** ![Windows Start](media/windows-start-icon.png "Windows upphafstákn") skaltu slá inn **Stjórnborð** og velja niðurstöðuna.
2. Veldu **Forrit** > **Forrit og eiginleikar**.
3. Farðu í leitargluggann og sláðu inn **WebView2**. Ef Microsoft Edge WebView2 hefur verið sett upp sést færsla sem nefnist **Microsoft Edge WebView2 Runtime**.

### <a name="how-to-install-microsoft-edge-webview2"></a>Hvernig á að setja upp Microsoft Edge WebView2

1. Í vafranum þínum skaltu fara á [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).
2. Veldu **Niðurhal**.
3. Veldu **Velja uppbyggingu** sem passar við kerfið þitt.
4. Veldu **Niðurhal**.

> [!NOTE]
> Fyrirtækið gæti takmarkað hvaða íhluti er hægt að setja upp í tækinu. Hafðu samband við stjórnanda til að fá aðstoð.

## <a name="use-a-supported-browser"></a>Notaðu studdan vafra

Íhugaðu að nota Outlook fyrir vefinn í einhverri vafranna sem Business Central styður. Listi yfir studda vafra er í [Lágmarkskröfur fyrir notkun Business Central](product-requirements.md#browsers).

## <a name="see-also"></a>Sjá einnig .

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Sækja Business Central í fartækið mitt](install-mobile-app.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Lágmarkskröfur fyrir Outlook](product-requirements.md#outlook)  
[Nota innbætur í Outlook á vefnum](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
