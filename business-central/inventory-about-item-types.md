---
title: Hvernig vörutegundir virka
description: Þú getur leiðrétt birgðaverðmat vöru með því að nota FIFO eða Meðalkostnaðaraðferð þegar vöruverð breytist ekki vegna viðskiptalegra ástæðna, heldur einhvers annars.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 9297, 5845, 30,
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: e902068398a636b5e205fa7d808066861059b901
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131692"
---
# <a name="about-item-types"></a>Um vörutegundir
Í reitnum **Tegund** á **síðunni Birgðaspjald** er hægt að velja til hvers varan er notuð í fyrirtækinu, sem hefur áhrif á að hve miklu leyti hægt er að stjórna vörunni í birgðum. Eftirfarandi tafla sýnir og lýsir þremur gerðum vara sem eru tiltækar.

|Valkostur|Dæmigerður tilgangur|
|------|-----------|
|Birgðir|Efnislegir hlutir, svo sem reiðhjól, símar og skrifborð, sem þú vilt geta notað öll birgðaferli fyrir. Þetta getur einnig innihaldið vörur sem ekki eru efnislegar, svo sem hugbúnaðarleyfi og áskriftir, ef vörurnar eru með kennitölur, svo sem raðnúmer. Hægt er að rekja að fullu vöruvirði og ráðstöfunarmagn í birgðum.|
|Engar birgðir|Venjulega eru vörur sem ekki eru birgðum efnislegir hlutir, svo sem boltar eða pennar, sem fyrirtæki notar en vill ekki rekja að fullu í birgðum. Til dæmis vegna þess að þær eru lággjaldavörur og eru aðeins notaðar við innri vinnslu.|
|Þjónusta|Vinnutímaeining, svo sem ráðgjöf í klukkustund, fyrir takmarkaðan stuðning fyrirtækis.|

> [!NOTE]
> Gerðirnar **Þjónusta** og **ekki birgðir** styðja ekki rakningu á birgðamagni og gildum. Aðeins valdar vörufærslugerðir og aðgerðir eru studdar.

Í eftirfarandi töflu er listi yfir aðgerðir sem vörugerðirnar þrjár styðja.

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