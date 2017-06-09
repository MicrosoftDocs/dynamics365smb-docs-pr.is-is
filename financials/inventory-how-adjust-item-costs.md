---
title: "Hvernig á að: Leiðrétta birgðakostnað handvirkt | Microsoft Docs"
description: "Hvernig á að: Leiðrétta birgðakostnað"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Hvernig á að: Leiðrétta birgðakostnað handvirkt
Kostnaðarverð vöru (birgðavirði) sem er keypt og seld síðar getur breyst á líftímanum, til dæmis vegna þess að kostnað við frakt er bætt við innkaupakostnaðinn þegar varan hefur verið seld. Kostnaðaraðlögun er sérstaklega viðeigandi í aðstæðum þar sem þú selur vörur áður en þú reiknar kaupin á þeim vörum. Til þess að vita alltaf rétt birgðavirði verður því að leiðrétta kostnaðarverð vöru reglubundið. Þetta tryggir að sölu- og hagnaðartölur séu réttar og afkastavísar (KPI) fjárhags séu réttir.

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] eru kostnaðarkostnaður sjálfkrafa leiðrétt í hvert skipti sem viðskiptin eiga sér stað, svo sem þegar þú sendir inn innkaupareikning fyrir hlut.

Þú getur einnig notað aðgerð til að breyta kostnaði við einn eða fleiri hluti handvirkt. Þetta er gagnlegt, til dæmis þegar þú veist að kostnaður hlutar hefur breyst af öðrum ástæðum en vörufærslu.

**Til athugunar**: Vörukostnaður er aðeins leiðréttur með FIFO-aðferðinni. Þetta þýðir að kostnaðarverð vöru er raunvirði sérhverrar innhreyfingar vörunnar og við verðmat birgða er gert ráð fyrir því að fyrstu vörurnar í birgðunum séu seldar fyrst.

Kostnaðarleiðréttingin vinnur aðeins virðisfærslur sem hafa ekki verið lagfærðar. Ef keyrslan þarf að flytja kostnaðarbreytingar á innleið í tengdar færslur á útleið gerir hún það með því að stofna nýjar virðisleiðréttingarfærslur sem byggja á upplýsingum um upphaflegar virðisfærslur en innihalda leiðréttingarupphæðina. Kostnaðarleiðréttingin notar dagsetningu bókunar upphaflegu virðisfærslunnar í leiðréttingarfærslunni nema hún sé í lokuðu birgðatímabili. Í því tilfelli notar kerfið upphafsdagsetningu næsta birgðatímabils. Ef birgðatímabil eru ekki notuð munu gögnin í reitnum **Bókun leyfð frá** í glugganum **Fjárhagsgrunnur** skilgreina hvenær leiðréttingarfærslan er bókuð.

Breytingar á birgðavirði frá viðskiptum eru sjálfkrafa afstemmdar við fjárhagsbækurnar þínar þegar þú bókar færslur. Nánari upplýsingar er að finna í [Ítarlegt: Afstemming birgða](advanced-inventory-reconciliation.md).

## <a name="to-adjust-item-costs-manually"></a>Til að uppfæra birgðakostnað verks handvirkt
1. Efst í hægra horninu skal velja táknið fyrir **Leit að síðu eða skýrslu** táknið fyrir ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "táknið fyrir Leit að síðu eða skýrslu"), slá inn **Leiðr. kostnað - Birgðafærslur** og velja síðan viðeigandi tengil.
2. Í glugganum **Leiðr. Kostnað - Birgðafærslur** skal tilgreina hvaða vörur á að leiðrétta kostnað fyrir.
3. Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Ítarlegt: Afstemming birgða](advanced-inventory-reconciliation.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

