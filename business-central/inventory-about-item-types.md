---
title: Skilningur á vörutegundum | Microsoft Docs
description: Þú getur leiðrétt birgðaverðmat vöru með því að nota FIFO eða Meðalkostnaðaraðferð, til dæmis þegar vöruverð breytist ekki vegna viðskiptalegra ástæðna, heldur einhvers annars.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab3da8450586928a02d17ccce14c704ed6d7c8fe
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182397"
---
# <a name="about-item-types"></a>Um vörutegundir
Í reitnum **Tegund** á síðunni **Birgðaspjald** er hægt að velja fyrir hvað varan er notuð í fyrirtækinu og því hvernig henni er stjórnað í kerfinu. Þrír valkostir eru til:

|Valkostur|Dæmigerður tilgangur|
|------|-----------|
|Birgðir|Efnisleg eining, svo sem reiðhjól, fyrir fullan stuðning fyrirtækisins.|
|Engar birgðir|Efnisleg eining, eins og bolti, fyrir takmarkaðan stuðning fyrirtækja, til dæmis vegna þess að hluturinn er aðeins notaður innbyrðis og er með litlum tilkostnaði.|
|Þjónusta|Vinnutímaeining, svo sem ráðgjöf í klukkustund, fyrir takmarkaðan stuðning fyrirtækis.|

Gerðin **Birgðir** felur í sér fulla mælingu á birgðamagni og gildi. Þess vegna eru allar færslugerðir vöru studdar og hlutir af tegundinni Birgðir geta verið notaðir með öllum eiginleikum meðhöndlunar vöru.

Gerðirnar **Þjónusta** og **Engar birgðir** fela ekki í sér mælingar á birgðamagni og gildi. Þess vegna eru aðeins valdar færslugerðir og eiginleikar studd.

Vörutegundirnar þrjár styðja eftirfarandi eiginleika eftir því sem við á.

|Gerð vöru|Sölur|Innkaup|Vinnunotkun|Þjónustunotkun|Samsetningarnotkun|Framleiðsla Notkun|Samsetningarfrálag|Framleiðslufrálag|Staðsetningarflutningur|Birgðatalning|Endurmat á birgðum|Birgðakostnaður|Vörurakning|Frátekning|Vörugeymsla|Áætlun|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Birgðir|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|
|Engar birgðir|Já|Já|Já|Já|Já|Já|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|
|Þjónusta|Já|Já|Já|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|

> [!NOTE]
> Vörur sem þú býður viðskiptamönnum þínum en þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær er hægt að setja upp sem vörulistaatriði. Vörulistaatriðum skal ekki rugla saman við venjulegar vörur af gerðinni „Engar birgðir“. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Hlutir viðskiptamanna sem þú framkvæmir þjónustu á, svo sem prentarar, kallast þjónustuvörur. Þjónustuvörur hafa ekkert að gera með venjulegar vörur eða vörulistaatriði. Hins vegar geta íhlutir þjónustuvara verið venjulegar vörur. Nánari upplýsingar er að finna í [Setja upp þjónustuvörur og íhluti þjónustuvara](service-how-setup-service-items.md).

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Uppsetning birgða](inventory-setup-inventory.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
