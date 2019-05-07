---
title: Uppsetning fjárhagseigna| Microsoft Docs
description: Áður en þú getur byrjað að stjórna eignum, verður þú að setja upp sjálfgefna fjárhagsreikninga, bókunarflokka, úthlutunarlykla, færslubókasniðmát og keyrslur, og flokkskóða.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 240e3e8dc151c971dcf5875bb3e7e8bb3d5edd45
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "941727"
---
# <a name="set-up-general-fixed-assets-information"></a>Uppsetning almennra eignaupplýsinga
Áður en hægt er að vinna með eignir, þarf að setja upp sjálfgefna fjárhagsreikninga, úthlutunarlykla, færslubókarsniðmát og keyrslur fyrir bókun á eign og endurflokkun og hægt er að flokka eignir í eignaflokka, til dæmis Áþreifanlegar og Óáþreifanlegar.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Uppsetning almennra sjálfgilda fyrir eignir
Skilgreina almenna virkni eða aðgerðina eign og setja upp númeraröð skjala á **Uppsetning Eigna** síðunni.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning eigna** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Setja upp bókunarflokka eigna
Bókunarflokkar eru notaðir til að skilgreina flokka eigna. Færslur í þessum bókunarflokkum eru bókaðar á sömu fjárhagsreikninga.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignabókunarflokkar** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.
3. Á síðunni **eignabókunarflokkaspjald** þarf að fylla reitina út eftir þörfum.

    > [!NOTE]  
    >   Til að ganga úr skugga um að mótreikningar fyrir mismunandi eignabókanir eru sjálfkrafa settir inn þegar þú velur **Setja inn mótreikning eigna** aðgerð í færslubókarlínum, fylgja skal næsta skref, í samræmi við uppfærslubókun.
4. Á flýtiflipi **Mótreikningur** í reitnum **mótreikningur uppfærslu** er valinn fjárhagsreikningurinn sem þú vilt bóka mótfærslur í fyrir uppfærslu.

Nánari upplýsingar um notkun **Setja inn mótreikning eigna** aðgerð á eignafjárhagslínur skal skoða, til dæmis, [Endurmeta eignir](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Úthlutunarlyklar eigna eru settir þannig upp:
Hægt er að úthluta færslum á ýmsar deildir og/eða verkefni samkvæmt úthlutunarlyklum sem notandi skilgreinir. Setja má upp úthlutunarlykil sem skiptir til dæmis hlutdeild í afskriftakostnaði af bílum í 35 prósent á stjórnunardeild og 65 prósent á söludeild. Frekari upplýsingar eru í [Úthluta kostnaði og tekjum](year-allocate-costs-income.md).

Úthlutunarlyklar gilda um eignaflokka en ekki um stakar eignir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignabókunarflokkar** og veldu síðan tengda tengilinn.  
2. Á síðunni **Eignabókunarflokkar** skal velja aðgerðina **Úthlutanir** og velja síðan bókunarflokk.
3. Á síðunni **eignaúthlutanir** þarf að fylla reitina út eftir þörfum.
4. Endurtaktu skref 2 og 3 fyrir hverja bókunargerð sem ætlunin er að skilgreina úthlutunarlykla fyrir.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Setja upp sniðmát eignabóka
Sniðmát er fyrirfram skilgreind uppsetning á færslubók. Í sniðmáti eru upplýsingar um ferilskóta, skýrslur og númeraraðir. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] býr sjálfkrafa til sniðmát færslubókar eignar í fyrsta sinn sem síðan **Færslubók eignar** er opnuð, en hægt er að setja upp önnur sniðmát færslubókar.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sniðmát færslubókar** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Setja upp keyrslur eignabóka
Hægt er að setja upp margar bókarkeyrslur sem eru sérstakar færslubækur fyrir hvert færslubókarsniðmát. Starfsmenn geta til dæmis verið með eigin bókarkeyrslur sem nota upphafsstafi starfsmannsins sem heiti bókarkeyrslu. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sniðmát færslubókar** og veldu síðan tengda tengilinn.  
2. Valin er viðeigandi sniðmát færslubókar og veldu svo **keyrslur** aðgerðina.
3. Á síðunni **eignabókarkeyrslur** þarf að fylla reitina út eftir þörfum.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Setja upp keyrslur endurflokkunarsniðmáta
Hægt er að nota eignaendurflokkunarbókina til að flytja eignir, skipta þeim upp eða sameina þær. [!INCLUDE[d365fin](includes/d365fin_md.md)] býr sjálfkrafa til sniðmát endurflokkunarbókar eignar í fyrsta sinn sem síðan **Endurflokkunarbók eignar** er opnuð, en hægt er að setja upp önnur sniðmát endurflokkunarbókar. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sniðmát eignaendurflokkunarbókar** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Setja upp endurflokkunarkeyrslur eignabóka
Hægt er að setja upp margar bókarkeyrslur sem eru sérstakar færslubækur fyrir hvert sniðmát endurflokkunarbókar. Starfsmenn geta til dæmis verið með eigin endurflokkunarbókarkeyrslur sem nota upphafsstafi starfsmannsins sem heiti bókarkeyrslu. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sniðmát eignaendurflokkunarbókar** og veldu síðan tengda tengilinn.  
2. Valin er viðeigandi sniðmát færslubókar og veldu svo **keyrslur** aðgerðina.
3. Á síðunni **keyrslur eignaendurflokkunarbókar** þarf að fylla reitina út eftir þörfum.

## <a name="to-set-up-fixed-asset-class-codes"></a>Uppsetning eignaflokkskóða
Flokkskóðana er hægt að nota við aðalflokkun eigna, eins og til dæmis í áþreifanlegar og óáþreifanlegar eignir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignarflokkar** og veldu síðan tengda tengilinn.
2. Færðir eru inn kótar og heiti á flokkunum sem búa á til.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Uppsetning eignaundirflokkskóða
Kóðar eignaundirflokks eru notaðir til að flokka eignir, s.s. í byggingar, ökutæki, húsbúnað eða vélbúnað.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Undirflokkar eigna** og veldu síðan tengda tengilinn.
2. Færðir eru inn kótar og heiti á flokkunum sem búa á til.

## <a name="to-set-up-fixed-asset-location-codes"></a>Staðsetningarkóðar eigna eru settir þannig upp:
Eignastaðsetningarkóta eru notaðir til að skrá staðsetningu eignarinnar, s.s. í söludeild, móttöku, stjórnunardeild, framleiðsludeild eða vöruhúsi. Þessar upplýsingar koma að gagni við vátryggingar og birgðir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **birgðageymslur eigna** og veldu síðan tengda tengilinn.
2. Færðir eru inn kóðar og heiti á staðsetningum eigna sem búa á til.

## <a name="to-register-opening-entries"></a>Skráning opnunarfærslna
Ef verið er að nota eignirnar í [!INCLUDE[d365fin](includes/d365fin_md.md)] í fyrsta sinn, verður að setja upp fjárhagskerfishlutann áður en eignir eru settar upp. Hvernig þetta er gert fer eftir því hvort eignir séu hluti af fjárhag.  

 Eftirfarandi aðferð er notuð ef bóka á eignafærslur í fjárhag.  

1. Gæta skal þess að lokið sé við grunnuppsetningu eigna.  
2. Búið er til eignaspjald fyrir hverja eign sem til er.  
3. Stofna eigna-/afskriftabók fyrir hvern afskriftartilgang (til dæmis fyrir skattinn og fjárhagsskýrslur). Fyrir hverja afskriftabók þarf að skilgreina skilmála og skilyrði, eins og sameiningu við fjárhag.  

    Virkja fjárhagssamþættingu með því að fylgja næstu skrefum. Fyrst skal ganga úr skugga um að slökkt sé á fjárhagssamþættingu fyrir allar afskriftarbækur, og svo bóka opnu færslurnar og að lokum kveikja á fjárhagssamþættingu.  
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabækur** og veldu síðan tengda tengilinn.  
5. Velja skal viðeigandi afskriftabók. Á flipanum **Heim** í flokknum **Stjórna** veljið **Breyta lista** til að opna síðuna **Afskriftabókarspjald**.
6. Ganga skal úr skugga um að á flýtiflipanum **Heildun** séu allir reitir auðir með því að hreinsa öll gátmerki. Ef um er að ræða fleiri en eina afskriftabók er skal óvirkja fjárhagsheildun fyrir hverja þeirra.  
7. Í eignabókinni eru færðar eftirfarandi línur fyrir hverja eign:
   * Færð er inn lína með stofnkostnaðinum.
   * Lína með uppsafnaðar afskriftir til loka fyrra fjárhagsárs.
   * Lína með uppsafnaðar afskriftir frá upphafi yfirstandandi reikningsárs til dagsetningarinnar sem [!INCLUDE[d365fin](includes/d365fin_md.md)] er stillt á og setur af stað útreikning á afskriftunum.

    Ef aðrar mótfærslur eru opnar eru einnig hægt að færa þær inn núna, til dæmis niðurfærsla og uppfærsla.  
8. Þegar lokið er við að færa inn og bókað færslubókarlínur fyrir hverja eign, skal kveikja á fjárhagsheildun í afskriftarbókunum.

Ef eignirnar eru ekki samþættar fjárhag er sleppt lið 6 og 8.

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
