---
title: Áætlanagerð með eða án birgðageymslna
description: Í þessu efnisatriði er kynning á framleiðslu, þ.m.t. áætlanagerð framboðs, í Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/15/2022
ms.author: edupont
ms.openlocfilehash: 4bb3f626e02259171a9a1bf41c580f34aaa19758
ms.sourcegitcommit: 2396dd27e7886918d59c5e8e13b8f7a39a97075d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524538"
---
# <a name="planning-with-or-without-locations"></a>Áætlanagerð með eða án birgðageymslna

Áður en hafist er handa við að nýta áætlunarvél er mælt með því að ákveða hvort nota eigi staðsetningar. Hér eru tvær helstu lagaleiðir:

* eftirspurnarlínur eru alltaf með birgðageymslukóta og kerfið notar birgðahaldseiningar til fulls með viðeigandi birgðageymsluuppsetningu. Frekari upplýsingar í [eftirspurn á staðnum](#demand-at-location).  
* Eftirspurnarlínur bera aldrei birgðageymslukóta og kerfið notar birgðaspjaldið. [Sjá eftirspurnina í "auða birgðageymslu"](#demand-at-blank-location) atburðarásina hér að neðan.

## <a name="demand-at-location"></a>Eftirspurn á staðnum  

Þegar áætlunarkerfið greinir eftirspurn í birgðageymslu (línu með birgðageymslukóta) vinnar það á mismunandi hátt í samræmi við 2 mikilvæg uppsetningargildi.  

Í áætlunarkeyrslu leitar kerfið að 2 uppsetningargildum í röð og áætlar samkvæmt þeim:  

1. Er BIRGÐAHALDSEINING til fyrir vöruna á kröfuharða staðnum?  

    Ef já:  

    Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.  

    Ef nei:  

2. Inniheldur reiturinn **Íhlutir í birgðageymslu** á síðunni **Framleiðslugrunnur** staðsetningarkóðann sem óskað er eftir?  

    Ef já:  

    Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

    Ef nei:  

    Varan er áætluð í samræmi við "lágmarks val" sem nær til nákvæmrar eftirspurnar. Áætlunarfæribreytur eru stilltar sem: Endurpöntunarstefna = *Lotu-fyrir-lotu*, taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auðar. (Vörur sem nota endurpöntunarstefnu *Panta* áfram með *pöntun* sem og aðrar stillingar.)

> [!TIP]
> Ef þú ætlar oft að áætla þörf á mismunandi stöðum, þá mælum við með því að þú notir getu birgðahalds og forðast eftirspurn á auðum stað. Frekari upplýsingar um það að [setja birgðahaldseiningar upp](inventory-how-to-set-up-stockkeeping-units.md)

Sjá frávik í atburðarásinni hér á [eftir](#scenarios).

> [!NOTE]
> **Reiturinn** Íhlutir á staðnum **á síðunni Uppsetning** framleiðslu er mjög mikilvægur í því að stjórnast af því hvernig áætlunarkerfið sér um eftirspurnarlínur framleiðslu.
>
> Fyrir framleiðslueftirspurn [!INCLUDE [prod_short](includes/prod_short.md)] mun nota sama stað fyrir undirsamsetningar og íhluti sem og fram kemur í framleiðslupöntuninni. Hins vegar er hægt að beina undirsetningunni og íhlutum í aðra birgðageymslu með því að fylla í þennan reit.
>
> Einnig er hægt að skilgreina þetta fyrir tiltekna birgðahaldseiningu með því að velja annan staðsetningarkóða í reitnum **Íhlutir í birgðageymslu** á birgðahaldseiningaspjaldinu. Athugið samt sem áður að það er varhugavert þar sem áætlunnargrunnur kann að skekkjast þegar áætlun er gerð fyrir íhluti birgðahaldseininga.

## <a name="demand-at-blank-location"></a>Eftirspurn á "auðum stað"

Almennt þegar áætlanakerfið finnur eftirspurn í auðri birgðageymslu (línu án birgðageymslukóta) er varan áætluð samkvæmt áætlunarfæribreytum á birgðaspjaldinu.

**Reiturinn birgðageymslur áskilin** á **síðunni Birgðagrunnur**, **reiturinn Íhlutir á staðnum** á **framleiðslustað**, eða birgðahaldseiningar hafa áhrif á hvernig áætlanakerfið meðhöndlar eftirspurnarlínur með/án birgðageymslukóta. Ef ein af eftirtöldum staðhæfingum er sönn er einnig stuðst við frávikstilboð og áætlanakerfið bregst við með því að leggja fram "lágmarks val": varan er áætluð samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auðar.

* **Reiturinn** Íhlutir á staðnum **á síðunni Uppsetning** framleiðslu hefur gildi.
* Birgðaeining er til fyrir áætluðu vöruna.
* **Reiturinn Birgðageymsla áskilin** er valinn.

## <a name="scenarios"></a>Dæmi

Sjá frávik í uppsetningardæmunum hér fyrir neðan.

### <a name="setup-1"></a>Skipulag 1

* Birgðageymsla áskilin = *Já*  
* Be er sett upp fyrir *vesti*  
* Íhluturinn á staðnum = *Austur*  

#### <a name="case-11-demand-is-at-west-location"></a>Mál 1,1: krafa er á *West* Location

Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu (að hugsanlegri millifærslu meðtalinni).

#### <a name="case-12-demand-is-at-east-location"></a>Mál 1,2: eftirspurn er á *Austurlandi* Staðsetning

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.

#### <a name="case-13-demand-is-at-north-location"></a>Mál 1,3: krafa er á *Norður* -stað

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auð.

#### <a name="case-14-demand-is-at-blank-location"></a>Mál 1,4: krafa er í *auða* birgðageymslu

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auð.

### <a name="setup-2"></a>Skipulag 2

* Birgðageymsla áskilin = *Já*  
* Engin birgðahaldseining er til  
* Íhluturinn á staðnum = *Austur*  

#### <a name="case-21-demand-is-at-west-location"></a>Mál 2,1: krafa er á *West* Location

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auð.

#### <a name="case-22-demand-is-at-east-location"></a>Mál 2,2: eftirspurn er á *Austurlandi* Staðsetning

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

### <a name="setup-3"></a>Skipulag 3

* Birgðageymsla áskilin = *Nei*  
* Engin birgðahaldseining er til  
* Íhluturinn á staðnum = *Austur*  

#### <a name="case-31-demand-is-at-west-location"></a>Mál 3,1: krafa er á *West* Location

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auð.

#### <a name="case-32-demand-is-at-east-location"></a>Mál 3,2: eftirspurn er á *Austurlandi* Staðsetning

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

#### <a name="case-33-demand-is-at-blank-location"></a>Mál 3,3: krafa er í *auða* birgðageymslu

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auð.

### <a name="setup-4"></a>Skipulag 4

* Birgðageymsla áskilin = *Nei*  
* Engin birgðahaldseining er til  
* Íhlutur á staðnum = *auður*  

#### <a name="case-41-demand-is-at-east-location"></a>Mál 4,1: eftirspurn er á *Austurlandi* Staðsetning

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lotu-fyrir-lotu* (*pöntun* leifar *pöntunar*), taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auð.

#### <a name="case-42-demand-is-at-blank-location"></a>Mál 4,2: krafa er í *auða* birgðageymslu

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.

Eins og sjá má á síðasta dæmi er eina leiðin til að fá réttar niðurstöður fyrir eftirspurnarlínu án birgðageymslukóta sú að gera öll uppsetningargildi sem tengjast birgðageymslum óvirk. Sömuleiðis er eina leiðin til að fá stöðugar áætlunarniðurstöður fyrir eftirspurn í birgðageymslum sú að nota birgðahaldseiningar.  

Ef þú þar af leiðandi áætlar oft eftirspurn í birgðageymslum þá mælum við með að þú notir möguleika birgðahaldseiningar.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Áætlun](production-planning.md)  
[Setja upp framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Setja upp birgðahaldseiningar](inventory-how-to-set-up-stockkeeping-units.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
