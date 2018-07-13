---
title: "Stjórnun sérstillinga sem stjórnandi í Business Central | Microsoft Docs"
description: "Lærðu hvernig á að aðlaga notendaviðmótið til að henta því hvernig þú vinnur."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 4914c0b7c269d5f725f33c839eb677455293cea0
ms.contentlocale: is-is
ms.lasthandoff: 06/01/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Stjórnun sérstillinga sem stjórnandi
<!--NAV in the Web client-->
Notendur geta sérsniðið vinnusvæði sitt að vild. Sem stjórnandi geturðu stjórnað og unnið með sérstillingar með því að slökkva á valkosti notenda til að sérstilla síður og hreinsa allar sérstillingar síðu sem notendur hafa gert.

## <a name="disable-personalization-for-a-profile"></a>Slökkva á sérstillingu fyrir forstillingu
Hægt er að koma í veg fyrir að allir notendur sem tilheyra tiltekinni forstillingu geti sérstillt síður sínar.
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forstillingar** og velja svo viðeigandi tengil.
2.  Veljið forstillinguna sem á að breyta í listanum.
3. Veljið gátreitinn **Afvirkja sérstillingar notanda** og smellið síðan á hnappinn **Í lagi**.

## <a name="clear-user-personalizations"></a>Hreinsa sérstillingar notenda

Þegar sérstillingar síðu er eytt fer síðan aftur í upprunalegt útlit áður en sérstillingin var gerð. Það eru tvær leiðir til að hreinsa sérstillingar sem notendur hafa gert á síðum: með **Eyða sérstillingum notanda** síðunni og **Sérstillingaspjald notanda**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Hreinsa sérstillingar notenda með því að nota síðuna Eyða sérstillingum notanda

Síðan **Eyða sérstillingum notanda** gerir þér kleift að hreinsa sérstillingar á einstaka síðum, eftir einstaka notendum.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Eyða sérstillingum notanda** og velja svo viðeigandi tengil.

    Á síðunni er listi yfir allar síður sem hafa verið sérstilltar og sem notandinn tilheyrir.

    >[!NOTE]
    > Gátmerki í **Eldri sérstilling** dálknum gefur til kynna að sérstillingin hafi verið gerð í eldri útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)], sem meðhöndlaði sérstillingu öðruvísi en er núna gert. Notendur sem reyna að sérstilla þessar síður eru útilokaðir frá því að gera það nema þeir velji að opna síðuna. Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).

2. Veljið færsluna sem á að eyða og veljið síðna aðgerðina **Eyða**.

    Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Hreinsa sérstillingar notenda með því að nota síðuna Sérstillingaspjald notanda

Síðan **Sérstillingaspjald notanda** gerir þér kleift að hreinsa sérstillingar á öllum síðum fyrir tiltekinn notanda. Þetta krefst skrifleyfis fyrir töflu 2000000072 **Forstilling**.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sérstillingar notanda** og velja svo viðeigandi tengil.

    Síðan **Sérstillingar notanda** sýnir alla notendur sem hugsanlega hafa sérstillt síður. Ef þú finnur ekki notanda á listanum þýðir það að hann hefur engar sérstilltar síður.

2. Veljið notanda af listanum og veljið svo aðgerðina **Breyta**.

3.  Í flipanum **Aðgerðir** veljið **Hreinsa sérstilltar síður**.

    Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

## <a name="see-also"></a>Sjá einnig
[Sérstillingar verksvæðis](ui-personalization-user.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Breyting á hvaða eiginleikar eru sýndir](ui-experiences.md)  

