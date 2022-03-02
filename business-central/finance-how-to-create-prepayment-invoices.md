---
title: Stofna fyrirframgreiðslureikninga
description: Takist á við aðstæður þar sem þú eða lánardrottinn þinn krefjast fyrirframgreiðslu. Notið sjálfgefnar prósentur fyrir hverja sölu- og innkaupalínu eða leiðréttið upphæðina eins og með þarf.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: c1374929790c27bd84733e506866a1e54cea9ffd
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136063"
---
# <a name="create-prepayment-invoices"></a>Stofna fyrirframgreiðslureikninga

Ef þú gerir kröfu um að viðskiptavinir inni greiðslu af hendi áður en þú sendir pöntun til þeirra getur þú notað aðgerð fyrirframgreiðslu. Sama gildir ef lánardrottinn þinn krefst þess að þú innir greiðslu af hendi áður en hann sendir pöntun til þín.  

Hægt er að hefja fyrirframgreiðsluferlið þegar búið er að stofna sölu- eða innkaupapöntun. Ef um er að ræða sjálfgefna fyrirframgreiðsluprósentu fyrir tiltekna vöru í pöntuninni eða fyrir þennan viðskiptavin eða lánardrottin, verður hún sjálfkrafa innifalin á fyrirframgreiðslureikningnum. Einnig er hægt að tilgreina fyrirframgreiðsluprósentuna fyrir allt skjalið.

Þegar búið er að stofna sölu- eða innkaupapöntun er hægt að stofna fyrirframgreiðslureikning. Hægt er að nota sjálfgefnar prósentur fyrir sölu- og innkauplínur eða leiðrétta upphæðina eins og með þarf. Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

Eftirfarandi ferli sýnir hvernig skal gefa út fyrirframgreiðslureikning fyrir sölupöntun. Skrefin eru svipuð fyrir innkaupapöntun.  

## <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna nýja sölupöntun fyrir viðeigandi viðskiptavin. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  

    Á flýtiflipanum **Fyrirframgreiðsla** tilgreinir svæðið **Fyrirframgreiðsla %** prósentuna sem á að nota til að reikna út fyrirframgreiðsluupphæðina. Ef sjálfgefin fyrirframgreiðsluprósenta er á spjaldi viðskiptavinar er svæðið sjálfkrafa fylltur út. Hægt er að breyta prósentunni. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Veldu svæðið **Þjappa fyrirframgreiðslu** ef óskað er eftir að stofna línur á fyrirframgreiðslureikningnum sem sameinar línur úr sölupöntuninni ef:  

    - Þær eru með sama fjárhagsreikninginn fyrir fyrirframgreiðslur samkvæmt stillingum í almenna bókunargrunninum.  
    - Þeir hafa sömu víddir.  

    Ekki velja svæðið **Þjappa fyrirframgreiðslu** ef þú vilt tilgreina fyrirframgreiðslureikning með einni línu fyrir hverja sölupöntunarlínu sem hefur fyrirframgreiðsluprósentu.  

    Gjalddagi fyrirframgreiðslunnar er sjálfkrafa reiknaður út frá gildinu í reitnum **Greiðsluskilmálakóði fyrirframgr.**.

3. Sölulínurnar eru fylltar út.  

    Ef þú hefur tilgreint sjálfgefna fyrirframgreiðsluprósentuna annað hvort fyrir viðskiptavininn eða á flýtiflipanum **Fyrirframgreiðsla** í þessu skjali, er þetta gildi afritað í hverja línu. Hægt er að breyta innihaldi reitsins **Fyrirframgreiðsla %** í línunni.  

    > [!TIP]
    > Ef reiturinn **Fyrirframgreiðsla %** sést ekki er hægt að bæta því við með sérstillingu.  Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

4. Veldu **Upplýsingar** aðgerðina til að skoða heildarupphæð fyrirframgreiðslu.

    Ef leiðrétta á heildarupphæð fyrirframgreiðslunnar fyrir pöntunina er hægt að breyta innihaldi reitsins **Upphæð fyrirframgreiðslu** á síðunni **Tölfræði sölupöntunar**.  

    Ef reiturinn **Verð ásamt VSK** er valinn er hægt að breyta reitnum **Upphæð fyrirframgreiðslu með VSK**.  

    Ef þú breytir innihaldi reitsins **Fyrirframgreiðsluupphæð**, mun upphæðinni verða dreift hlutfallslega á milli allra lína, nema þeirra sem hafa **0** í reitnum **Fyrirframgreiðsla %**.  

5. Til að prenta prufuskýrslu áður en fyrirframgreiðslureikningurinn er bókaður skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Prufuskýrsla fyrirframgreiðslu**.  
6. Til að bóka fyrirframgreiðslureikningurinn skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Bóka fyrirframgreiðslureikning**.  

    Fyrirframgreiðslureikningur er bókaður og prentaður með því að velja aðgerðina **Bóka og prenta fyrirframgr.reikning**.  

Hægt er að gefa út viðbótar fyrirframgreiðslureikninga fyrir pöntunina. Þetta er gert með því að hækka upphæð fyrirframgreiðslunnar í einni eða fleiri línum, leiðrétta dagsetningu fylgiskjalsins, ef þess þarf, og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðarinnar.  

> [!NOTE]  
> Ef þú ert í Norður Ameríku, geturðu ekki breytt fyrirframgreiðsluprósentunni eftir að fyrirframgreiðslureikningurinn hefur verið bókaður. Í N-amerísku útgáfu [!INCLUDE[prod_short](includes/prod_short.md)] er komið í veg fyrir þetta, því útreikningur söluskatts yrði annars rangur.  

 Þegar hægt er að bóka restina af reikningnum er hann bókaður eins og hver annar reikningur og fyrirframgreiðsluupphæðin er sjálfvirkt dregin frá þeirri upphæð sem greiða á.  

## <a name="see-also"></a>Sjá einnig

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]