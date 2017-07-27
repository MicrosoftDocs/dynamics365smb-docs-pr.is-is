---
title: "Leiðrétta birgðakostnað handvirkt| Microsoft Docs"
description: "Þú getur leiðrétt birgðaverðmat vöru með því að nota FIFO eða Meðalkostnaðaraðferð, til dæmis þegar vöruverð breytist ekki vegna viðskiptalegra ástæðna, heldur einhvers annars."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Hvernig á að: Leiðrétta birgðakostnað handvirkt
Kostnaðarverð vöru (birgðavirði) sem er keypt og seld síðar getur breyst á líftímanum, til dæmis vegna þess að kostnað við frakt er bætt við innkaupakostnaðinn þegar varan hefur verið seld. Kostnaðaraðlögun er sérstaklega viðeigandi í aðstæðum þar sem þú selur vörur áður en þú reiknar kaupin á þeim vörum. Til þess að vita alltaf rétt birgðavirði verður því að leiðrétta kostnaðarverð vöru reglubundið. Þetta tryggir að sölu- og hagnaðartölur séu réttar og afkastavísar (KPI) fjárhags séu réttir.

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] eru kostnaðarkostnaður sjálfkrafa leiðrétt í hvert skipti sem viðskiptin eiga sér stað, svo sem þegar þú sendir inn innkaupareikning fyrir hlut.

Þú getur einnig notað aðgerð til að breyta kostnaði við einn eða fleiri hluti handvirkt. Þetta er gagnlegt, til dæmis þegar þú veist að kostnaður hlutar hefur breyst af öðrum ástæðum en vörufærslu.

Kostnaðarverð er leiðrétt með FIFO eða Meðalkostnaðaraðferð, það fer eftir vali þínu í **Uppsetning fyrirtækis** í uppsetning með aðstoð. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

Ef þú notar FIFO kostnaðaraðferð, þá er einingarverð vöru raunvirði sérhverrar innhreyfingar vörunnar. Fyrir verðmat birgða, er gert ráð fyrir að vörur sem settar voru fyrst í birgðir seljist fyrst.

Ef þú notar Meðalkostnaðaraðferð, er einingaverð vara reiknað út sem meðaleiningaverð á hverjum tímapunkti eftir innkaup. Fyrir verðmat birgða, er gert ráð fyrir að allar birgðir verði seldar á sama tíma.

Kostnaðarleiðréttingin vinnur aðeins virðisfærslur sem hafa ekki verið lagfærðar. Ef keyrslan þarf að flytja kostnaðarbreytingar á innleið í tengdar færslur á útleið gerir hún það með því að stofna nýjar virðisleiðréttingarfærslur sem byggja á upplýsingum um upphaflegar virðisfærslur en innihalda leiðréttingarupphæðina. Kostnaðarleiðréttingin notar dagsetningu bókunar upphaflegu virðisfærslunnar í leiðréttingarfærslunni nema hún sé í lokuðu birgðatímabili. Í því tilfelli notar kerfið upphafsdagsetningu næsta birgðatímabils. Ef birgðatímabil eru ekki notuð munu gögnin í reitnum **Bókun leyfð frá** í glugganum **Fjárhagsgrunnur** skilgreina hvenær leiðréttingarfærslan er bókuð.

Breytingar á birgðavirði frá viðskiptum eru sjálfkrafa afstemmdar við fjárhagsbækurnar þínar þegar þú bókar færslur. Frekari upplýsingar, sjá „Birgðasamræming“ hlutann í [Birgðir](inventory-manage-inventory.md) 

## <a name="to-adjust-item-costs-manually"></a>Til að uppfæra birgðakostnað verks handvirkt
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Leiðrétta kostnað - Birgðafærslur** og velja svo viðeigandi tengil.
2. Í glugganum **Leiðr. Kostnað - Birgðafærslur** skal tilgreina hvaða vörur á að leiðrétta kostnað fyrir.
3. Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

