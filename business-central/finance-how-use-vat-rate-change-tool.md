---
title: Notkun breytingaverkfæris VSK-hlutfalls | Microsoft Docs
description: Notkun breytingaverkfæris VSK-hlutfalls
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992229"
---
# <a name="use-the-vat-rate-change-tool"></a>Notkun breytingaverkfæris VSK-hlutfalls

## <a name="understanding-the-vat-rate-conversion-process"></a>Að skilja umbreytingarferli VSK-hlutfalls.  
VSK-hlutfall breytingarverkfærið umreiknar VSK-hlutfall fyrir aðalgögn, færslubækur og pantanir á mismunandi hátt. Valin aðalgögn og færslubækur verða uppfærð af nýja almenna vörubókunarflokknum eða VSK-vörubókunarflokki. Ef pöntun hefur verið afhent að fullu eða að hluta munu afhentar vörur halda almenna vörubókunarflokknum eða VSK-vörubókunarflokknum. Ný pöntunarlína verður stofnuð fyrir óafhentar vörur og uppfærð til að samræma núverandi og nýtt VSK eða almenna vörubókunarflokka. Úthlutanir kostnaðarauka, frátekningar og vörurakningarupplýsingar uppfærast einnig í samræmi við það.  

Það eru nokkrir hlutir sem verkfærið getur ekki umbreytt:

* Sölu-eða innkaupapöntunum og reikningum þar sem sendingar hafa verið bókaðar. Þessi skjöl eru bókuð með gildandi VSK-hlutfalli.  
* Skjölum sem hafa bókaða fyrirframgreiðslureikninga. Til dæmis gæti notandi hafa greitt eða móttekið fyrirframgreiðslur á reikningum sem eru ekki loknir áður en breytingaverkfærið VSK-hlutfall er notað. Í þessu tilviki verður mismunur á vsk sem er á gjalddaga og vsk sem hefur verið borgaður í fyrirframgreiðslum þegar reikningnum er lokið. Breytingarverkfæri VSK-hlutfalls sleppir þessum skjölum og það þarf að uppfæra þau handvirkt.  
* Beinum afhendingum eða sérpöntunum.  
* Sölu- eða innkaupapöntunum með samhæfingu vöruhúsa ef þær eru að hluta sendar eða mótteknar.  
* Þjónustusamninga.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Til að undirbúa umreikning VSK-hlutfalls  
Áður en breytingaverkfæri VSK-hlutfalls er sett upp þarf að velja úr eftirfarandi.

* Ef mismunandi hlutföll eru notuð í færslum þarf að búa til nýjar fjárhagsreikninga fyrir hvert hlutfall eða nota gagnaafmarkanir til að flokka færslur eftir hlutfalli.  
* Ef stofnaðir eru nýir fjárhagsreikningar þarf að stofna nýja almenna bókunarflokka.  
* Til að fækka fylgiskjölum sem er breytt skal bóka eins mörg fylgiskjöl og mögulegt er og halda óbókuðum skjölum í lágmarki.  
* Taka öryggisafrit af gögnum.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Til að setja upp breytingaverkfæri VSK-hlutfalls  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning VSK hlutfall breytingar** og veldu síðan tengda tengilinn.  
2. Á flýtiflipunum **Aðalgögn**, **Færslubækur** og **Skjöl** skal velja gildi bókunarflokks af valkostalistanum fyrir nauðsynlega reiti. Í hverjum flokki er hægt að velja hvort eigi að umbreyta VSK-vörubókunarflokkum eða almennum vörubókunarflokkum eða umbreyta báðum gildunum ef þau eru tiltæk í aðalgagnavörunni. Fyrir sum svæði er einnig hægt að setja afmörkun til að umbreyta aðeins hlutmengi gildanna, til dæmis fjárhagsreikningum. 

### <a name="to-set-up-product-posting-group-conversion"></a>Til að setja upp vörubókunarflokksumbreytingar  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning VSK hlutfall breytingar** og veldu síðan tengda tengilinn.  
2. Á síðunni **Uppsetning á breytingu VSK-hlutfalls** skal annaðhvort velja aðgerðina **Umreikna VSK-vörubókunarflokk** eða **Umreikna almennan vörubókunarflokk**.  
3. Í reitnum **Frá kóða** er færður inn núverandi bókunarflokkur.  
4. Í reitnum **Til kóða** er færður inn nýr bókunarflokkur.  

### <a name="to-perform-vat-rate-change-conversion"></a>Til að umreikna VSK-hlutfall  
Breytingarverkfæri VSK-hlutfalls er notað til að stjórna breytinum á stöðluðu VSK-hlutfalli. VSK og útreikningar almenns vörubókunarflokks eru notaðir til að breyta VSK-hlutfalli og viðhalda nákvæmum VSK-skýrslum. Eftirfarandi breytingar eru gerðar, allt eftir uppsetningu:  

* VSK og almennum bókunarflokkum er umbreytt.  
* Breytingar eru innleiddar í fjárhagsreikninga, viðskiptamenn, lánardrottna, opin skjöl, bókarlínum, o.s.frv.  

> [!IMPORTANT]  
>  Áður en þú umreiknar VSK-hlutfallsbreytingu, er hægt að prófa umreikninginn. Til að gera það, skal fylgja eftirfarandi skrefum, en vertu viss um að hafa auða gátreitina **Framkvæma umreikning** og **VSK hlutfall breytingarverkfæri lokið**. Við prófun á umreikningi er reiturinn **Umbreytt** í töflu **Breyting á VSK gengi í skráningarfærslu** hreinsað og reiturinn **Umbreytt dagsetning** í töflunni **Breyting á VSK gengi í skráningarfærslu** auður. Þegar umreikningnum er lokið, skal velja **Breytingaskrárfærslur fyrir VSK-hlutfall** til að skoða niðurstöður af prufuumreikningnum. Staðfesta hverja færslu áður en umreikningur er framkvæmdur. Sérstaklega skal staðfesta færslur sem nota eldra VSK-hlutfall.     

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Breytingar á VSK-hlutfalli** og veldu síðan **Uppsetning breytinga á VSK-hlutfalli** hlekkinn.  
2. Staðfesta að VSK-vörubókunarflokksumbreytingar eða almennar vörubókunarflokksumbreytingar hafi þegar verið settar upp.  
3. Velja skal gátreitinn **Framkvæma umreikning**.  

    > [!IMPORTANT]  
    >  Hreinsa gátreitinn **breytingaverkfæri fyrir VSK gengi lokið**. Gátreiturinn er valinn sjálfvirkt þegar umreikningi vsk-stigs er lokið.  

4. Velja skal **Umreikna** aðgerðina.  
5. Þegar umreikningnum er lokið, skal velja aðgerðina **Breytingaskrárfærslur fyrir VSK-hlutfall** til að skoða niðurstöður umreiknings.  

> [!IMPORTANT]  
>  Eftir prófun á umreikningi er reiturinn **Umbreytt** í töflu **Breyting á VSK gengi í skráningarfærslu** valinn og reiturinn **Umbreytt dagsetning** í töflunni **Breyting á VSK gengi í skráningarfærslu** sýnir umreiknuðu dagsetninguna.  
## <a name="see-also"></a>Sjá einnig  
[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Uppsetning á óinnleystum virðisaukaskatti](finance-setup-unrealized-vat.md)      
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Staðbundin virkni í Business Central](about-localization.md)
