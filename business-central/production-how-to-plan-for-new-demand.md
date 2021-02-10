---
title: Hvernig skal gera áætlanir pöntun fyrir pöntun | Microsoft Docs
description: Þessa áætlanagerð er hægt að framkvæma á síðunni **Pantanaáætlun** sem birtir alla nýja eftirspurn auk upplýsinga um ráðstöfunarmagn og tillögum um framboð. Hann veitir nauðsynlegan sýnileika og verkfæri til að gera skilvirkar áætlanir um eftirspurn úr sölulínum og íhlutalínum og stofna síðan beint mismunandi tegundir af framboðspöntunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 62f5254da05749c2da4690e7d49488af852ac67a
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013845"
---
# <a name="plan-for-new-demand-order-by-order"></a>Gera áætlanir um nýja eftirspurn pöntun fyrir pöntun
Þessa áætlanagerð er hægt að framkvæma á síðunni **Pantanaáætlun** sem birtir alla nýja eftirspurn auk upplýsinga um ráðstöfunarmagn og tillögum um framboð. Hann veitir nauðsynlegan sýnileika og verkfæri til að gera skilvirkar áætlanir um eftirspurn úr sölulínum og íhlutalínum og stofna síðan beint mismunandi tegundir af framboðspöntunum.  

Hægt er að fara inn á síðuna **Pantanaáætlun** á tvenna vegu, eftir því hvert markmiðið er: Frá pöntun sem þú vilt gera áætlun fyrir sérstaklega eða í keyrslufasa því þú vilt gera áætlun fyrir allar og hverja nýja eftispurn.  


## <a name="to-plan-for-new-production-order-demand"></a>Til að gera áætlun fyrir nýja framleiðslupöntunareftirspurn  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlaðar framleiðslupantanir** og veldu síðan tengda tengilinn. (Hægt er að framkvæma þessi skref fyrir áætlaða, fastáætlaða eða útgefna framleiðslupöntun).
2.  Opna framleiðslupöntunina sem á að áætla og velja síðan **Áætla** aðgerðina.  
3.  Á síðunni **Pantanaáætlun** er smellt á **Reikna áætlun** aðgerðina.  

Síðan birtir áætlanalínur eftir yfirlitsafmörkuninni **Framleiðslueftirspurn** sem þýðir óuppfylltar íhlutalínur allra framleiðslupantana sem eru til. Eftirspurn fyrir aðeins eina framleiðslupöntunina er ekki sýnd vegna þess að nauðsynlegt er að áætla fyrir eina framleiðslupöntun með yfirsýn yfir eftirspurn fyrir hugsanlegar eldri íhlutalínur. Áætlanalínur fyrir framleiðslupöntunina eru stækkaðar.  

## <a name="to-plan-for-any-new-demand"></a>Áætlað fyrir alla nýja eftirspurn  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Pantanaáætlun** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Pantanaáætlun** er smellt á **Reikna áætlun** aðgerðina.
3.  Smellt er á táknið **Stækka (+)** fyrir framan dagsetninguna í reitnum **Dags. eftirsp.** til að sjá undirliggjandi áætlanalínur sem tákna eftirspurnarlínur með ónægt ráðstöfunarmagn.  
4.  Hægt er að sjá gildi fyrir hverja stækkaða áætlunarlínu, þ.e. eftirspurnarlínu, í upplýsingareitunum neðst á síðunni.  

    |Valkostur|Description|  
    |----------------------------------|---------------------------------------|  
    |**Magn í öðrum birgðageymslum**|Sýnir hvort vara er til í annarri birgðageymslu. Þá er hægt að fletta henni upp og velja hana.|  
    |**Staðgenglar eru til**|Sýnir ef staðgengilsvara er búin til fyrir vöruna. Þá er hægt að fletta henni upp og velja hana. Hafa ber í huga að þessi aðgerð á aðeins við um íhluti, þ.e. úr eftirspurnarlínum af tegundinni **Framleiðsla**.|  
    |**Tiltækt magn**|Sýnir heildarráðstöfunarmagn vöru, þ.e. áætlaða stöðu til ráðstöfunar.|  
    |**Fyrsta tiltæka dagsetning**|Sýnir komudagsetningu framboðspöntunar á innleið sem getur uppfyllt það magn sem þarf á dagsetningu sem er eftir eftirspurnardagsetninguna.|  

5.  Í reitnum **Áfyllingarkerfi** er valið hvaða tegund framboðspöntunar á að búa til.  

    Sjálfgefna gildið er gildi birgðaspjaldsins eða birgðahaldseiningaspjalds. Hins vegar er hægt að breyta því í einn af þrem eftirtöldum valkostum:  

    |Valkostur|Description|  
    |----------------------------------|---------------------------------------|  
    |**Innkaup**|Stofnar innkaupapöntun.|  
    |**Millifærsla**|Stofnar millifærslupöntun.|  
    |**Framl.pöntun**|Stofnar framleiðslupöntun.|  

    Í reitnum **Framboð frá** þarf að velja gildi í samræmi við valið áfyllingarkerfi.  

    > [!NOTE]  
    >  Ef reiturinn er ekki útfylltur birtir kerfið villumeldingu þegar aðgerðin **Gera framboðspöntun** er notuð og engin framboðspöntun er búin til fyrir viðkomandi áætlanalínu. Þetta á hins vegar ekki við þegar áfyllingarkerfið er **Framl.pöntun**.  

6.  Úr reitnum **Framboð frá** er leitað að viðeigandi lista og valið hvaðan framboð kemur:  

    - Ef áfyllingarkerfið er **Innkaup** flettir uppflettihnappurinn í reitnum upp á síðunni **Birgðalisti lánardrottins**.  
    - Ef áfyllingarkerfið er **Millifærsla** flettir uppflettihnappurinn í reitnum upp á síðunni **Staðsetningalisti**.  

    Ef varan er til í annarri birgðageymslu sýnir reiturinn **Magn í öðrum birgðageymslum**, neðst, gildi. Þá er hægt að fletta upp og velja birgðageymsluna sem varan á að koma frá þegar millifærslupöntunin er búin til.  

    Ef staðgengill er til fyrir vöruna sem spurt er eftir inniheldur reiturinn **Staðgengill er til** stilltur á **Já**. Þá er hægt að fletta upp á síðunni **Staðgengilsvörufærslur** og velja staðgengil.  

7.  Gátmerki er sett í reitinn **Frátekið** til að stofna frátekningu milli framboðspöntunar sem er verið að stofna og eftirspurnarlínunar pöntunin er gerð fyrir. Reiturinn er sjálfgefið tómur.  

    > [!NOTE]  
    >  Aðeins er hægt að velja þennan gátreit ef varan er **Valfrjálst** eða **Alltaf** í reitnum **Frátekið** á birgðaspjaldinu.  

8.  Í reitnum **Magn til pöntunar** er sett inn magnið sem fer í framboðspöntunina sem stofnuð var.   
    Sjálfgefna gildið er sama magn og það sem er í reitnum **Magn sem þarf**. Á hinn bóginn kann að vera að panta þurfi meira eða minna magn, allt eftir þekkingu á ástandi eftirspurnar. Ef síðan **Pantanaáætlun** sýnir t.d. að nokkrar ótengdar eftirspurnarlínur eru fyrir sömu keyptu vöruna og með svipaða skiladagsetningu er hægt að steypa þeim saman með því að færa heildarmagn þeirra í reitinn **Magn til pöntunar** í einni línu og svo eyða hinum óþörfu áætlanalínunum fyrir umrædda vöru.  

9.  Í reitina **Skiladagur** og **Pöntunardags.** er hægt að færa inn dagsetningarnar sem á að nota á stofnaðar framboðspantanir.  

    Þessir tveir reitir tengjast samkvæmt reitnum **Sjálfgefið öryggisforskot** sem er á síðunni **Framleiðsluuppsetning**. Sjálfgefið er að skiladagur sé sá sami og dagsetning eftirspurnar, en hægt er að breyta þessu að vild.  

> [!NOTE]  
>   Ef færð er inn seinni dagsetning en dagsetning eftirspurnar birtast viðvörunarboð.  

## <a name="to-make-supply-orders"></a>Framboðspantanir gerðar  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlaðar framleiðslupantanir** og veldu síðan tengda tengilinn. Hægt er að framkvæma þessi skref fyrir áætlaða, fastáætlaða eða útgefna framleiðslupöntun.  
2.  Opna framleiðslupöntunina sem á að áætla og velja síðan **Áætla** aðgerðina.  
3.  Bendillinn er færður á viðeigandi áætlunarlínu og smellt á **Búa til pantanir** aðgerðina.  
4.  Á síðunni **Gera framboðspantanir** á flýtiflipanum **Pantanaáætlun** í reitnum **Gera pantanir fyrir** skal velja eitt af eftirfarandi valkostum.  

    |Valkostur|Description|  
    |----------------------------------|---------------------------------------|  
    |**Virka línan**|Gera einungis framboðspöntun fyrir línuna sem bendillinn er á.|  
    |**Virka pöntunin**|Gera framboðspantanir fyrir allar línur í pöntuninni sem bendillinn er á.|  
    |**Allar línur**|Gera framboðspantanir fyrir allar línur á síðunni **Pantanaáætlun**.|  

5.  Á flipanum **Valkostir** er tilgreint hvernig framboðspantanir eða innkaupatillögulínur á að gera.  

    > [!NOTE]  
    >  Þær stillingar sem síðast voru gerðar á síðunni **Gera framboðspantanir** eru vistaðar undir notendakenni þess sem þær gerir þannig að þær eru þær sömu næst þegar sá hinn sami notar síðuna.  

6.  Veldu hnappinn **Í lagi** til að láta forritið búa til þær framboðspantanir eða innkaupatillögulínur sem stungið er upp á.  

Nú hefur verið áætlað fyrir óuppfylltri eftirspurn með því að gera viðeigandi framboðspantanir. Nánari upplýsingar um tiltekin verkflæði þegar síðan **Pantanaáætlun** er notuð fara eftir verklagsreglum viðkomandi fyrirtækis.  

Þegar áætlanavinnu er lokið á síðunni **Pantanaáætlun**, t.d. við að tilgreina annan valkost í útvega magnið, er hægt að byrja á að búa til framboðspantanir fyrir eina eða fleiri áætlanalínur.  

> [!NOTE]  
>  Framboðspantanirnar sem gerðar eru kunna að búa til nýja háða eftirspurn, t.d. fyrir undirliggjandi framleiðslupantanir, og þess vegna ætti að velja aftur **Reikna áætlun** til að finna slíkt og vinna úr því áður en haldið er áfram niður listann.  

## <a name="see-also"></a>Sjá einnig  
[Kynning: Handvirk áætlun birgða](walkthrough-planning-supplies-manually.md)  
[Áætlun](production-planning.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
