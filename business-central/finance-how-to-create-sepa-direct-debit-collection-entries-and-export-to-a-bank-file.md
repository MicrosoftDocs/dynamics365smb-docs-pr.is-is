---
title: Innheimta SEPA-beingreiðslu | Microsoft Docs
description: Búa til innheimta beingreiðslu og flytja út XML-skrá og hún send eða henni hlaðið upp í netbanka til úrvinnslu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct-debit, collection, payment, sepa
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 4032fd0708dcb0d420045563354677c049321f7d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238970"
---
# <a name="create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá
Til að gefa bankanum fyrirmæli um að flytja greiðsluupphæðir af bankareikningi viðskiptamannsins á reikning fyrirtækis þíns, stofnarðu innheimtu beingreiðslu sem inniheldur upplýsingar um bankareikning viðskiptamanns, sölureikningana sem um ræðir og umboð fyrir beingreiðslu. Úr innheimtufærslu beingreiðslu sem þá myndast er XML-skrá flutt út og hún send eða henni hlaðið upp í netbanka til úrvinnslu. Bankinn lætur vita af greiðslum sem hann getur ekki meðhöndlað og þá þarf að hafna viðkomandi innheimtufærslur fyrir beingreiðslur.  

> [!NOTE]  
>  Að safna greiðslum með SEPA-beingreiðslur, verður gengið á sölureikningi að vera EVRA.  

### <a name="to-create-a-direct-debit-collection"></a>Til að stofna innheimtu beingreiðslu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **innheimta beingreiðslu** og veldu síðan tengda tengilinn.  
2. Á síðunni **Innheimta beingreiðslu** í flipanum **Heim** úr flokknum **Nýtt** skal velja **Stofna innheimtu beingreiðslu**.  
3. Á síðunni **Stofna innheimtu beingreiðslu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Frá gjalddaga**|Tilgreina fyrsta gjalddaga greiðslunnar á sölureikningum sem þú vilt stofna innheimtu beingreiðslu fyrir.|  
    |**Til gjalddaga**|Tilgreina síðasta gjalddaga greiðslunnar á sölureikningum sem þú vilt stofna beina innheimtu beingreiðslu fyrir.|  
    |**Gerð viðskiptafélaga**|Tilgreina ef innheimta beingreiðslu er gerð fyrir viðskiptamenn af gerðinni **Fyrirtæki** eða **Einstaklingur**.|  
    |**Aðeins viðskiptamenn með gilt umboð**|Tilgreina ef innheimta beingreiðslu er stofnuð fyrir viðskiptamenn sem hafa gilt umboð fyrir beingreiðslu. **Athugið:** Beingreiðsla er stofnuð þó svo reiturinn **Kenni umboðs með beinni skuldfærslu** sé ekki útfylltur á sölureikningnum.|  
    |**Aðeins reikningar með gilt umboð**|Tilgreina ef innheimta beingreiðslu er stofnuð eingöngu fyrir sölureikninga ef gilt umboð fyrir beingreiðslu er valið í reitnum **Kenni umboðs með beinni skuldfærslu** reitinn á sölureikningnum.|  
    |**Númer bankareiknings**|Tilgreina hvaða bankareikningar fyrirtækis þíns hin innheimta greiðsla verður flutt á úr bankareikningi viðskiptamanns.|  
    |**Heiti Bankareiknings**|Tilgreinir nafn bankareiknings sem þú velur í **bankareikningsnúmer** reitnum. Þessi reitur er fylltur út sjálfkrafa.|  

4. Velja hnappinn **Í lagi**.  

     Innheimtu beingreiðslu er bætt við síðuna **Innheimta beingreiðslu** og ein eða fleiri innheimtufærsla fyrir beingreiðslu er stofnuð.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Flytja út innheimtufærslu beingreiðslu í bankaskrá  
1. Á síðunni **Innheimta beingreiðslu** í flipanum **Heim** úr flokknum **Vinnsla** skal velja **Innheimtafærsla fyrir beingreiðslu**.  
2. Á síðunni **Innheimtafærsla fyrir beingreiðslu**, veljið færsluna sem á að flytja út og svo, á flipanum **Heim** í hópnum **Vinnsla**, veljið **Stofna beingreiðslu** skrá.  
3. Vistar útflutningsskrá á staðsetningu þaðan sem hún er send eða henni hlaðið upp í netbanka til úrvinnslu.  

     Á síðunni **Innheimtafærsla fyrir beingreiðslu** breytist reiturinn **Staða innheimtu beingreiðslu** í Skrá stofnuð. Á síðunni **SEPA tilskipun beingreiðslu** er reiturinn **Afgreiðsluborð** uppfærður um einn.  

Ef ekki er hægt að meðhöndla útfluttu skrána, t.d. vegna þess að viðskiptavinurinn er gjaldþrota, er hægt að hafna innheimtufærslunni fyrir beingreiðslu. Ef útflutta skráin er meðhöndluð af bankanum er gjaldföllnum greiðslum sölureikninganna sjálfkrafa safnað af viðkomandi viðskiptavinum. Í því tilfelli er hægt að loka innheimtunni.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Hafna innheimtufærslu beingreiðslu  
* Á síðunni **Færsla innheimtu með beinni skuldfærslu** veljið færsluna sem ekki var meðhöndluð og svo, á flipanum **Heim** í hópnum **Vinnsla**, veljið **Hafna færslu**.  

     Gildið í reitnum **Staða** á síðunni **Innheimtufærsla fyrir beingreiðslu** er breytt í **Hafnað**.  

### <a name="to-close-a-direct-debit-collection"></a>Loka innheimtu beingreiðslu  
* Á síðunni **Færsla innheimtu með beinni skuldfærslu**, veljið færsluna sem ekki var meðhöndluð og svo, á flipanum **Heim** í hópnum **Vinnsla**, veljið **Loka færslu**.  

     Tengd innheimta beingreiðslu er lokuð.  

Þá er hægt að bóka greiðslukvittanir fyrir viðkomandi sölureikninga. Hægt er að gera þetta á sama hátt og greiðslukvittanir eru vanalega bókaðar, s.s. á síðunni **Skráning greiðslna**, en einnig er hægt að bóka tengdu greiðslukvittunina beint af síðunni **Innheimtufærslur fyrir beingreiðslu**. Frekari upplýsingar er að finna í [Bóka SEPA-greiðslukvittanir beingreiðslna](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Sjá einnig  
[Setja upp SEPA-beingreiðslur](finance-how-to-set-up-sepa-direct-debit.md)   
[Bóka SEPA-greiðslukvittanir beingreiðslna](finance-how-to-post-sepa-direct-debit-payment-receipts.md)   
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)   
