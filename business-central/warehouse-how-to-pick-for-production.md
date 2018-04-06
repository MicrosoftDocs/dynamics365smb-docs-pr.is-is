---
title: "Hvernig á að tína fyrir framleiðslu með einföldum vöruhúsaaðgerðum | Microsoft Docs"
description: "Þegar vöruhúsið krefst tínsluvinnslu en ekki afhendingarvinnslu er glugginn **Birgðatínsla** notaður til að skipuleggja og skrá tínslu íhluta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bd8bf55a69833745739a5c575bee2a3818cb7634
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-production-or-assembly"></a>Taka til fyrir framleiðslu eða samsetningu
Hátturinn við frágang tínsluíhluta fyrir framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan krefst tínsluvinnslu en ekki afhendingarvinnslu er glugginn **Birgðatínsla** notaður til að skipuleggja og skrá tínslu íhluta.  

Í einfaldri vöruhúsagrunnstillingu er nauðsynlegt að taka til fyrir samsetningarpantanir með glugganum **Birgðahreyfing**. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu” í [Tína vörur með Birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).  

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar er **Vöruhúsatínsla** glugginn notaður til að færa íhluti til framleiðslu eða samsetningarpantana.

> [!NOTE]  
>  Hér á eftir er mikilvægur mismunur sem er á milli birgðatínslu og birgðahreyfinga.  
>   
>  -   Þegar birgðatínsla er skráð fyrir innri aðgerð, s.s. framleiðslu, er notkun fyrir tínda hluti bókuð samhliða. Þegar birgðahreyfing er skráð fyrir innri aðgerð þarf aðeins að skrá raunverulegan flutning nauðsynlegs íhlutar að hólfi í rekstrarsvæðinu án þess að bóka notkun.  
> -   Þegar birgðatínsla er notuð skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar hólfið *taka* hvaðan íhlutir eru minnkaðir þegar notkun er bókuð. Þegar birgðahreyfingar eru notaðar, skilgreinir reiturinn **Hólfkóti** í framleiðslupöntunaríhlutalínum hólfið *setja* í aðgerðasvæðinu þar sem starfsmaður í vöruhúsi verður setja íhlutina.  

Áður en hægt er að tína eða færa íhluti fyrir upprunaskjöl, gildir sú kerfisforsenda að vöruhúsabeiðni á útleið sé til staðar til að tilkynna vöruhúsasvæðinu um íhlutsþörfina. Vöruhúsabeiðnin út er stofnuð hvenær sem framleiðslupöntunarstaðan breytist í Útgefin eða þegar útgefna framleiðslupöntunin er stofnuð.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Tína íhluti í einfaldri vöruhúsagrunnstillingu
Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan notar eingöngu tínslu, eru íhlutir tíndir fyrir framleiðsluaðgerðir með glugganum **Birgðatínsla**. Frekari upplýsingar, sjá [Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatínsla** og velja svo viðeigandi tengil.  
2.  Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
3.  Tínslan er framkvæmd og síðan eru rauntínsluupplýsingarnar skráðar í reitnum **Tínt magn**.  
4.  Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar notkun varanna.  

Einnig er hægt að stofna **Birgðatínslu** beint úr útgefnu framleiðslupöntuninni. Veljið aðgerðina **Stofna birgðafrágang/tínslu**, veljið gátreitinn **Stofna birgðatínslu** og smellið síðan á hnappinn **Í lagi**.

Einnig er hægt að nota gluggann **Birgðahreyfingar** til að færa vörur milli hólfa á tilfallandi hátt, þ.e. án tilvísunar í upprunaskjal.
Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun setja saman í pöntun íhluta við birgðatínslu
Glugginn **Birgðatínsla** er einnig notaður til að tína og senda vegna sölu þar sem vörur verða að vera samsettar áður en hægt er að senda þær. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Vörur sem á að afhenda eru ekki efnislega til staðar í hólfi fyrr en þær eru settar saman og bókaðar sem frálag í hólf í samsetningarsvæði. Þetta þýðir að tínsla vara sem sameina á í pöntun fyrir afhending fylgir ákveðnu flæði. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna. Bókaða birgðatínslan bókar svo samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Til að virkja þetta þarf að velja reitinn **Búa til hreyfingar sjálfvirkt** í **Uppsetning samsetningar** glugganum. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Birgðatínslulínurnar fyrir söluvörur eru stofnaðar á mismunandi hátt eftir því hvort ekkert, sumt eða allt magn sölulínunnar er sett saman í pöntun.

Í venjulegri sölu þar sem birgðatínsla er notuð til að bóka afhendingu birgðamagns, er ein birgðatínslulína búin til, eða fleiri ef varan er sett í mismunandi hólf. Þessi tínslulína grundvallast af magninu í reitnum **Magn til afhendingar**.

Í sölu með samsetningarpöntun þar sem allt magn línu sölupöntunarinnar er sett saman í pöntun er ein birgðatínslulína búin til fyrir magnið. Þetta þýðir að gildið í reitnum Magn til samsetningar er það sama og gildið í reitnum **Magn til afhendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna eru gildið í reitnum **Setja saman í pöntun hólfakóði** eða gildið í reitnum **Frá samsetningu hólfakóði**, í þeirri röð, sett inn í reitinn **Hólfakóði** í birgðatínslulínunni.

Ef enginn hólfskóði er gefinn upp í sölupöntunarlínunni og samsetningarfrálagsflæði hefur ekki verið sett upp fyrir birgðageymsluna er reiturinn **Hólfakóði** í birgðatínslulínunni er auður. Starfsmaður í vöruhúsi verður að opna gluggann **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Við blandaðar aðstæður, þar sem fyrst þarf að setja saman hluta magnsins og tína þarf annað magn úr birgðum, eru minnst tvær birgðatínslulínur búnar til. Ein tínslulína er fyrir sameiningarpöntunarmagnið. Hin tínslulínan fer eftir hvaða hólf geta uppfyllt eftirstöðvar úr birgðum. Hólfkóti á línunum tveimur er fylltur út er á mismunandi hátt eins og lýst er fyrir þessar tvær mismunandi sölutegundir. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Tína íhluti í ítarlegri vöruhúsagrunnstillingu
Í ítarlegri vöruhúsastillingu þar sem birgðageymslan notar tínslu auk afhendingar eru íhlutir tíndir fyrir framleiðslu- og samsetningarverkþætti með glugganum **Vöruhús - Tína**. Frekari upplýsingar, sjá [Tína Vörur með vöruhúsatínslu](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Einnig er hægt að nota gluggann **Vinnublað hreyfingar** til að færa vörur milli hólfa á tilfallandi hátt, þ. e. a. án tilvísunar í upprunaskjal. Frekari upplýsingar eru í [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni þar sem tínsluaðgerð er alltaf hluti af verkflæði, annað hvort sem dráttur eða ýting.  

Einnig er hægt að stofna vöruhúsatínsluskjöl í ýtingu með því að velja aðgerðina **Stofna vöruhússtínslu** á upprunaskjalinu, eins og útgefna samsetningarpöntun eða vöruhúsaafhendingu. Frekari upplýsingar, sjá [Tína Vörur með vöruhúsatínslu](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Einnig er hægt að stofna vöruhúsatínsluskjal eins og drátt með því að nota gluggann **Vinnublað tínslu** til að finna tínslubeiðnir, bæði til afhendingar og innri aðgerða, og síðan stofna nauðsynleg vöruhúsatínsluskjöl.  

Eftirfarandi ferli skýrir dæmi þar sem valdir eru íhlutir fyrir afhenta framleiðslupöntun í gegnum gluggann **Vinnublað tínslu**. Ferlið á einnig við fyrir samsetningarpantanir  

Til að stofna tínslubeiðnir, bæði fyrir tog- og ýtidæmi, þurfa viðkomandi upprunaskjöl að vera útgefin. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

 |Upprunaskjal|Losunaraðferð|  
 |---------------------|--------------------|  
 |Framleiðslupöntun|Breyta tegund pöntunar í útgefna framleiðslupöntun.|  
 |Samsetningarpöntun|Breyta stöðu í Útgefið.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Íhlutir tíndir úr tínsluvinnublöðunum:  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vinnublað tínslu** og velja svo viðeigandi tengil.  
2.  Velja skal **Sækja vöruhúsaskjöl** og síðan velja íhlutalínurnar í útgefnu framleiðslupöntuninni.  
3.  Línurnar eru skoðaðar, þeim raðað til að tryggja skilvirkni tínsluferðarinnar og þær sameinaðar öðrum vinnublaðslínum ef þarf, til að nýta tíma starfsmanna sem best.  
4.  Veldu aðgerðina **Stofna tínslu**.  
5.  Skilgreina hvernig eigi að stofna vöruhúsatínsluskjöl og hvernig á að raða tínslulínunum með því að fylla út reiti í gluggnum **Stofna tínslu**.  
6.  Velja hnappinn **Í lagi**.

Vöruhúsatínsluskjöl eru nú búin til með tínslulínum fyrir hvern íhlut sem er krafist í innri aðgerð.

Ef svæði innri starfsemi, s.s. framleiðsluvinnusalur, er sett upp með sjálfgefnu hólfi fyrir staðsetningu íhluta sem notaðir eru verður kóti þess hólfs settur inn í Setja-línur í tínsluskjali vöruhússins til að leiðbeina starfsmönnum í vöruhúsi um hvert setja eigi vörurnar. Frekari upplýsingar, sjá [Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

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

