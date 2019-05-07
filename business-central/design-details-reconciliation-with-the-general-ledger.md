---
title: Hönnunarupplýsingar - Afstemming í fjárhagur | Microsoft Docs
description: Þetta efnisatriði lýsir afstemmingu í fjárhag Þegar birgðafærslur eins og söluafhendingar, framleiðslufrálag eða neikvæðar leiðréttingar eru bókaðar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, reconciliation, general ledger, inventory
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2cb3e743dfd28e96a404209f086caa3f9e84be6c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "928982"
---
# <a name="design-details-reconciliation-with-the-general-ledger"></a>Hönnunarupplýsingar: afstemming í fjárhagur
Þegar birgðafærslur eins og söluafhendingar, framleiðslufrálag eða neikvæðar leiðréttingar eru bókaðar eru magnið og gildisbreytingarnar í birgðunum skráð í birgðafærslunum og virðisfærslurnar, hvort í sínu lagi. Næsta skrefið í ferlinu er að bóka birgðagildin í birgðareikningana í fjárhagnum.  

Tvær aðferðir eru til að afstemma birgðabók við fjárhag.  

* Með því að keyra runuvinnsluna **Bóka birgðakostnað á fjárhag** handvirkt.  
* Sjálfkrafa í hvert skipti sem þú bókar birgðafærslu.  

## <a name="post-inventory-cost-to-gl-batch-job"></a>Keyrslan Bóka birgðakostnað á fjárhag  
Þegar runuvinnslan **Bóka birgðakostnað í fjárhag** er keyrð eru fjárhagsfærslur stofnaðar á grundvelli virðisfærslna. Nú hefur þú þann valkost að taka saman fjárhagsfærslur fyrir hverja virðisfærslu eða stofna fjárhagsfærslur fyrir hverja samsetningu bókunardagsetningar. staðsetningarkóða, birgðabókunarflokks, almenns bókunarflokks fyrirtækja og almenns vörubókunarflokks.  

Bókunardagsetningar fjárhagsfærslnanna eru stilltar á bókunardagsetningu samsvarandi virðisfærslu, nema þegar virðisfærslan fellur undir lokað bókhaldstímabil. Í þessu tilviki, virðisfærsla er sleppt, og þú verður að breyta annaðhvort uppsetningu almennrar höfuðbókar eða notandauppsetningu til að virkja bókun á tímabilinu.  

Þegar runuvinnslan **Bóka birgðakostnað í fjárhag** er keyrð gæti kerfið rekist á villur sem hafa með uppsetningu sem vantar að gera eða ósamhæfa víddaruppsetningu. Ef keyrslan rekst á villur í víddaruppsetningunni hefur hún þessar villur að engu og notar víddir virðisfærslunnar. Í tilfelli annarra villna hoppar keyrslan yfir bókun virðisfærslnanna og telur þær upp við lok skýrslunnar í hluta sem heitir **Færslur sem hoppað var yfir**. Til að bóka þessar færslur þarf að leiðrétta villurnar. Hægt er að sjá lista af villum áður en keyrslan er keyrð með því að keyra skýrsluna **Bóka birgðakostnað í fjárhag - Prófun**. Þessi skýrsla inniheldur allar villur sem koma upp í prufubókun. Þá er hægt að laga villurnar og keyra bókunarkeyrslu birgðakostnaðar án þess að sleppa neinum færslum.  

## <a name="automatic-cost-posting"></a>Sjálfvirk kostnaðarbókun  
Til að setja upp kostnaðarbókun í fjárhag til að keyra sjálfkrafa þegar þú bókar birgðafærslu, veldu **Sjálfvirk kostnaðarbókun** gátreitinn á síðunni **Uppsetning birgða**. Bókunardagsetning fjárhagsfærslnanna er sú sama og fyrir bókunardagsetning birgðafærslunnar.  

## <a name="account-types"></a>Gerðir reikninga  
Við afstemmingu, eru birgðarvirði skráð í birgðarreikning í efnahagsreikning. Sama upphæð, með andstætt tákn, er bókuð á viðeigandi mótreikning. Venjulega er jöfnunarreikningur rekstrarreikningur. Hins vegar, þegar þú birtir beinan kostnað vegna neyslu eða framleiðslu, er mótreikningurinn efnahagslykill. Tegund birgðafærslunnar og virðisfærslunnar ákvarðar í hvaða fjárhagsreikning er bókað.  

Færslugerð sýnir hvaða fjárhagsreikning á að bóka í. Þetta er ákvarðað annað hvort með merki magns á birgðafærslu eða virði magns á virðisfærslu, þar sem magn hefur alltaf sama merki. Til dæmis lýsir sölufærsla með jákvæðu magni birgðaminnkun vegna sölu og sölufærsla með neikvæðu magni lýsir birgðaaukningu vegna vöruskila.  

### <a name="example"></a>Dæmi  
Eftirfarandi dæmi sýnir reiðhjólakeðju sem er framleidd úr keyptum hlekkjum. Þetta dæmi sýnir hvernig mismunandi gerðir fjárhagsreikninga eru notaðir í dæmigerðum aðstæðum.  

Gátreiturinn **Áætluð kostnaðarbókun í fjárhag** á síðunni **Uppsetning birgða** er valinn og eftirfarandi uppsetning er tilgreind.  

Eftirfarandi tafla sýnir hvernig hlekkur er settur upp á birgðaspjaldi.  

|Uppsetning reits|Gildi:|  
|-----------------|-----------|  
|**Aðferð kostn.útreiknings**|Staðlað|  
|**Staðlað kostn.verð**|SGM 1.00|  
|**Hlutf. sameiginl. kostn.**|SGM 0.02|  

Eftirfarandi tafla sýnir hvernig keðja er sett upp á birgðaspjaldi.  

|Uppsetning reits|Gildi:|  
|-----------------|-----------|  
|**Aðferð kostn.útreiknings**|Staðlað|  
|**Staðlað kostn.verð**|SGM 150.00|  
|**Hlutf. sameiginl. kostn.**|SGM 25.00|  

Eftirfarandi tafla sýnir hvernig vinnustöð er sett upp á vinnustöðvarspjaldi.  

|Uppsetning reits|Gildi:|  
|-----------------|-----------|  
|**Innkaupsverð**|SGM 2.00|  
|**Óbeinn kostnaður prósenta**|10|  

##### <a name="scenario"></a>Aðstæður  
1. Notandinn kaupir 150 tengla og bókar innkaupapöntunina samkvæmt móttöku. (Innkaup)  
2. Notandinn bókar innkaupapöntunina samkvæmt reikningi. Þetta stofnar sameiginlegan kostnað upp á SGM 3.00 sem á að úthluta og fráviksupphæð upp á 18.00. (Innkaup)  

    1. Bráðaðbirgðareikningar eru hreinsaðir. (Innkaup)  
    2. Beinn kostnaðurinn er bókaður. (Innkaup)  
    3. Óbeini kostnaðurinn er reiknaður út og bókaður. (Innkaup)  
    4. Frávik innkaupanna eru reiknuð út og bókuð (aðeins fyrir vörur á stöðluðu kostnaðarverði). (Innkaup)  
3. Notandinn selur eina keðju og bókar sölupöntunina sem afgreidda. (Sala)  
4. Notandinn bókar sölupöntunina samkvæmt reikningi. (Sala)  

    1. Bráðaðbirgðareikningar eru hreinsaðir. (Sala)  
    2. Kostnaður seldra vara (cogs) er bókaður. (Sala)  

        ![Niðurstöður sölubókunar á fjárhagsreikninga](media/design_details_inventory_costing_3_gl_posting_sales.png "Niðurstöður sölubókunar á fjárhagsreikninga")  
5. Notandinn bókar notkun 150 tengla, sem er fjöldi tengla sem það tekur að stofna eina keðju. (notkun, efni)  

    ![Niðurstöður efnisbókunar á fjárhagsreikninga](media/design_details_inventory_costing_3_gl_posting_material.png "Niðurstöður efnisbókunar á fjárhagsreikninga")  
6. Vinnustöðin notar 60 mínútur til að framleiða keðjuna. Notandinn bókar umbreytingakostnað. (Notkun, Afkastaveita)  

    1. Beinn kostnaður er bókaður. (Notkun, Afkastaveita)  
    2. Óbeinn kostnaður eru reiknuð og staða. (Notkun, Afkastaveita)  

        ![Niðurstöður afkastagetubókunar á fjárhagsreikninga](media/design_details_inventory_costing_3_gl_posting_capacity.png "Niðurstöður afkastagetubókunar á fjárhagsreikninga")  
7. Notandinn bókar væntanlegan kostnað einnar keðju. (frálag)  
8. Notandinn lýkur framleiðslupöntuninni og keyrir **Kostnaðarleiðrétting - Birgðafærslur** runuvinnsluna. (frálag)  

    1. Bráðaðbirgðareikningar eru hreinsaðir. (frálag)  
    2. Beinn kostnaður færist af VÍV-reikningi á birgðareikning. (frálag)  
    3. Óbeini kostnaðurinn (stjórnunarkostnaður´) er fluttur af kostnaðarreikningi óbeins kostnaðar yfir á birgðarreikning. (frálag)  
    4. Þetta leiðir til dreifni fjárhæðar í staðbundinni mynt 157,00. Frávik eru aðeins reiknað fyrir staðlaða kostnaðarliði. (frálag)  

        ![Niðurstöður úttaksbókunar á fjárhagsreikninga](media/design_details_inventory_costing_3_gl_posting_output.png "Niðurstöður úttaksbókunar á fjárhagsreikninga")  

        > [!NOTE]  
        >  Til einföldunar er aðeins sýndur einn fráviksreikningur. Í raun eru til fimm mismunandi reikningar:  
        >   
        >  * Hráefnisfrávik  
        >  * Getufrávik  
        >  * Fráv. sameiginl. kost. afk.getu  
        >  * Frávik undirverktaka  
        >  * Sameiginl. kostn.frávik framleiðslu  

9. Notandinn endurmetur keðjuna úr SGM 150.00 í SGM 140.00. (Leiðrétting/endurmat/Sléttun/millifærsla)  

    ![Niðurstöður leiðréttingarbókunar á fjárhagsreikninga](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Niðurstöður leiðréttingarbókunar á fjárhagsreikninga")  

Frekari upplýsingar um vensl milli reikningsgerða og mismunandi gerðir virðisfærslna eru í [Hönnunarupplýsingar: Reikningar í fjárhag](design-details-accounts-in-the-general-ledger.md).  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
[Hönnunarupplýsingar: Væntanleg kostnaðarfærsla](design-details-expected-cost-posting.md)   
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)
[Stjórna birgðakostnaði](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
