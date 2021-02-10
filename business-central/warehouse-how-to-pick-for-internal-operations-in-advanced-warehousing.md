---
title: Tína fyrir innri starfsemi með ítarlegum vöruhúsaskilgreiningum
description: Ef birgðageymslurnar nota tiltekt sem og sendingu skal velja íhluti fyrir framleiðslu og samsetningaraðgerðir á tiltektarsíðu vöruhúss.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8c1f51e722e3ec41e4c31170dca8ea891e9786e2
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014076"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss
Í ítarlegri vöruhúsastillingu þar sem birgðageymslan notar tínslu auk afhendingar eru íhlutir tíndir fyrir framleiðslu- og samsetningarverkþætti á síðunni **Vöruhús - Tína**.  

Einnig er hægt að nota síðuna **Vinnublað hreyfingar** til að færa vörur milli hólfa á tilfallandi hátt, þ. e. a. án tilvísunar í upprunaskjal. Frekari upplýsingar eru í [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Upplýsingar um tínslu atriða fyrir innri starfsemi í einföldum vöruhúsum sem hafa aðeins verið sett upp fyrir tínslu eru í [Færa íhluti á aðgerðasvæði með einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni þar sem í tínsluaðgerð er alltaf hluti af verkflæði, annað hvort sem dráttur eða ýting.  

Einnig er hægt að stofna vöruhúsatínsluskjöl eins og ýtingu í glugganum **Stofna vöruhússtínslu** á upprunaskjalinu, eins og útgefna samsetningarpöntun eða vöruhúsaafhendingu. Frekari upplýsingar, sjá [Tína Vörur með vöruhúsatínslu](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Einnig er hægt að stofna vöruhúsatínsluskjal eins og drátt með því að nota síðuna **Vinnublað tínslu** til að finna tínslubeiðnir, bæði til afhendingar og innri aðgerða, og síðan stofna nauðsynleg vöruhúsatínsluskjöl.  

Eftirfarandi ferli skýrir dæmi þar sem valdir eru íhlutir fyrir afhenta framleiðslupöntun á síðunni **Vinnublað tínslu**. Ferlið á einnig við fyrir samsetningarpöntun.  

Til að stofna tínslubeiðnir, bæði fyrir tog- og ýtidæmi, þurfa viðkomandi upprunaskjöl að vera útgefin. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun|Breyta tegund pöntunar í útgefna framleiðslupöntun.|  
|Samsetningarpöntun|Breyta stöðu í Útgefið.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Íhlutir tíndir úr tínsluvinnublöðunum  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tínsluvinnublöð** og veldu síðan tengda tengilinn.  
2.  Velja skal **Sækja vöruhúsaskjöl** og síðan velja íhlutalínurnar í útgefnu framleiðslupöntuninni.  
3.  Línurnar eru skoðaðar, þeim raðað til að tryggja skilvirkni tínsluferðarinnar og þær sameinaðar öðrum vinnublaðslínum ef þarf, til að nýta tíma starfsmanna sem best.  
4.  Veldu aðgerðina **Stofna tínslu**.  
5.  Skilgreina hvernig eigi að stofna vöruhúsatínsluskjöl og hvernig á að raða tínslulínunum með því að fylla út reiti á síðunni **Stofna tínslu**.  
6.  Velja hnappinn **Í lagi**. Vöruhúsatínsluskjöl eru búin til með tínslulínum fyrir hvern íhlut sem er krafist í innri aðgerð.  

Ef svæði innri starfsemi, s.s. framleiðsluvinnusalur, er sett upp með sjálfgefnu hólfi fyrir staðsetningu íhluta sem notaðir eru verður kóti þess hólfs settur inn í Setja-línur í tínsluskjali vöruhússins til að leiðbeina starfsmönnum í vöruhúsi um hvert setja eigi vörurnar. Nánari upplýsingar má nálgast á **Hólfkóði til framleiðslu** eða **Í samsetningu hólfakóð** reitina.

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið
Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfa](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Sjá einnig
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
