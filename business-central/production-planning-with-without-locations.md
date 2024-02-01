---
title: Áætlanagerð með eða án birgðageymslna
description: 'Í þessu efnisatriði er kynning á framleiðslu, þ.m.t. áætlanagerð framboðs, í Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="planning-with-or-without-locations"></a>Áætlanagerð með eða án birgðageymslna

Áður en þú byrjar að nota áætlunarvélina mælum við með því að þú ákveðir hvort þú viljir nota staðsetningar eða ekki. Tvær meginleiðir eru til:

* eftirspurnarlínur eru alltaf með birgðageymslukóta og kerfið notar birgðahaldseiningar til fulls með viðeigandi birgðageymsluuppsetningu. Frekari upplýsingar eru á [Eftirspurn í birgðageymslu](#demand-at-location).  
* eftirspurnarlínur eru aldrei með birgðageymslukóða og kerfið notar birgðaspjaldið. Sjá aðstæðurnar [Eftirspurn í „tómri birgðageymslu“](#demand-at-blank-location) fyrir neðan.

## <a name="demand-at-location"></a>Eftirspurn í birgðageymslu

Þegar áætlunarkerfið greinir eftirspurn í birgðageymslu (línu með birgðageymslukóta) vinnar það á mismunandi hátt í samræmi við 2 mikilvæg uppsetningargildi.  

Í áætlunarkeyrslu leitar kerfið að 2 uppsetningargildum í röð og áætlar samkvæmt þeim:  

1. Er SKU til fyrir vöruna í umbeðinni birgðageymslu?  

    Ef já:  

    Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.  

    Ef nei:  

2. Inniheldur reiturinn **Íhlutir í birgðageymslu** á síðunni **Framleiðslugrunnur** staðsetningarkóðann sem óskað er eftir?  

    Ef já:  

    Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

    Ef nei:  

    Varan er áætluð í samræmi við „lágmarksvalkost“ sem nær yfir nákvæma eftirspurn. Áætlunarfæribreyturnar eru stilltar sem: Endurpöntunarstefna = *Lota fyrir lotu*, Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auðar. (Vörur sem nota endurpöntunarstefnuna *Pöntun* nota *Pöntun* áfram ásamt öðrum stillingum.)

> [!TIP]
> Ef þú áætlar oft eftirspurn á mismunandi birgðageymslum, þá er mælt með að þú notir möguleika birgðahaldseininga og forðist eftirspurn í tómum birgðageymslum. Frekari upplýsingar má finna á [Setja upp birgðahaldseiningar](inventory-how-to-set-up-stockkeeping-units.md)

Sjá frávik í [dæmunum hér fyrir neðan](#scenarios).

> [!NOTE]
> Reiturinn **Íhlutir í birgðageymslu** á síðunni **Framleiðsluuppsetning** er mikilvægur í að stjórna hvernig áætlanakerfið meðhöndlar eftirspurnarlínur framleiðslu.
>
> Fyrir framleiðslueftirspurn mun [!INCLUDE [prod_short](includes/prod_short.md)] nota sömu birgðageymslu fyrir undirsamsetningu og íhluti og sem gefin er upp í framleiðslupöntuninni. Með því að fylla út þennan reit er hins vegar hægt að framsenda undirsamsetninguna og íhlutina á aðra birgðageymslu.
>
> Einnig er hægt að skilgreina þetta fyrir tiltekna birgðahaldseiningu með því að velja annan staðsetningarkóða í reitnum **Íhlutir í birgðageymslu** á birgðahaldseiningaspjaldinu. Athugið samt sem áður að það er varhugavert þar sem áætlunnargrunnur kann að skekkjast þegar áætlun er gerð fyrir íhluti birgðahaldseininga.

## <a name="demand-at-blank-location"></a>Eftirspurn í "Tómri birgðageymslu"

Almennt, þegar áætlunarkerfið greinir eftirspurn í tómri birgðageymslu (línu án staðsetningarkóða), er varan áætluð samkvæmt áætlunarfæribreytum í birgðaspjaldinu.

Reiturinn **Birgðageymsla áskilin** á síðunni **Birgðauppsetning**, reiturinn **Íhlutir í birgðageymslu** á síðunni **Framleiðsluuppsetning** eða í birgðahaldseiningum munu hafa áhrif á hvernig áætlanakerfið meðhöndlar eftirspurnarlínur með/án staðsetningarkóða. Ef ein af eftirfarandi fullyrðingum er sönn er einnig litið á eftirspurn í tómri birgðageymslu sem frávik og áætlunarkerfið bregst við með því að leggja til „lágmarksvalkostinn“: Varan er áætluð samkvæmt: Endurpöntunarstefna = *Lota fyrir lotu* (*Pöntun* verður áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = auðar.

* Reiturinn **Íhlutir í birgðageymslu** á síðunni **Framleiðsluuppsetning** er með gildi.
* Birgðahaldseining er til fyrir áætlaða vöru.
* Reiturinn **Birgðageymsla áskilin** er valinn.

## <a name="scenarios"></a>Dæmi

Sjá frávik í uppsetningardæmunum hér fyrir neðan.

### <a name="setup-1"></a>Uppsetning 1

* Birgðageymsla áskilin = *Já*  
* BHE er sett upp fyrir *VESTUR*  
* Íhlutir í birgðageymslu = *AUSTUR*  

#### <a name="case-11-demand-is-at-west-location"></a>Mál 1.1: Eftirspurn er í birgðageymslu *VESTUR*

Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu (að hugsanlegri millifærslu meðtalinni).

#### <a name="case-12-demand-is-at-east-location"></a>Mál 1.2: Eftirspurn er í birgðageymslu *AUSTUR*

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.

#### <a name="case-13-demand-is-at-main-location"></a>Mál 1,3: eftirspurn er á  *aðalstað*

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lota-fyrir-lotu* (*Pöntun* er áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-14-demand-is-at-blank-location"></a>Dæmi 1.4: Eftirspurn er í birgðageymslunni *TÓMT*

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lota-fyrir-lotu* (*Pöntun* er áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = tómar.

### <a name="setup-2"></a>Uppsetning 2

* Birgðageymsla áskilin = *Já*  
* Engin birgðahaldseining er til  
* Íhlutir í birgðageymslu = *AUSTUR*  

#### <a name="case-21-demand-is-at-west-location"></a>Mál 2.1: Eftirspurn er í birgðageymslu *VESTUR*

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lota-fyrir-lotu* (*Pöntun* er áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-22-demand-is-at-east-location"></a>Mál 2.2: Eftirspurn er í birgðageymslu *AUSTUR*

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

### <a name="setup-3"></a>Uppsetning 3

* Birgðageymsla áskilin = *Nei*  
* Engin birgðahaldseining er til  
* Íhlutir í birgðageymslu = *AUSTUR*  

#### <a name="case-31-demand-is-at-west-location"></a>Mál 3.1: Eftirspurn er í birgðageymslu *VESTUR*

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lota-fyrir-lotu* (*Pöntun* er áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-32-demand-is-at-east-location"></a>Mál 3.2: Eftirspurn er í birgðageymslu *AUSTUR*

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

#### <a name="case-33-demand-is-at-blank-location"></a>Dæmi 3.3: Eftirspurn er í birgðageymslunni *TÓMT*

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lota-fyrir-lotu* (*Pöntun* er áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = tómar.

### <a name="setup-4"></a>Uppsetning 4

* Birgðageymsla áskilin = *Nei*  
* Engin birgðahaldseining er til  
* Íhlutir á staðnum = *TÓMT*  

#### <a name="case-41-demand-is-at-east-location"></a>Mál 4.1: Eftirspurn er í birgðageymslu *AUSTUR*

Vörunni er áætlað samkvæmt: Endurpöntunarstefna = *Lota-fyrir-lotu* (*Pöntun* er áfram *Pöntun*), Taka með birgðir = *Já*, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-42-demand-is-at-blank-location"></a>Dæmi 4.2: Eftirspurn er í birgðageymslunni *TÓMT*

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.

Eins og sjá má á síðasta dæmi er eina leiðin til að fá réttar niðurstöður fyrir eftirspurnarlínu án birgðageymslukóta sú að gera öll uppsetningargildi sem tengjast birgðageymslum óvirk. Sömuleiðis er eina leiðin til að fá stöðugar áætlunarniðurstöður fyrir eftirspurn í birgðageymslum sú að nota birgðahaldseiningar.  

Ef þú þar af leiðandi áætlar oft eftirspurn í birgðageymslum þá mælum við með að þú notir möguleika birgðahaldseiningar.

## <a name="see-also"></a>Sjá einnig .

[Áætlun](production-planning.md)  
[Setja upp framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Setja upp birgðahaldseiningar](inventory-how-to-set-up-stockkeeping-units.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
