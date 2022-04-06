---
title: Tína framleiðslu eða samsetningu í einföldu vöruhúsi
description: Þegar staðsetning vöruhússins krefst tínsluvinnslu en ekki afhendingarvinnslu skal nota Birgðatínslusíðuna til að skipuleggja og skrá tínslu hluta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: b7be198a27a5c0a95aacb9c6eca988681d097316
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515226"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss
Hátturinn við frágang tínsluíhluta fyrir framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).


## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Tína fyrir framleiðslu með einföldum vörhúsagrunnstillingum
Losunaraðferð hefur einnig áhrif á flæði íhluta í framleiðslu. Nánari upplýsingar eru í [Birgðaskrá íhluti samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar þarf að nota síðuna **Vöruhúsatínsla** til að færa íhluti með losunaraðferð stillta á *Handvirkt*, *Tína + framvirkt*, *Tína + afturvirkt* yfir í framleiðslupantanir. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

Í einfaldri vöruhúsagrunnstillingu þar sem staðsetningin krefst tínsluvinnslu en ekki afhendingarvinnslu er einnig hægt að nota síðuna **Birgðatínsla** til að skipuleggja og skrá tínslu íhluta með losunaraðferð stillta á *Handvirkt*. Þegar birgðatínsla er skráð fyrir innri aðgerð, s.s. framleiðslu, er notkun fyrir tínda hluti bókuð samhliða. Einnig er hægt að nota **Birgðahreyfingar** með tilvísun í upprunaskjal til að færa íhluti með losunaraðferð stillta á *Handvirkt*, *Tína + framvirkt*, *Tína + afturvirkt* yfir í framleiðslupantanir.

Þegar framleiðsluaðgerðir eru samþættar við vöruhúsaferli, annaðhvort af hólfum eða með stýrðum frágangi og tínslu, er hólfið sem íhlutirnir eru notaðir úr hólfið sem skilgreint er á hverri íhlutalínu framleiðslupöntunar. Allar íhlutir sem þörf er á verða að vera tiltækir í því hólfi. Annars er handvirk eða sjálfvirk notkunarbókun stöðvuð fyrir íhlutinn.

**Birgðahreyfing** með tilvísanir í upprunaskjalið og **Vöruhúsatínslu** er ekki hægt að nota til að tína íhluti með losunaraðferðunum *Framvirkt* og *Afturvirkt*. Ekki er hægt að nota **Birgðatínsla** til að tína íhluti með neinni losunaraðferð nema *Handvirkt*. Til að sjá um eftirstandandi íhluti skal nota **Birgðahreyfingu** án tilvísana í upprunaskjal. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

> [!NOTE]  
>  Eftirfarandi mikilvægur munur er til milli birgðatínslna, birgðahreyfinga og vöruhúsatínsla:  
>   
>  -   Þegar birgðatínsla er skráð fyrir innri aðgerð, s.s. framleiðslu, er notkun fyrir tínda hluti bókuð samhliða. Þegar birgðahreyfing er skráð fyrir innri aðgerð eða vöruhúsatínslu þarf aðeins að skrá raunverulegan flutning nauðsynlegs íhlutar að hólfi í rekstrarsvæðinu án þess að bóka notkun.  
> -   Þegar birgðatínsla er notuð skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar hólfið *taka* hvaðan íhlutir eru minnkaðir þegar notkun er bókuð. Þegar birgðahreyfingar eru notaðar í vöruhúsatínslu skilgreinir reiturinn **Hólfkóti** í framleiðslupöntunaríhlutalínum hólfið *setja* í aðgerðasvæðinu þar sem starfsmaður í vöruhúsi verður setja íhlutina.  

Áður en hægt er að tína eða færa íhluti fyrir upprunaskjöl, gildir sú kerfisforsenda að vöruhúsabeiðni á útleið sé til staðar til að tilkynna vöruhúsasvæðinu um íhlutsþörfina. Vöruhúsabeiðnin út er stofnuð hvenær sem framleiðslupöntunarstaðan breytist í Útgefin eða þegar útgefna framleiðslupöntunin er stofnuð.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Að tína framleiðsluíhluti í grunnstillingum vöruhúss með birgðatínslu
Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan notar eingöngu tínslu, eru íhlutir tíndir fyrir framleiðsluaðgerðir með síðunni **Birgðatínsla**. Frekari upplýsingar, sjá [Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2.  Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
3.  Tínslan er framkvæmd og síðan eru rauntínsluupplýsingarnar skráðar í reitnum **Magn til afgreiðslu**.  
4.  Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar notkun varanna.  

Einnig er hægt að stofna **Birgðatínslu** beint úr útgefnu framleiðslupöntuninni. Veljið aðgerðina **Stofna birgðafrágang/-tínslu/-hreyfingu**, veljið gátreitinn **Stofna birgðatínslu** og smellið síðan á hnappinn **Í lagi**.

Annars er hægt að nota **Birgðahreyfinguna** með tilvísun í upprunaskjalið til að færa vörur á milli hólfa. Notkun þarf að skrá sérstaklega. Frekari upplýsingar er að finna í [Fjöldabóka framleiðslunotkun](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Tiltekt fyrir samsetningu í grunnstillingum vöruhúss
Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar þarf að nota síðuna **Vöruhúsatínsla** til að færa íhluti til samsetningarpantana. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

Í einfaldri vöruhúsagrunnstillingu er einnig hægt að taka til fyrir samsetningarpantanir með síðunni **Birgðahreyfing**. 

Í grunnstillingum vöruhúss þar sem staðsetningin krefst tínsluvinnslu en ekki afhendingarvinnslu er síðan **Birgðatínsla** einnig notuð til að tína, safna saman og senda fyrir sölupöntun þar sem sameina þarf vörur áður en þær eru sendar. Nánari upplýsingar eru í [Meðhöndlun á vörum samsetningarpöntunar með birgðatínslum](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun setja saman í pöntun íhluta við birgðatínslu
Síðan **Birgðatínsla** er einnig notaður til að tína og senda vegna sölu þar sem vörur verða að vera samsettar áður en hægt er að senda þær. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Vörur sem á að afhenda eru ekki efnislega til staðar í hólfi fyrr en þær eru settar saman og bókaðar sem frálag í hólf í samsetningarsvæði. Þetta þýðir að tínsla vara sem sameina á í pöntun fyrir afhending fylgir ákveðnu flæði. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna. Bókaða birgðatínslan bókar svo samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Til að virkja þetta þarf að velja reitinn **Búa til hreyfingar sjálfvirkt** á síðunni **Uppsetning samsetningar**. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Birgðatínslulínurnar fyrir söluvörur eru stofnaðar á mismunandi hátt eftir því hvort ekkert, sumt eða allt magn sölulínunnar er sett saman í pöntun.

Í venjulegri sölu þar sem birgðatínsla er notuð til að bóka afhendingu birgðamagns, er ein birgðatínslulína búin til, eða fleiri ef varan er sett í mismunandi hólf. Þessi tínslulína grundvallast af magninu í reitnum **Magn til afhendingar**.

Í sölu með samsetningarpöntun þar sem allt magn línu sölupöntunarinnar er sett saman í pöntun er ein birgðatínslulína búin til fyrir magnið. Þetta þýðir að gildið í reitnum Magn til samsetningar er það sama og gildið í reitnum **Magn til afhendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna eru gildið í reitnum **Setja saman í pöntun hólfakóði** eða gildið í reitnum **Frá samsetningu hólfakóði**, í þeirri röð, sett inn í reitinn **Hólfakóði** í birgðatínslulínunni.

Ef enginn hólfskóði er gefinn upp í sölupöntunarlínunni og samsetningarfrálagsflæði hefur ekki verið sett upp fyrir birgðageymsluna er reiturinn **Hólfakóði** í birgðatínslulínunni er auður. Starfsmaður í vöruhúsi verður að opna síðuna **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Við blandaðar aðstæður, þar sem fyrst þarf að setja saman hluta magnsins og tína þarf annað magn úr birgðum, eru minnst tvær birgðatínslulínur búnar til. Ein tínslulína er fyrir sameiningarpöntunarmagnið. Hin tínslulínan fer eftir hvaða hólf geta uppfyllt eftirstöðvar úr birgðum. Hólfkóti á línunum tveimur er fylltur út er á mismunandi hátt eins og lýst er fyrir þessar tvær mismunandi sölutegundir. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið
Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfs.](media/binflow.png "BinFlow")

## <a name="see-also"></a>Sjá einnig
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
