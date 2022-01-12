---
title: Hvernig vörutegundir virka
description: Þú getur leiðrétt birgðaverðmat vöru með því að nota FIFO eða Meðalkostnaðaraðferð þegar vöruverð breytist ekki vegna viðskiptalegra ástæðna, heldur einhvers annars.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 0fc31469d13c0c84a7357ae99929d6efb30bbb47
ms.sourcegitcommit: 13b811918b3c9f1598150b5cbbf387974b2a6df6
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/04/2022
ms.locfileid: "7949044"
---
# <a name="about-item-types"></a>Um vörutegundir
Í **reitnum Tegund** á **vöruspjaldinu er** hægt að velja hvað varan er notuð í viðskiptunum, sem hefur áhrif á það hversu hægt er að stjórna vörunni í birgðum. Eftirfarandi töflulistum og lýsir þeim þremur tegundum atriða sem eru tiltæk.

|Valkostur|Dæmigerður tilgangur|
|------|-----------|
|Birgðir|Eðlislegir hlutir, svo sem reiðhjól, síma-og deskunarskápar, sem óskað er eftir að geti notað alla birgðaferla. Þetta geta einnig verið Óefnislegir hlutir eins og hugbúnaðarleyfi og áskriftir, ef vörurnar eru með kennitölum, eins og raðnúmerum. Hægt er að rekja gildi vöru og ráðstöfunarmagn í birgðum.|
|Engar birgðir|Yfirleitt eru það ekki birgðavörur, til dæmis boltar eða pennar, sem fyrirtæki eyðir en vill ekki fullkomlega rekja birgðir. Til dæmis vegna þess að þeir eru lágkostnaðarliðir og eru aðeins notaðir innbyrðis.|
|Þjónusta|Vinnutímaeining, svo sem ráðgjöf í klukkustund, fyrir takmarkaðan stuðning fyrirtækis.|

> [!NOTE]
> **Þjónustan** og ekki **birgðagerðir** styðja ekki mælingar á magni birgða og virði. Aðeins valdar vörufærslugerðir og eiginleikar eru studdir.

Í eftirfarandi töflu er listi yfir aðgerðirnar sem þrjár vörutegundir styðja.

|Gerð vöru|Sölur|Innkaup|Vinnunotkun|Þjónustunotkun|Samsetningarnotkun|Framleiðsla Notkun|Samsetningarfrálag|Framleiðslufrálag|Staðsetningarflutningur|Birgðatalning|Endurmat á birgðum|Birgðakostnaður|Vörurakning|Frátekning|Vörugeymsla|Áætlun|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Birgðir|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|
|Engar birgðir|Já|Já|Já|Já|Já|Já|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|
|Þjónusta|Já|Já|Já|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|

## <a name="costing-methods-for-types-of-items"></a>Kostnaðaraðferðir fyrir vörutegundir
Þegar birgðafærslur eru bókaðar eru magnið og gildisbreytingarnar í birgðunum skráð í birgðafærslunum og virðisfærslurnar, hvort í sínu lagi. 

Fyrir birgðavörur er kostnaðurinn skráður í reitinn **Kostnaðarupphæð (raunveruleg)** á **Virðisfærslur**, og við afstemmingu við fjárhag er kostnaðurinn sýndur í reitnum **Kostnaður bókaður í fjárhag**. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðakostnaður](design-details-inventory-costing.md)

Fyrir vörur sem eru ekki birgðir og þjónusta er kostnaðurinn skráður í **Kostnaðarupphæð (óbirgðafæranl.)** svæði á síðunni **Virðisfærslur**. Fyrir vörur sem eru ekki birgðir og þjónusta er kostnaðurinn tilgreindur í sölu, samsetningu og framleiðsluskjölum og færslubókum. Hægt er að tilgreina sjálfgefinn kostnað í reitnum **Einingarkostnaður** á síðunum **Birgðaspjald** og **Birgðahaldseining**. Kostnaður fyrir þessar vörutegundir er ekki stemmdur við fjárhag. 

## <a name="catalog-and-service-items"></a>Vörulistar og þjónustuvörur
Vörur sem þú býður viðskiptamönnum þínum en þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær er hægt að setja upp sem vörulistaatriði. Vörulistaatriðum skal ekki rugla saman við venjulegar vörur af gerðinni „Engar birgðir“. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

Hlutir viðskiptamanna sem þú framkvæmir þjónustu á, svo sem prentarar, kallast þjónustuvörur. Þjónustuvörur hafa ekkert að gera með venjulegar vörur eða vörulistaatriði. Hins vegar geta íhlutir þjónustuvara verið venjulegar vörur. Nánari upplýsingar er að finna í [Setja upp þjónustuvörur og íhluti þjónustuvara](service-how-setup-service-items.md).

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Uppsetning birgða](inventory-setup-inventory.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]