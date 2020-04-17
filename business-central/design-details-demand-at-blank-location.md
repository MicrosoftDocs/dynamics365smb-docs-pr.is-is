---
title: Hönnunarupplýsingar - Eftirspurn og framboð | Microsoft Docs
description: Í þessu efnisatriði er fjallað um hugtakið Eftirspurn, sem er algengasta orðið notað yfir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f808865bd4fc2113dd5c04071f7ba2e8793fe3af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185565"
---
# <a name="design-details-demand-at-blank-location"></a>Hönnunarupplýsingar: Eftirspurn í birgðageymslunni Tómt
Þegar notandi býr til eftirspurnartilvik, svo sem sölupöntunarlínu gerir kerfið notandanum kleift að stundum tilgreina staðsetningarkóða og stundum ekki, það er, að nota auða staðsetningu.

Varðandi áætlanir með eða án birgðageymslukóða vinnur áætlanakerfið á einfaldan hátt þegar:

- Eftirspurnarlínur eru alltaf með staðsetningarkóða og kerfið notar birgðahaldseiningar til fulls með viðeigandi staðsetningaruppsetningu.
- Eftirspurnarlínur eru aldrei með birgðageymslukóða og kerfið notar ekki birgðahaldseiningar eða neina birgðageymsluuppsetningu (sjá síðasta dæmið hér fyrir neðan).

Ef hins vegar eftirspurnaratvik eru stundum með birgðageymslukóða og stundum ekki fer áætlanakerfið eftir tilteknum reglum í samræmi við uppsetningu.

## <a name="demand-at-location"></a>Eftirspurn í birgðageymslu
Þegar áætlunarkerfið greinir eftirspurn á staðsetningu vinnur það á mismunandi hátt í samræmi við þrjú mikilvæg uppsetningargildi. Í áætlunarkeyrslu leitar kerfið að 3 uppsetningargildum í röð og áætlar samkvæmt þeim:

1. Er gátmerki í reitnum **Birgðageymsla áskilin**?

    Ef já:

2. Er birgðahaldseining til fyrir vöruna?

    Ef já:

    Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.

    Ef nei:

3. Er reiturinn Íhlutir á staðnum með áskildum birgðageymslukóta?

  Ef já:

  Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.

  Ef nei:

  Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu , Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar. Vörur sem nota endurpöntunarstefnuna Pöntun nota Pöntun ásamt öðrum stillingum.

> [!NOTE]
> Einstök áætlunaruppsetning sem er framleiðsla sem síðasta svörun í skrefi 3 hér að ofan er vitnað til í eftirfarandi sem „lágmarksvalkostur“. Þessi áætlunaruppsetning nær aðeins yfir nákvæma eftirspurn. Allar skilgreindar áætlunarfæribreytur eru hunsaðar.

Upplýsingar um afbrigði af þessum áætlunarrökum eru í hlutanum Dæmi fyrir neðan.

## <a name="demand-at-blank-location"></a>Eftirspurn í tómir stöðu
Jafnvel þó merkt sé við reitinn **Birgðageymsla áskilin** er heimilt að stofna línur í kerfinu án birgðageymslukóða – einnig kallað tóm birgðageymsla. Þetta er frávik í kerfinu því það er með mismunandi uppsetningargildi sem stillt eru á að vinna með birgðageymslur (sjá ofangreint) og niðurstaðan verður sú að áætlunarkerfið stofnar ekki áætlunarlínu fyrir svona eftirspurnarlínu.

Ef reiturinn **Birgðargeymsla áskilin** áskilin er ekki valinn en einhver af uppsetningargildum birgðageymsla eru til er það einnig talið vera frávik og eftirspurnarkerfið bregst við með því að nota „lágmarksvalkost“: Varan er áætluð samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = Auðar.

## <a name="scenarios"></a>Dæmi
Eftirfarandi atburðarás lýsir afbrigðum eftirspurnar á auðum stað og hvernig áætlanakerfi leysir „lágmarksvalkost“.

### <a name="setup-1"></a>Uppsetning 1:
Birgðageymsla áskilin = Já

Birgðahaldseining er sett upp fyrir RAUTT

Íhlutir á staðnum = BLÁTT

#### <a name="case-11-demand-is-at-red-location"></a>Dæmi 1.1: Eftirspurn er í birgðageymslunni  RAUTT
Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.

#### <a name="case-12-demand-is-at-blue-location"></a>Dæmi 1.2: Eftirspurn er í birgðageymslunni  BLÁTT
Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-13-demand-is-at-green-location"></a>Dæmi 1.3: Eftirspurn er í birgðageymslunni GRÆNT
Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-14-demand-is-at-blank-location"></a>Dæmi 1.4: Eftirspurn er í birgðageymslunni TÓMT
Vörunni er ekki áætlað þar sem engin birgðageymsla er skilgreind í eftirspurnarlínunni.

### <a name="setup-2"></a>Uppsetning 2:
Birgðageymsla áskilin = Já

Engin birgðahaldseining er til

Íhlutir á staðnum = BLÁTT

#### <a name="case-21-demand-is-at-red-location"></a>Dæmi 2.1: Eftirspurn er í birgðageymslunni  RAUTT
Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-22-demand-is-at-blue-location"></a>Dæmi 2.2: Eftirspurn er í birgðageymslunni  BLÁTT
Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.

### <a name="setup-3"></a>Uppsetning 3:
Birgðageymsla áskilin = Nei

Engin birgðahaldseining er til

Íhlutir á staðnum = BLÁTT

#### <a name="case-31-demand-is-at-red-location"></a>Dæmi 3.1: Eftirspurn er í birgðageymslunni RAUTT
Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-32-demand-is-at-blue-location"></a>Dæmi 3.2: Eftirspurn er í birgðageymslunni  BLÁTT
Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.

#### <a name="case-33-demand-is-at-blank-location"></a>Dæmi 3.3: Eftirspurn er í birgðageymslunni TÓMT
Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.

### <a name="setup-4"></a>Uppsetning 4:
Birgðageymsla áskilin = Nei

Engin birgðahaldseining er til

Íhlutir á staðnum = TÓMT

#### <a name="case-41-demand-is-at-blue-location"></a>Dæmi 4.1: Eftirspurn er í birgðageymslunni BLÁTT
Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.

#### <a name="case-42-demand-is-at-blank-location"></a>Dæmi 4.2: Eftirspurn er í birgðageymslunni TÓMT
Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.

Eins og sjá má á síðasta dæmi er eina leiðin til að fá réttar niðurstöður fyrir eftirspurnarlínu án birgðageymslukóða sú að gera öll uppsetningargildi sem tengjast birgðageymslum óvirk. Sömuleiðis er eina leiðin til að fá stöðugar áætlunarniðurstöður fyrir eftirspurn í birgðageymslum sú að nota birgðahaldseiningar. Af þeim sökum er fyrirtækjum sem þurfa oft að áætla fyrir eftirspurn í birgðageymslum ráðlagt að nota eindina Birgðahaldseiningar.

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
