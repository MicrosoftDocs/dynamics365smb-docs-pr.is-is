---
title: "Setja upp GetAddress.io UK Postcodes viðbætur | Microsoft Docs"
description: "Lýsir hvernig á að setja upp og stilla póstnúmeraþjónustu til að flytja inn heimilisföng í Bretlandi"
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29b3b551e3ea8e8dfd52a3846332eec47f9346ce
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="set-up-the-getaddressio-uk-postcodes-extension"></a>Setja upp GetAddress.io UK Postcodes viðbótina
Þessi viðbót gerir það auðvelt að færa inn heimilisföng í Bretlandi fyrir aðila eins og viðskiptavini, tengiliði, starfsmenn, söluaðila, bankareikninga og svo framvegis. 

The GetAddress.io UK Postcodes viðbótin notar getAddress API til að finna heimilisföng í póstnúmerum í Bretlandi. Til að nota viðbótina þarf að hafa áskrift API-lykil fyrir getAddress API. Það er auðvelt og við aðstoðum við það þegar þú setur upp GetAddress.io UK Postcodes viðbótina. Áætlanir eru byggðar á notkun, eða því sem stundum er kallað köll. Köll í þessu tilviki er þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] birtir lista yfir heimilisföng í póstnúmeri. Veldu áætlunin sem hentar þér best út frá því hversu oft þú bætir við heimilisföngum. Ef þú velur eingöngu **Fá API-lykil** á síðunni notarðu áætlunina **Ókeypis**, sem leyfir þér að bæta við 20 heimilisföngum á dag og gildir í 30 daga. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Til að setja upp GetAddress.io UK Postcodes viðbótina 
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Þjónustutengingar**, og velja síðan viðeigandi tengil.  
2. Í reitnum **Þjónustutengingar** er valið **UK Postcode Service**.
3. Á síðunni **Grunnstilling póstnúmera** skal velja **Slökkt**.
4. Í reitnum **Þjónustuval póstnúmerakóða** er valið **GetAddress.io**.
5. Í **GetAddress.io Config** glugganum er valið **Sækja API-lykilinn** til að opna á **Áætlanir** síðuna á vefsetrinu getAddress API.  

    **Athugið**: Hugsanlega þarf að leyfa sprettiglugga í vafranum.
6. Kauptu áætlun, eða veldu bara **Fá API-lykil** og gefðu síðan upp netfangið þitt.
7. Opnaðu póstinn frá getAddress.io og afritaðu API-lykilinn. Lykilinn er í **API-lykilinn þinn**.
8. Í **GetAddress.io Config** glugganum límirðu API-lykilinn inn í **API-lykill** og velur svo **Í lagi**.
9. Í reitnum **Þjónustutengingar** skaltu stafðesta að **Aðsetursveit** reiturinn sýni **GetAddress.io**. Ef svo er, er þjónustan virkjuð.

## <a name="see-also"></a>Sjá einnig
[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md) [Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)]Með Extensions](ui-extensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
