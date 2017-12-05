---
title: Setja upp gagnaskipti | Microsoft Docs
description: "Setja upp gagnaskiptarammann í Dynamics 365 Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 593904835c55d4ce9b137d0af387ea897603795f
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-data-exchange"></a>Setja upp gagnaskipti
Áður en hægt er að senda og taka á móti rafrænum skjölum eða flytja inn og út bankaskrár verður að setja upp gagnaskiptaumgjörð til að vinna úr umræddum skjölum. Auk þess verður að setja upp tengd svæði, t.d. aðalgögn fyrir viðskiptamenn sem fá senda rafræna reikninga eða umskráningarþjónusta fyrir bankagögn í tilvikum þar sem nota þarf utanaðkomandi þjónustuaðili til að umbreyta bankaskrám. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).  

 Þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] er sett upp fyrir gagnaskipti við ytri skrár geta notendur notað uppsetningu í almennum viðskiptaverkum, s.s. að senda og taka á móti rafrænum skjölum og flytja inn og út bankaskrár.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp forstillta skjalaskiptaþjónustu til að hægt sé að senda og taka á móti rafrænum skjölum frá og til [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Hvernig á að setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md)|  
|Setja upp forstillta OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í færslur fyrir skjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Hvernig á að: Setja upp skjöl á innleið](across-how-setup-income-documents.md)|  
|Setja upp eina af tveimur forstilltum þjónustu til að fá nýjasta gengi gjaldmiðils í gluggann **Gengi gjaldmiðils**.|[Hvernig á að: Uppfæra gengi](finance-how-update-currencies.md)|  
|Setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, lánardrottna, atriði, og mælieiningar, sem tengjast vörpunargögnum í [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Hvernig á að: Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Setja upp bankareikning, lánardrottin og greiðslubók fyrir SEPA-millifærslur.|[Hvernig á að: Setja upp SEPA-kreditfærslur](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Undirbúið bankareikningssnið, greiðsluaðferðir og samninga við viðskiptavini um SEPA-beingreiðslur.|[Hvernig á að: Setja upp SEPA-beingreiðslur](finance-how-to-set-up-sepa-direct-debit.md)|  
|Setja upp sannvottun notanda og slóðina á þjónustuveitu bankagagnaumbreytingar sem þarf að hafa banka skrá umbreyttir til snið bankans þíns.|[Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md)|  
|Setja upp og virkja utanaðkomandi þjónustu sem gerir kleift að flytja inn bankayfirlit beint sem bankastreymi.|[Hvernig á að: Setja upp bankayfirlitsþjónustu](bank-how-setup-bank-statement-service.md)|  
|Eftir að bankayfirlitsþjónusta er gerð virk skal tengja bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Hvernig á að setja upp Bankareikninga](bank-how-setup-bank-accounts.md)|  
|Undirbúið að setja upp nýja gagnaskiptaskilgreiningu fyrir tiltekna gagnaskrá eða straum með því að nota XML-skema skrárinnar til að fylla út í flýtiflipann **Dálkskilgreiningar** í glugganum **Bókunarskilgreining**.|[Hvernig á að. Nota XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Setja upp Data Exchange Framework til að gera notendum kleift að taka á móti nýju sniði innkaupaskjala, senda ný snið söluskjala, flytja inn nýjar bankaskrá eða önnur gagnaskipti.|[Hvernig á að: Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Sjá einnig  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Gagnaskipti](across-exchange-data.md)   
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

