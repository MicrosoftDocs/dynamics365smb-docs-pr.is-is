---
title: Hvernig á að selja vörur sem eru settar saman í pöntun | Microsoft Docs
description: Ef varan er settu upp til samsetningar til pöntunar er ekki gert ráð fyrir því að varan sé í birgðum og þá þarf að setja hana saman fyrir þessa sölupöntun. Þegar varan er sett inn í sölupöntunarlínu er samsetningarpöntun síðan búin til sjálfkrafa og tengd við sölupöntunina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92a1faa77132e4f26c1999411f6d8304c24dd8f7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772905"
---
# <a name="sell-items-assembled-to-order"></a>Selja hluti sem eru settir saman í pöntun
Ef reiturinn **Samsetningarstefna** á birgðaspjaldi samsetningarvörunnar er **Samsetning til pöntunar** er ekki gert ráð fyrir því að varan sé í birgðum og þá þarf að setja hana saman fyrir þessa sölupöntun. Þegar varan er sett inn í sölupöntunarlínu er samsetningarpöntun síðan búin til sjálfkrafa og tengd við sölupöntunina.  

> [!NOTE]  
>  Ef einhverjar samsetningarpöntunarvörur eru þegar í birgðum er hægt að draga það magn frá samsetningarpöntuninni og taka það frá í birgðum. Frekari upplýsingar eru í [Selja birgðavörur í flæðum samsetningar í pöntun](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Í þessu ferli er sala vöru sem verður sett saman samkvæmt óskum viðskiptamannsins meðhöndluð. Skrefin eru meðal annars að hefja sölupöntunarlínuna, sérsníða samsetningarvöruna með því að breyta íhlutum hennar og forða, athuga hvað er til ráðstöfunar til að ákveða skiladag og gefa út sölupöntun sem setja má saman og afhenda tafarlaust.  

> [!NOTE]  
>  Eftirfarandi ferli inniheldur ekki stöðluðu sölupöntunarskrefin fyrir skrefið þegar birgðir sem settar eru saman í pöntun eru færðar inn í sölupöntunarlínu.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Til að selja vöru sem er sett saman í pöntun  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Stofnið sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  
3.  Í reitnum **númer** færið inn vöru sem stillt eru til að setja saman í pöntun.  
4.  Í reitnum **Kóti birgðageymslu** er tilgreind sú birgðageymsla sem varan mun verða seld frá. Samsetningarferlið fer fram í þeirri birgðageymslu.  
5.  Í reitnum **Magn** er fært inn hversu margar einingar á að selja.  

    > [!NOTE]  
    >  Ef einn eða fleiri íhlutir umbeðins magns samsetningarvöru eru ekki tiltækir birtist nákvæm ráðstöfunarviðvörunarsíða. Nánari upplýsingar, sjá samsetning í boði.  

    Samsetningarpöntun er nú stofnuð sjálfkrafa og tengd við sölupöntunarlínuna. Gjalddagi þessarar samsetningarpöntunar er samstilltur við afhendingardagsetningu sölupöntunarlínunnar.  

    Magnið sem á að selja er afritað í reitinn **Magn Til að setja saman í pöntun**, sem þýðir að uppsetning vörunnar býst við að allt magn í sölulínunni sé sett saman í pöntunina. Hægt er að minnka magnið til að setja saman í pöntun, t. d. ef vitað er að sumar vörur eru þegar til staðar. Frekari upplýsingar eru í [Selja birgðavörur í flæðum samsetningar í pöntun](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Til að gefa til kynna að viðskiptavinur vill aukavöru í setti er farið í flýtiflipann **Línur** , aðgerðin **Lína** valin, síðan **Sameina í pöntun** aðgerðin og svo **Sameina-í-pöntun línur** aðgerðin til að skoða og breyta stöðluðum samsetningaríhlutum. Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar**.  
7.  Á síðunni **Setja saman í pöntunarlínur** stofnið nýja tegund línu **Atriði** vegna viðbótarinnihalds setts sem beðið var um. Línan stendur fyrir annan samsetningaríhlut.  

    Einnig er hægt að sérsníða pöntun með því að auka magni einnar af staðalvöru í setti. Hægt er að gera þetta með því að auka gildið í reitnum **Magn á** á viðkomandi samsetningarpöntunarlínu.  

    > [!NOTE]  
    >  Síðan **Setja-saman-í-pöntun línur** hefur aðeins að geyma grunnsvæði sem vænst er að sölufulltrúi noti til að sérsníða íhlutalistann, bæta við vörurakningarnúmeri eða leysa vandamál með framboð íhluta. Til að sjá frekari upplýsingar um samsetningarpöntun, til dæmis upphafsdagsetningu samsetningarpöntunarinnar, er aðgerðin **Sýna skjöl** valin. Þá opnast fullt yfirlit yfir samsetningarpöntunina sem er tengd við sölupöntunarlínuna. Ekki er hægt að breyta innihaldi flestra reita í haus samsetningarpöntunar, og ekki er hægt að bóka frálag samsetningar þar sem nota þarf afhendingarbókun sölupöntunarlínunnar.  
    >   
    >  Í haus tengdra samsetningarpantana, getur aðeins reitnum **Upphafsdagsetning** verið breytt til að virkja samsetningarstarfsmenn til að tilgreina dagsetningu sem er á undan gjalddaga um hvenær þeir munu hefja ferlið. Öllum reitum í línunum á tengdu samsetningarpöntuninni er hægt að breyta svo að vöruhússstarfsmenn geti fært inn notkunartölur við vinnsluna.  

8.  Fara skal yfir eða bregðast við vandamálum með ráðstöfun íhluta. Veljið til dæmis tiltæka staðgengdarvöru eða komið á nýjum gjalddaga.  
9. Loka síðunni **Setja saman í pöntunarlínur**. Tengda samsetningarpöntunin er nú tilbúin til að hefja samsetningu sérsniðnu vörunnar eftir gjalddaganum.  
10. Á sölupöntuninni skal velja **Losa** aðgerðina til að tilkynna samsetningardeildinni að sem samsetningarferlið geti hafist.  
11. Í samsetningardeildinni, framkvæmið aðgerðir samsetningu varanna sem seldar eru í þessu ferli. Nánari upplýsingar, sjá [Sameina vörur](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Sjá einnig  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]