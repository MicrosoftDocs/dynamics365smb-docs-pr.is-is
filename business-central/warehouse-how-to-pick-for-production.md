---
title: Hvernig á að tína fyrir framleiðslu með einföldum vöruhúsaaðgerðum | Microsoft Docs
description: Þegar vöruhúsið krefst tínsluvinnslu en ekki afhendingarvinnslu er síðan **Birgðatínsla** notuð til að skipuleggja og skrá tínslu íhluta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 214ac7824dadca7d63c4ed1b91273a7409850e12
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249607"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss
Hátturinn við frágang tínsluíhluta fyrir framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan krefst tínsluvinnslu en ekki afhendingarvinnslu er síðan **Birgðatínsla** notuð til að skipuleggja og skrá tínslu íhluta.  

Í einfaldri vöruhúsagrunnstillingu er nauðsynlegt að taka til fyrir samsetningarpantanir með síðunni **Birgðahreyfing**. Nánari upplýsingar eru í [Meðhöndlun á vörum samsetningarpöntunar með birgðatínslum](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar er síðan **Vöruhúsatínsla** notuð til að færa íhluti til framleiðslu eða samsetningarpantana. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

> [!NOTE]  
>  Hér á eftir er mikilvægur mismunur sem er á milli birgðatínslu og birgðahreyfinga.  
>   
>  -   Þegar birgðatínsla er skráð fyrir innri aðgerð, s.s. framleiðslu, er notkun fyrir tínda hluti bókuð samhliða. Þegar birgðahreyfing er skráð fyrir innri aðgerð þarf aðeins að skrá raunverulegan flutning nauðsynlegs íhlutar að hólfi í rekstrarsvæðinu án þess að bóka notkun.  
> -   Þegar birgðatínsla er notuð skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar hólfið *taka* hvaðan íhlutir eru minnkaðir þegar notkun er bókuð. Þegar birgðahreyfingar eru notaðar, skilgreinir reiturinn **Hólfkóti** í framleiðslupöntunaríhlutalínum hólfið *setja* í aðgerðasvæðinu þar sem starfsmaður í vöruhúsi verður setja íhlutina.  

Áður en hægt er að tína eða færa íhluti fyrir upprunaskjöl, gildir sú kerfisforsenda að vöruhúsabeiðni á útleið sé til staðar til að tilkynna vöruhúsasvæðinu um íhlutsþörfina. Vöruhúsabeiðnin út er stofnuð hvenær sem framleiðslupöntunarstaðan breytist í Útgefin eða þegar útgefna framleiðslupöntunin er stofnuð.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Tína íhluti í einfaldri vöruhúsagrunnstillingu
Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan notar eingöngu tínslu, eru íhlutir tíndir fyrir framleiðsluaðgerðir með síðunni **Birgðatínsla**. Frekari upplýsingar, sjá [Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðatínsla** og veldu síðan tengda tengilinn.  
2.  Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
3.  Tínslan er framkvæmd og síðan eru rauntínsluupplýsingarnar skráðar í reitnum **Tínt magn**.  
4.  Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar notkun varanna.  

Einnig er hægt að stofna **Birgðatínslu** beint úr útgefnu framleiðslupöntuninni. Veljið aðgerðina **Stofna birgðafrágang/tínslu**, veljið gátreitinn **Stofna birgðatínslu** og smellið síðan á hnappinn **Í lagi**.

Einnig er hægt að nota síðuna **Birgðahreyfingar** til að færa vörur milli hólfa á tilfallandi hátt, þ.e. án tilvísunar í upprunaskjal.
Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun setja saman í pöntun íhluta við birgðatínslu
Síðan **Birgðatínsla** er einnig notaður til að tína og senda vegna sölu þar sem vörur verða að vera samsettar áður en hægt er að senda þær. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Vörur sem á að afhenda eru ekki efnislega til staðar í hólfi fyrr en þær eru settar saman og bókaðar sem frálag í hólf í samsetningarsvæði. Þetta þýðir að tínsla vara sem sameina á í pöntun fyrir afhending fylgir ákveðnu flæði. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna. Bókaða birgðatínslan bókar svo samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Til að virkja þetta þarf að velja reitinn **Búa til hreyfingar sjálfvirkt** á síðunni **Uppsetning samsetningar**. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Birgðatínslulínurnar fyrir söluvörur eru stofnaðar á mismunandi hátt eftir því hvort ekkert, sumt eða allt magn sölulínunnar er sett saman í pöntun.

Í venjulegri sölu þar sem birgðatínsla er notuð til að bóka afhendingu birgðamagns, er ein birgðatínslulína búin til, eða fleiri ef varan er sett í mismunandi hólf. Þessi tínslulína grundvallast af magninu í reitnum **Magn til afhendingar**.

Í sölu með samsetningarpöntun þar sem allt magn línu sölupöntunarinnar er sett saman í pöntun er ein birgðatínslulína búin til fyrir magnið. Þetta þýðir að gildið í reitnum Magn til samsetningar er það sama og gildið í reitnum **Magn til afhendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna eru gildið í reitnum **Setja saman í pöntun hólfakóði** eða gildið í reitnum **Frá samsetningu hólfakóði**, í þeirri röð, sett inn í reitinn **Hólfakóði** í birgðatínslulínunni.

Ef enginn hólfskóði er gefinn upp í sölupöntunarlínunni og samsetningarfrálagsflæði hefur ekki verið sett upp fyrir birgðageymsluna er reiturinn **Hólfakóði** í birgðatínslulínunni er auður. Starfsmaður í vöruhúsi verður að opna síðuna **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Við blandaðar aðstæður, þar sem fyrst þarf að setja saman hluta magnsins og tína þarf annað magn úr birgðum, eru minnst tvær birgðatínslulínur búnar til. Ein tínslulína er fyrir sameiningarpöntunarmagnið. Hin tínslulínan fer eftir hvaða hólf geta uppfyllt eftirstöðvar úr birgðum. Hólfkóti á línunum tveimur er fylltur út er á mismunandi hátt eins og lýst er fyrir þessar tvær mismunandi sölutegundir. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið
Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfa](media/binflow.png "Hólfaflæði")

## <a name="see-also"></a>Sjá einnig
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
