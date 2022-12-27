---
title: Tína fyrir innri starfsemi með ítarlegum vöruhúsaskilgreiningum
description: Ef birgðageymslurnar nota tínslu og afhendingu skal velja tínsluíhluti fyrir framleiðslu, samsetningu og verkaðgerðir á síðu vöruhúsatínslunnar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607554"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Tínsla fyrir framleiðslu, samsetningu eða verk í ítarlegum vöruhúsastillingum

Í ítarlegum vöruhúsastillingum þar sem staðsetningin er sett upp til að nota tínslu og afhendingu er hægt að tína íhluti fyrir framleiðslu- og samsetningarverkþætti á síðunni **Vöruhúsatínsla**.  

Einnig er hægt að nota síðuna **Hreyfingavinnublað** til að flytja vörur á milli hólfa á tilfallandi hátt án vísunar í upprunaskjal. Frekari upplýsingar eru í [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Upplýsingar um tínslu vara í birgðageymslu í einföldu vöruhúsi sem eru aðeins settar upp fyrir tínslu er að finna í [Færa íhluti yfir á aðgerðasvæði í einfaldri vöruhúsastillingu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni þar sem í tínsluaðgerð er alltaf hluti af verkflæði, annað hvort sem dráttur eða ýting.  

Einnig er hægt að stofna vöruhúsatínsluskjöl eins og ýtingu í glugganum **Stofna vöruhússtínslu** á upprunaskjalinu, eins og útgefna samsetningarpöntun eða vöruhúsaafhendingu. Frekari upplýsingar, sjá [Tína Vörur með vöruhúsatínslu](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Einnig er hægt að búa til tínsluskjal vöruhúss með drætti með því að nota síðuna **Tínsluvinnublað** til að finna tínslubeiðnir. Þessi aðferð er gagnleg fyrir afhendingu og innri aðgerðir. Síðan er hægt að búa til nauðsynleg tínsluskjöl vöruhúss.  

Eftirfarandi ferli skýrir dæmi þar sem valdir eru íhlutir fyrir afhenta framleiðslupöntun á síðunni **Vinnublað tínslu**. Ferlið á einnig við fyrir samsetningarpöntun.  

Til að stofna tínslubeiðnir, bæði fyrir tog- og ýtidæmi, þurfa viðkomandi upprunaskjöl að vera útgefin. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun|Breyta tegund pöntunar í útgefna framleiðslupöntun.|  
|Samsetningarpöntun|Breyta stöðu í Útgefið.|
|Verk | Breyttu stöðu í opna.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Íhlutir tíndir úr tínsluvinnublöðunum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  
2. Velja skal **Sækja vöruhúsaskjöl** og síðan velja íhlutalínurnar í útgefnu framleiðslupöntuninni.  
3. Raðaðu línunum til að tryggja skilvirka tínslu. Þú gætir viljað sameina línur til að spara tíma starfsmanna.  
4. Veldu aðgerðina **Stofna tínslu**.  
5. Skilgreina hvernig eigi að stofna vöruhúsatínsluskjöl og hvernig á að raða tínslulínunum með því að fylla út reiti á síðunni **Stofna tínslu**.  
6. Velja hnappinn **Í lagi**. Vöruhúsatínsluskjöl eru búin til með tínslulínum fyrir hvern íhlut sem er krafist í innri aðgerð.  

Rekstrarsvæði eins og framleiðslugólf gætu verið með sjálfgefið hólf fyrir íhluti sem þarf á að halda. Ef svo, þá er sjálfgefnum hólfakóða bætt við tínsluskjal vöruhússins til að gefa til kynna hvar á að setja vörurnar. Frekari upplýsingar er að finna í ábendingum fyrir reitina **Hólfakóði framleiðslu á innleið** eða **Hólfakóði samsetningar á innleið**.

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið

Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfs.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
