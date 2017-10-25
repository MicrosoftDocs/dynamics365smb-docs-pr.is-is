---
title: "Áætlanagerð með eða án birgðageymslna | Microsoft Docs"
description: "Mikilvægt er að skilja áætlanir með eða án birgðageymslukóta í eftirspurnarlínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 964bcd38897e676baa993399fe772b8ccfdc9ea0
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="planning-with-or-without-locations"></a>Áætlanagerð með eða án birgðageymslna
Varðandi áætlanir með eða án birgðageymslukóta í eftirspurnarlínum vinnur áætlanakerfið á einfaldan hátt þegar:  

-   eftirspurnarlínur eru alltaf með birgðageymslukóta og kerfið notar birgðahaldseiningar til fulls með viðeigandi birgðageymsluuppsetningu.  
-   eftirspurnarlínur eru aldrei með birgðageymslukóta og kerfið notar ekki birgðahaldseiningar eða neina birgðageymsluuppsetningu (sjá síðasta dæmið hér fyrir neðan).  

Ef hins vegar eftirspurnarlínur eru stundum með birgðageymslukóta og stundum ekki fer áætlanakerfið eftir tilteknum reglum í samræmi við uppsetningu.  

## <a name="demand-at-location"></a>Eftirspurn í birgðageymslu  
Þegar áætlunarkerfið greinir eftirspurn í birgðageymslu (línu með birgðageymslukóta) vinnar það á mismunandi hátt í samræmi við 3 mikilvæg uppsetningargildi.  

Í áætlunarkeyrslu leitar kerfið að 3 uppsetningargildum í röð og áætlar samkvæmt þeim:  

1.  Er gátmerki í reitnum **Birgðageymsla áskilin**?  

    Ef já:  

2.  Er birgðahaldseining til fyrir vöruna?  

    Ef já:  

    Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.  

    Ef nei:  

3.  Er reiturinn **Íhlutir á staðnum** með áskildum birgðageymslukóta?  

    Ef já:  

    Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.  

    Ef nei:  

    Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* , Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar. (Vörur sem nota endurpöntunarstefnuna  *Pöntun* nota  *Pöntun* ásamt öðrum stillingum).  

> [!NOTE]  
>  Þessi lágmarksvalkostur nær aðeins yfir nákvæma eftirspurn. Allar skilgreindar áætlunarfæribreytur eru hunsaðar.  

Sjá frávik í dæmunum hér fyrir neðan.  

## <a name="demand-at-blank-location"></a>Eftirspurn í "Tómri birgðageymslu"  
Jafnvel þó merkt sé við reitinn **Birgðageymsla áskilin** er heimilt að stofna línur í kerfinu án birgðageymslukóta – einnig kallað *TÓM* birgðageymsla. Þetta er frávik í kerfinu því það er með mismunandi uppsetningargildi sem stillt eru á að vinna með birgðageymslur (sjá ofangreint) og niðurstaðan verður sú að áætlunarkerfið stofnar ekki áætlunarlínu fyrir svona eftirspurnarlínu. Ef ekki er merkt við reitinn **Birgðageymsla áskilin** en einhver af uppsetningargildum birgðageymsla eru til er það einnig talið vera frávik og eftirspurnarkerfið bregst við með því að leggja til „lágmarksvalkostinn“:   
Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram *Pöntun)*, Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = Auðar.  

Sjá frávik í uppsetningardæmunum hér fyrir neðan.  

### <a name="setup-1"></a>Uppsetning 1:  

-   Birgðageymsla áskilin = *Já*  
-   Birgðahaldseining er sett upp fyrir  *RAUTT*  
-   Íhlutir á staðnum =  *BLÁTT*  

#### <a name="case-11-demand-is-at--red-location"></a>Dæmi 1.1: Eftirspurn er í birgðageymslunni  *RAUTT*  

Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu (að hugsanlegri millifærslu meðtalinni).  

#### <a name="case-12-demand-is-at--blue-location"></a>Dæmi 1.2: Eftirspurn er í birgðageymslunni  *RAUTT*  

Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.  

#### <a name="case-13-demand-is-at--green-location"></a>Dæmi 1.3: Eftirspurn er í birgðageymslunni  *GRÆNT*  

Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.  

#### <a name="case-14-demand-is-at--blank-location"></a>Dæmi 1.4: Eftirspurn er í birgðageymslunni  *TÓMT*  

Vörunni er ekki áætlað þar sem engin birgðageymsla er skilgreind í eftirspurnarlínunni.  

### <a name="setup-2"></a>Uppsetning 2:  

-   Birgðageymsla áskilin = *Já*  
-   Engin birgðahaldseining er til  
-   Íhlutir á staðnum =  *BLÁTT*  

#### <a name="case-21-demand-is-at--red-location"></a>Dæmi 2.1: Eftirspurn er í birgðageymslunni  *RAUTT*  

Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.  

#### <a name="case-22-demand-is-at--blue-location"></a>Dæmi 2.2: Eftirspurn er í birgðageymslunni  *RAUTT*  

Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.  

### <a name="setup-3"></a>Uppsetning 3:  

-   Birgðageymsla áskilin = *Nei*  
-   Engin birgðahaldseining er til  
-   Íhlutir á staðnum =  *BLÁTT*  

#### <a name="case-31-demand-is-at--red-location"></a>Dæmi 3.1: Eftirspurn er í birgðageymslunni  *RAUTT*  

Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.  

#### <a name="case-32-demand-is-at--blue-location"></a>Dæmi 3.2: Eftirspurn er í birgðageymslunni  *RAUTT*  

Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.  

#### <a name="case-33-demand-is-at--blank-location"></a>Dæmi 3.3: Eftirspurn er í birgðageymslunni  *TÓMT*  

Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.  

### <a name="setup-4"></a>Uppsetning 4:  

-   Birgðageymsla áskilin = *Nei*  
-   Engin birgðahaldseining er til  
-   Íhlutir á staðnum =  *TÓMT*  

#### <a name="case-41-demand-is-at--blue-location"></a>Dæmi 4.1: Eftirspurn er í birgðageymslunni  *BLÁTT*  

Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.  

#### <a name="case-42-demand-is-at--blank-location"></a>Dæmi 4.2: Eftirspurn er í birgðageymslunni  *TÓMT*  

Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.  

Eins og sjá má á síðasta dæmi er eina leiðin til að fá réttar niðurstöður fyrir eftirspurnarlínu án birgðageymslukóta sú að gera öll uppsetningargildi sem tengjast birgðageymslum óvirk. Sömuleiðis er eina leiðin til að fá stöðugar áætlunarniðurstöður fyrir eftirspurn í birgðageymslum sú að nota birgðahaldseiningar.  

Ef þörf í birgðageymslum er áætluð oft er eindregið mælt með að nota birgðahaldseiningaaðgerðina.  

## <a name="see-also"></a>Sjá einnig
[Áætlun](production-planning.md)    
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

