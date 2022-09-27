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
ms.openlocfilehash: ffb2adb5a0ec43da14ee7fd9126c3293ea73ab22
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534913"
---
# <a name="create-prepayment-invoices"></a>Stofna fyrirframgreiðslureikninga

Ef þú þarfnast þess að Viðskiptavinir greiði áður en þú pantar pöntunina er hægt að nota fyrirframgreiðsluaðgerðirnar. Sama gildir ef seljandi krefst þess að Bú sitt sé greitt áður en hann skipar pöntunina.  

Hægt er að hefja fyrirframgreiðsluferlið þegar búið er að stofna sölu- eða innkaupapöntun. Ef sjálfgefin fyrirframgreiðsluprósenta er fyrir vöru í pöntuninni, eða fyrir viðskiptavin eða lánardrottinn, verður prósentan tekin með í fyrirframgreiðslureikninginn. Einnig er hægt að tilgreina fyrirframgreiðsluprósentuna fyrir allt skjalið.

Þegar búið er að stofna sölu-eða innkaupapöntun er hægt að stofna fyrirframgreiðslureikning fyrir hann. Annaðhvort nota sjálfgefnu prósenturnar fyrir hverja sölu-eða innkaupalínu eða leiðrétta upphæðina. Til dæmis væri hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

Eftirfarandi ferli sýnir hvernig skal gefa út fyrirframgreiðslureikning fyrir sölupöntun. Skrefin eru svipuð fyrir innkaupapöntun.  

## <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna nýja sölupöntun fyrir viðeigandi viðskiptavin. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  

    Á flýtiflipanum **Fyrirframgreiðsla** tilgreinir svæðið **Fyrirframgreiðsla %** prósentuna sem á að nota til að reikna út fyrirframgreiðsluupphæðina. Ef það er sjálfgefin fyrirframgreiðsluprósenta á viðskiptamannaspjaldinu er reiturinn fylltur út sjálfkrafa. Hægt er að breyta prósentunni. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Veldu svæðið **Þjappa fyrirframgreiðslu** ef óskað er eftir að stofna línur á fyrirframgreiðslureikningnum sem sameinar línur úr sölupöntuninni ef:  

    - Þær eru með sama fjárhagsreikninginn fyrir fyrirframgreiðslur samkvæmt stillingum í almenna bókunargrunninum.  
    - Þeir hafa sömu víddir.  

    Ef tilgreina á fyrirframgreiðslureikning með einni línu fyrir hverja sölupöntunarlínu sem hefur fyrirframgreiðsluprósentu skal ekki velja **reitinn þjappa fyrirframgreiðslu**.  

    Gjalddagi fyrirframgreiðslunnar er sjálfkrafa reiknaður út frá gildinu í reitnum **Greiðsluskilmálakóði fyrirframgr.**.

3. Sölulínurnar eru fylltar út.  

    Ef tilgreint er sjálfgefið hlutfall fyrirframgreiðslu fyrir viðskiptavin eða á **flipanum fyrirframgreiðsla** á þessu fylgiskjali er þetta gildi afritað í hverja línu. Hægt er að breyta innihaldi reitsins **Fyrirframgreiðsla %** í línunni.  

    > [!TIP]
    > Ef reiturinn fyrirframgreiðsla% **sést** ekki er hægt að bæta honum í gegnum sérsnið.  Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

4. Veldu **Upplýsingar** aðgerðina til að skoða heildarupphæð fyrirframgreiðslu.

    Ef leiðrétta á heildarupphæð fyrirframgreiðslunnar fyrir pöntunina er hægt að breyta innihaldi reitsins **Upphæð fyrirframgreiðslu** á síðunni **Tölfræði sölupöntunar**.  

    Ef reiturinn **Verð ásamt VSK** er valinn er hægt að breyta reitnum **Upphæð fyrirframgreiðslu með VSK**.  

    Ef efni **reitsins upphæð** fyrirframgreiðslu er breytt er upphæðinni dreift í hlutfalli við **allar línur nema línur sem hafa** 0 **í reitnum fyrirframgreiðsla%**.  

5. Til að prenta prufuskýrslu áður en fyrirframgreiðslureikningurinn er bókaður skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Prufuskýrsla fyrirframgreiðslu**.  
6. Til að bóka fyrirframgreiðslureikningurinn skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Bóka fyrirframgreiðslureikning**.  

    Fyrirframgreiðslureikningur er bókaður og prentaður með því að velja aðgerðina **Bóka og prenta fyrirframgr.reikning**.  

Hægt er að gefa út aðra fyrirframgreiðslureikninga fyrir pöntunina. Til að gefa út annan reikning er upphæð fyrirframgreiðslu aukin í einni eða fleiri línum, stilla dagsetningu fylgiskjals ef þörf krefur og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðarinnar.  

> [!NOTE]  
> Ef þú ert í Norður Ameríku, geturðu ekki breytt fyrirframgreiðsluprósentunni eftir að fyrirframgreiðslureikningurinn hefur verið bókaður. Í N-amerísku útgáfu [!INCLUDE[prod_short](includes/prod_short.md)] er komið í veg fyrir þetta, því útreikningur söluskatts yrði annars rangur.  

 Þegar þú ert tilbúinn að bóka afganginn af reikningnum skaltu bóka hann eins og þú bókar hvaða reikning sem er og upphæð fyrirframgreiðslu verður dregin frá upphæðinni sem er á gjalddaga.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Uppfæra stöðu fyrirframgreiddra pantana og reikninga sjálfkrafa

Hægt er að flýta pöntunar-og reikningsvinnslu með því að setja upp vinnsluraðarfærslur sem uppfæra sjálfkrafa stöðu skjalanna. Þegar Greiðslureikningur er greiddur geta færslur í vinnslubiðröð sjálfkrafa breytt stöðu skjals úr **fyrirframgreiddum** reikningi í **Útgefin**. Þegar verkraðarafærslur eru settar upp verður kostnaðareining sem nota á sé **383 UPD. Fyrirframreikningur biðlauna** Sölvi **383 UPD. Fyrirframreikningur biðlauna Innkaupa**. Mælt er með því að færslurnar séu keyrðar oft, til dæmis á hverri mínútu. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
