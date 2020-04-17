---
title: Áætla vinnslur vöruhúss | Microsoft Docs
description: Dreifingaráætlun fyrirtækis endurspeglast í grunnstillingu á vinnslum vöruhúss. Í henni felst skilgreining á því hvernig mismunandi vörur eru meðhöndlaðar í mismunandi vöruhúsum, til dæmis stig hólfastýringar og umfang nauðsynlegs verkflæðis á milli vöruhúsaaðgerða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: afb9f2d21b0b343846b2f0ba7143ea090433a8aa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195953"
---
# <a name="setting-up-warehouse-management"></a>Vöruhúsastjórnun sett upp
Dreifingaráætlun fyrirtækis endurspeglast í grunnstillingu á vinnslum vöruhúss. Í henni felst skilgreining á því hvernig mismunandi vörur eru meðhöndlaðar í mismunandi vöruhúsum, til dæmis stig hólfastýringar og umfang nauðsynlegs verkflæðis á milli vöruhúsaaðgerða.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Fá yfirlit yfir afkastagetu einfaldrar vöruhúsavirkni samanborið við ítarlega vöruhúsavirkni.|[Hönnunarupplýsingar: Yfirlit vöruhúss](design-details-warehouse-overview.md)|  
|Setja upp átta mismunandi gerðir hólfa, til dæmis Tínsluhólf, til þess að skilgreina flæðisaðgerðir sem tengjast hverri gerð hólfs.|[Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md)|  
|Stofna hólf, annað hvort sjálfvirkt eða handvirkt, með upplýsingum eins og heiti, númeraröð og flokk, samkvæmt hólfasniðmáti.|[Stofna hólf](warehouse-how-to-create-individual-bins.md)|  
|Skilgreina hvaða vörur á að geyma í tilteknu hólfi og búa til reglur sem ákvarða hvenær hólf er fyllt með tiltekinni vöru.|[Stofna innihald hólfs](warehouse-how-to-set-up-bin-contents.md)|  
|Stilla að tiltekin vara sé alltaf sett í tiltekið hólf.|[Sjálfgefin hólf tengd vörum](warehouse-how-to-assign-default-bins-to-items.md)|
|Stofna sniðmát til að ráða hvar og hvernig er gengið frá vörum í beinum frágangi.|[Setja upp frágangssniðmát](warehouse-how-to-set-up-put-away-templates.md)|
|Setja notendur upp sem vöruhúsastarfsmenn í tilteknum birgðageymslum.|[Setja upp vöruhúsastarfsmenn](warehouse-how-to-set-up-warehouse-employees.md)|
|Skilgreina mismunandi gerðir hólfa í vöruhúsi til þess að stýra hvar vörum er komið fyrir eftir gerð þeirra, flokkun eða meðhöndlunarstigi.|[Setja upp birgðageymslur til að þær noti hólf](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Gera viðbótarstillingar fyrir núverandi birgðageymslu til að virkja hana fyrir vöruhúsaaðgerðir.|[Breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Virkja tínslu, hreyfingu og frágang fyrir samsetningar- eða framleiðslupantanir í einfaldri grunngerð vöruhúss.|[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Setja vörur og birgðageymslur upp fyrir ítarlegasta umfang vöruhúsastjórnunar þar sem allar aðgerðir verða að fylgja ströngu vinnuflæði.|[Setja upp vörur og birgðageymslur fyrir beinan frágang og tínslu](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Skilgreina hvenær og hvernig vörur í birgðageymslum eru taldar vegna viðhalds eða fjárhagsskýrslugerðar.|[Talning, breytingar eða endurflokkun birgða](inventory-how-count-adjust-reclassify.md)|
|Gera vöruhúsastarfsmönnum kleift að brjóta stærri mælieiningu niður í smærri mælieiningar til að uppfylla þarfir upprunaskjala.|[Virkja sjálfvirk einingaskipti með beinum frágangi og tínslu](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Setja upp vöruhús þannig að það stingi sjálfkrafa upp á vörum til tínslu sem munu renna út fyrstar.|[Virkja tínslu eftir FEFO](warehouse-picking-by-fefo.md)|
|Fá ábendingar um hvernig á að endurskipuleggja birgðageymslur, hólf eða svæði til þess að auka skilvirkni vöruhúsaaðgerða.|[Endurskipulagning vöruhúsa](warehouse-how-to-restructure-warehouses.md)|
|Samlaga strikamerkjalesara að vöruhúsakerfislausninni. Eingöngu fyrir uppsetningu á staðnum.|[Nota sjálfvirkt gagnatökukerfi (ADCS)](warehouse-use-automated-data-capture-systems-adcs.md)|

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
