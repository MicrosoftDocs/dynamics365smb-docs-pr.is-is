---
title: Búa til framleiðslupantanir úr sölupöntunum
description: Hægt er að búa til framleiðslupantanir úr sölupöntunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115237"
---
# <a name="create-production-orders-from-sales-orders"></a>Búa til framleiðslupantanir úr sölupöntunum
Hægt er að búa til framleiðslupantanir fyrir framleiðsluvörur beint frá sölupöntunum.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Framleiðslupantanir búnar til í sölupöntunum:  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Veldu sölupöntun sem þú vilt búa til framleiðslupöntun fyrir.  
3.  Veldu aðgerðina **Áætlun**. Á síðunni **Áætlun sölupöntunar** er hægt að skoða magn vörunnar í sölupöntuninni sem er til ráðstöfunar.  
4.  Veldu aðgerðina **Stofna framl.pöntun**.  
5.  Velja skal stöðu og pöntunartegund.  
6.  Veldu hnappinn **Já** til að búa til eina eða fleiri framleiðslupantanir fyrir línurnar sem eru með **Framl.pöntun** í reitnum **Áfyllingarkerfi**.


> [!NOTE]  
> Eftirspurnarlínur í tilbúinn framleiðslupöntun sem hafa **Framl.pöntun** í reitnum **Áfyllingarkerfi** tákna undirliggjandi framleiðslupantanir. Eftir að hafa myndað þessar framleiðslupantanir þarf að reikna aftur út áætlun á síðunni **Pantanaáætlun** eða **Enduráætla** til að auðkenna alla óuppfyllta eftirspurn eftir íhlutum fyrir þær. 

## <a name="order-type"></a>Gerð pöntunar  
Hægt er að velja um tvær leiðir til að búa til framleiðslupantanir eins og lýst er í eftirfarandi töflu.

|Valkostur|Description|
|------|-----------|
|Vörupöntun|Ein framleiðslupöntun er stofnuð fyrir hverja framleiðslupöntun sem þarf og sem er táknuð með línu í glugganum **Áætlun sölupöntunar**.|
|Verkefnispöntun|Ein framleiðslupöntun er stofnuð fyrir allar framleiðslupantanir sem þarf og sem eru táknaðar með línum í glugganum **Áætlun sölupöntunar**. |

Þegar verkpantanir eru notaðar inniheldur **Tegund uppruna** í framleiðslupöntuninni **Söluhaus** og hún hefur margar línur, eina fyrir hverja vöru sölulínu sem þarf að framleiða.  


## <a name="see-also"></a>Sjá einnig  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
