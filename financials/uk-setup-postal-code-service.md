---
title: "Hvernig skal: Setja upp GetAddress.io UK Postcodes viðbótina | Microsoft Docs"
description: "Lýsir þeirri almennu virkni sem þú notar til að vinna með gögn í Financials, eins og t.d. að færa inn gildi, raða gögnum og breyta yfirliti."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a>Hvernig skal: Setja upp GetAddress.io UK Postcodes viðbótina
Þessi viðbót gerir það auðvelt að færa inn heimilisföng í Bretlandi fyrir aðila eins og viðskiptavini, tengiliði, starfsmenn, söluaðila, bankareikninga og svo framvegis. 

The GetAddress.io UK Postcodes viðbótin notar getAddress API til að finna heimilisföng í póstnúmerum í Bretlandi. Til að nota viðbótina þarf að hafa áskrift API-lykil fyrir getAddress API. Það er auðvelt og við aðstoðum við það þegar þú setur upp GetAddress.io UK Postcodes viðbótina. Áætlanir eru byggðar á notkun, eða því sem stundum er kallað köll. Köll í þessu tilviki er þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] birtir lista yfir heimilisföng í póstnúmeri. Veldu áætlunin sem hentar þér best út frá því hversu oft þú bætir við heimilisföngum. Ef þú velur eingöngu **Fá API-lykil** á síðunni notarðu áætlunina **Ókeypis**, sem leyfir þér að bæta við 20 heimilisföngum á dag og gildir í 30 daga. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Til að setja upp GetAddress.io UK Postcodes viðbótina 
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustutengingar** og velja svo viðeigandi tengil.  
2. Í reitnum **Þjónustutengingar** er valið **UK Postcode Service**.
3. Á síðunni **Grunnstilling póstnúmera** skal velja **Slökkt**.
4. Í reitnum **Þjónustuval póstnúmerakóða** er valið **GetAddress.io**.
5. Í **GetAddress.io Config** glugganum er valið **Sækja API-lykilinn** til að opna á **Áætlanir** síðuna á vefsetrinu getAddress API.  

    > [!NOTE]  
>   Hugsanlega þarf að leyfa sprettiglugga í vafranum.
6. Kauptu áætlun, eða veldu bara **Fá API-lykil** og gefðu síðan upp netfangið þitt.
7. Opnaðu póstinn frá getAddress.io og afritaðu API-lykilinn. Lykilinn er í **API-lykilinn þinn**.
8. Í **GetAddress.io Config** glugganum límirðu API-lykilinn inn í **API-lykill** og velur svo **Í lagi**.
9. Í reitnum **Þjónustutengingar** skaltu stafðesta að **Aðsetursveit** reiturinn sýni **GetAddress.io**. Ef svo er, er þjónustan virkjuð.

## <a name="see-also"></a>Sjá einnig
[GetAddress.io UK póstnúmer](ui-extensions-getaddressio.md)
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
