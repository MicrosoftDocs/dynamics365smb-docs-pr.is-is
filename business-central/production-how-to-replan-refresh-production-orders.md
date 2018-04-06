---
title: "Hvernig skal enduráætla eða uppfæra framleiðslupantanir beint| Microsoft Docs"
description: "Í framleiðslupöntunarlínunum eru vörur sem vinna á í framleiðslupöntuninni."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a2bfabbb680233fad7e578d6de6340cd26bdc1db
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="replan-or-refresh-production-orders-directly"></a>Enduráætla eða uppfæra framleiðslupantanir beint
Aðgerðin **Enduráætla** er venjulega notuð eftir íhlutum, sem standa fyrir undirliggjandi framleiðslupantanir, hefur verið bætt við eða þeim breytt. Þessi áætlunaraðgerð reiknar breytingar sem gerðar eru á íhlutum og leiðarlínum. Hún tekur með vörur í neðri framleiðsluuppskriftum og kann að stofna nýjar framleiðslupantanir fyrir þær.  

Aðgerðin Enduráætla byggir útreikninga og áætlun á nýrri eftirspurn fyrir framleiðslupöntun á breytingum sem gerðar hafa verið á íhlutum og leiðarlínum.  

Virknin **Uppfæra** á framleiðslupantanir er venjulega notuð eftir að gert er eitt af eftirfarandi:

- Stofnaði framleiðslupöntunarhaus handvirkt til að reikna og búa til línugögn í fyrsta skipti.
- Gerði breytingar á framleiðslupöntunarhaus til að endurreikna öll línugögn.

Uppfæra virknin reiknar breytingar sem gerðar eru á framleiðslupantanahaus og tekur ekki með framleiðsluuppskriftarstig. Aðgerðin reiknar og virkjar gildi íhluta- og leiðarlínanna í samræmi við aðalgögnin, sem skilgreind eru í úthlutaðri framleiðsluuppskrift og leið, eftir pantanamagni og skiladegi í haus framleiðslupöntunar.

Hægt er að setja framleiðslulínur inn handvirkt eða nota aðgerðina sem reiknar framleiðslupöntunarlínurnar úr hausnum.  

> [!NOTE]
> Ef aðgerðin Uppfæra er notuð til að endurreikna framleiðslupöntunarlínur, er eldri framleiðslupöntunarlínunum eytt og nýjar línur eru reiknaðar.  

## <a name="to-replan-a-production-order"></a>Enduráætla Framleiðslupöntun  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Fastáætluð framleiðslupöntun** og velja svo viðeigandi tengil.  
2.  Opna framleiðslupöntunina sem á að enduráætla.  
3.  Á flýtiflipanum **Línur** skal velja aðgerðina **Línur**, og velja svo aðgerðina **Íhlutir**.  
4.  Íhlut, sem er framleidd vara epa millivara, er bætt við.  
5.  Frá framleiðslupöntuninni, veldu **Enduráætla** aðgerðina.  

    Í glugganum **Enduráætla framleiðslupöntun** er tilgreint hvernig og hvað á að enduráætla.  
6.  Í reitnum **Stefna tímasetningar** veljið einn eftirfarandi valkost.  

    |Valkostur|Description|  
    |----------------------------------|---------------------------------------|  
    |**Afturvirk**|Reiknar aðgerðaröðina afturábak frá fyrstu mögulegu lokadagsetningu (skilgreind af skiladegi og/eða öðrum dagsettum pöntunum) að síðustu mögulegu upphafsdagsetningunni. **Til athugunar: Þessi sjálfgefni valkostur á við í flestum tilvikum.**|  
    |**Framvirk**|Reiknar aðgerðaröðina áfram frá fyrstu mögulegu upphafsdagsetningu (skilgreind af skiladegi og/eða öðrum dagsettum pöntunum) að fyrstu mögulegu lokadagsetningu. **Athugið:** Þessi valkostur á aðeins við um hraðpantanir.|  

7.  Í reitnum **Áætla** er valið hvort reikna á framleiðslukröfur fyrir framleidda vöru á framleiðsluuppskrift, með eftirfarandi hætti:  

    |Valkostur|Description|  
    |----------------------------------|---------------------------------------|  
    |**Engin stig**|Lægri stig framleiðslu ekki tekin með. Þetta uppfærir aðeins tímasetningu vöru (líkt og endurnýjun).|  
    |**Eitt stig**|Áætla eftirspurn fyrir framleiðslu á fyrsta stigi. Hægt er að stofna fyrsta stigs framleiðslupantanir.|  
    |**Öll stig**|Áætla eftirspurn fyrir framleiðslu á öllum stigum. Hægt er að stofna framleiðslupantanir fyrir öll stig.|  

8.  **Eitt stig** er valið og smellt á **Í lagi** til að enduráætla framleiðslupöntunina, auk þess að reikna og stofna nýja undirliggjandi framleiðslupöntun fyrir nýju millivöruna – ef hún er ekki alveg til.  

> [!NOTE]  
>  Breytingar sem gerðar eru með aðgerðinni **Enduráætla** hafa að öllum líkindum í för með sér breytingar á afkastaþörf framleiðslupöntunarinnar og því gæti þurft að endurtímasetja aðgerðir í kjölfarið.  

## <a name="to-refresh-a-production-order"></a>Framleiðslupöntun endurnýjuð  
Ef framleiðslupöntunarlínunum, íhlutum eða leiðarlínum hefur verið breytt þarf einnig að uppfæra upplýsingar um framleiðslupöntun. Eftirfarandi aðferð sýnir hvernig íhlutirnir eru reiknaðir fyrir fastáætlaða framleiðslupöntun. Skrefin eru svipuð fyrir Leiðarlínur.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Fastáætluð framleiðslupöntun** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð. Frekari upplýsingar eru í [Stofna framleiðslupantanir](production-how-to-create-production-orders.md).  
3.  Velja aðgerðina **Uppfæra**.
4. Í glugganum **Uppfæra framleiðslupöntun** velurðu einn af eftirfarandi kostum:

    |Valkostur|Description|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Stefna tímasetningar**|**Framvirkt**|Áætlunin hefst á upphafsdagsetningu og heldur áfram (að lokadagsetningunni). Fylla verður inn upphafsdagsetningu til að nota þennan valkost.|  
    ||**Afturvirk**|Áætlunin hefst á lokadagsetningunni og heldur afturábak (að upphafsdagsetningu).|  
    |**Reikna**|**Línur**|Veljið þennan reit til að reikna framleiðslupöntunarlínur.|  
    ||**Leiðir**|Þessi reitur hefur engin áhrif á útreikning framleiðslulína.|  
    ||**Íhlutaþörf**|Þessi reitur hefur engin áhrif á útreikning framleiðslulína.|  
    |**Vöruhús**|**Stofna innleiðarbeiðni**|Þessi reitur hefur engin áhrif á útreikning framleiðslulína.|  

5. Velja **Í lagi** til að staðfesta valið. Framleiðslupöntunarlínurnar hafa nú verið reiknaðar.

> [!NOTE]  
>  Þegar framl.pöntunaríhlutir eru reiknaður eyðast fyrri breytingar á íhlutunum.

## <a name="see-also"></a>Sjá einnig  
[Áætlun](production-planning.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

