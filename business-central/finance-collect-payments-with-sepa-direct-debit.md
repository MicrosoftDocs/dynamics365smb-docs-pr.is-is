---
title: SEPA-beingreiðsla í Business Central
description: Með samþykki viðskiptamanns er hægt að sækja greiðslur beint inn á bankareikninga viðskiptamanns samkvæmt SEPA-sniðinu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 371, 423, 424, 427, 1208, 1207, 1230
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 681775b78a6d3461a9cd5d6fa1cade1519579903
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7970779"
---
# <a name="collect-payments-with-sepa-direct-debit"></a>Innheimta greiðslur með SEPA-beingreiðslum

Með samþykki viðskiptamanns er hægt að sækja greiðslur beint inn á bankareikninga viðskiptamanns samkvæmt SEPA-sniðinu.  

Setjið fyrst upp útflutningssnið bankaskráarinnar með leiðbeiningum til bankans um beingreiðsluaðgerð. Síðan skal setja upp greiðslumáta viðskiptamanns. Að síðustu skal setja upp umboð fyrir beingreiðslu sem endurspeglar samning þinn við viðskiptavininn um söfnun greiðslna á tilteknu samningstímabili.  

Til að gefa bankanum fyrirmæli um að flytja greiðsluupphæðir af bankareikningi viðskiptamannsins á reikning fyrirtækis þíns, stofnarðu innheimtufærslu beingreiðslu sem inniheldur upplýsingar um bankareikninga, sölureikningana sem um ræðir og umboð fyrir beingreiðslu. Flytjið svo út XML-skrá sem byggir á innheimtufærslu sem er send til úrvinnslu í banka. Bankinn lætur vita af greiðslum sem ekki er hægt að meðhöndla og þá þarf að hafna viðkomandi innheimtufærslur fyrir beingreiðslur.  

Hægt er að setja upp staðlaða sölukóða viðskiptamanns með beingreiðsluaðferð og umboðsupplýsingum. Þá er hægt að nota **Stofna staðlaða viðskiptamannareikninga** runuvinnsluna til að mynda marga sölureikninga með fyrirfram útfylltum upplýsingum um beingreiðslur. Þetta er hægt að gera handvirkt eða sjálfkrafa, samkvæmt gjalddaga greiðslunnar.  

Þegar banki staðfestir að greiðslur séu meðhöndlaðar er hægt að bóka greiðslukvittanir beint úr **Innheimtufærslubeingreiðslur** glugganum eða með því að færa greiðslulínurnar í færslubókina þar sem greiðslukvittanir eru bókaðar, s.s. á síðunni **Inngreiðslubók**. Bjóði sjóðseiginleikar upp á það er einnig hægt að bíða og jafna greiðslurnar úr bankaafstemmingu.  

> [!NOTE]  
> Að safna greiðslum með SEPA-beingreiðslur, verður gengið á sölureikningi að vera EVRA.  

## <a name="setting-up-sepa-direct-debit"></a>Uppsetning SEPA-beingreiðslna

Á síðunni **Innheimta beingreiðslu** er hægt að flytja út leiðbeiningar fyrir rafrænan banka til að innheimta beingreiðslu af bankareikningi viðskiptamanns á þinn bankareikning í samræmi við SEPA-beingreiðslusniðið.

> [!NOTE]
> Almenn útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] styður eingöngu SEPA-beingreiðslusniðið. Útgáfa þíns lands/svæðis kann að styðja önnur snið fyrir rafrænar greiðslur. Sjá undir **Staðbundin virkni** í efnisyfirlitinu.  

Til að opna fyrir útflutning af skráasniði bankaskrár sem ekki eru studdar af [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að setja upp gagnaskiptaskilgreiningu með því að nota gagnaskiptaumgjörð. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en hægt er að afgreiða greiðslu viðskiptamanna rafrænt með því að flytja innheimtu beingreiðslu út í SEPA-beingreiðslusnið, verður að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp útflutningssnið bankaskráarinnar með leiðbeiningum til bankans um innheimtu beingreiðslu af bankareikningi viðskiptamanns yfir á eigin bankareikning.  
* Setja upp greiðslumáta viðskiptamanns.  
* Setja upp umboð fyrir beingreiðslu sem endurspeglar samning þinn við viðskiptavininn um söfnun greiðslna á tilteknu samningstímabili.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Setja upp bankareikning fyrir SEPA-beingreiðslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.  
2. Opnið bankareikning sem á að nota fyrir beingreiðslur.  
3. Á flýtiflipanum **Færsla** í reitnum **SEPA – Útflutningssnið beinnar skuldfærslu** skal velja valkostinn fyrir SEPA-beingreiðslur.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Setja upp greiðslumáta viðskiptamanns fyrir SEPA-beingreiðslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslumátar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Setjið upp greiðsluaðferð. Fylla inn í reitina eins\- og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Bein skuldfærsla**|Tilgreina ef greiðsluaðferð er fyrir SEPA innheimtu beingreiðslu.|  
    |**Greiðsluskilmálakóti beinnar skuldfærslu**|Tilgreina greiðsluskilmála eins og EKKI BORGA sem eru birtir á sölureikningum sem eru borgaðir með SEPA-beingreiðslu til að auðkenna fyrir viðskiptamanninn að greiðslan verður innheimt sjálfkrafa. Einnig er hægt að skilja þennan reit eftir auðan.|  

    > [!NOTE]  
    >  Sláið ekki inn gildi í **Mótreikningur nr.** reitinn.  

4. Veldu hnappinn **Í lagi** til að loka síðunni **Greiðslumátar**.  
5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.  
6. Opnið viðskiptamannaspjaldið fyrir viðskiptamanninn sem setja á upp innheimtu fyrir SEPA-beingreiðslur.  
7. Veljið **Kóði greiðslumáta** reitinn og svo kóðann fyrir greiðslumátann sem var tilgreindur í skrefi 3.  
8. Endurtakið skref 6 til 7 fyrir alla viðskiptamenn sem á að setja upp fyrir innheimtu SEPA-beingreiðslu.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Setja upp umboð fyrir beingreiðslu sem stendur fyrir samning viðskiptamannsins

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.  
2. Opnið spjaldið fyrir viðskiptamanninn sem á að setja upp fyrir SEPA-beingreiðslur.  
3. Veldu aðgerðina **Bankareikningar**.  
4. Á síðunni **Bankareikn.listi viðskiptam.** skal velja bankareikning viðskiptamanns sem mun nota beingreiðslu og svo aðgerðina **Umboð fyrir beingreiðslu**.  
5. Á síðunni **SEPA-umboð fyrir beint debet** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Bankareikn.kóði viðskiptamanns**|Tilgreinir bankareikninginn þaðan sem beingreiðslur eru teknar. Þessi reitur er fylltur út sjálfkrafa.|  
    |**Gildir frá**|Tilgreina dagsetningu þegar beingreiðsla hefst.|  
    |**Gildir til**|Tilgreina dagsetningu þegar beingreiðslu lýkur.|  
    |**Dagsetning undirskriftar**|Tilgreinið dagsetninguna þegar viðskiptamaðurinn skrifaði undir beingreiðslu.|  
    |**Runugerð**|Tilgreina ef samkomulag nær yfir nokkrar (**Ítrekað**) eða eina (**Stakt**)innheimtur beingreiðslu.|  
    |**Áætlaður fjöldi debetfærslna**|Tilgreinir hversu margar innheimtur beingreiðslna þú býst við að búa til. Þessi reitur á aðeins við ef valið var **Ítrekun** í reitnum **Runugerð**.|  
    |**Teljari debetfærslna**|Tilgreinir hversu margar innheimtur beingreiðslna hafa verið gerðar með þessu umboði fyrir beingreiðslur. Þessi reitur er uppfærður sjálfkrafa.|  
    |**Útilokað**|Tilgreina að innheimtu beingreiðslu er ekki hægt að gera með því að nota þetta umboð fyrir beingreiðslu.|  

6. Endurtakið skref 1 til 5 fyrir alla viðskiptamenn sem á að setja upp fyrir SEPA-beingreiðslur.  

 Umboðið fyrir beingreiðslur er sjálfkrafa sett inn í **Kenni umboðs fyrir beint debet** reitinn þegar sölureikningur er stofnaður fyrir viðskiptamann sem var valinn í skrefi 2. Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Stofnun SEPA-innheimtufærslna fyrir beingreiðslur og þær fluttar út í bankaskrá

Til að gefa bankanum fyrirmæli um að flytja greiðsluupphæðir af bankareikningi viðskiptamannsins á reikning fyrirtækis þíns, stofnarðu innheimtu beingreiðslu sem inniheldur upplýsingar um bankareikning viðskiptamanns, sölureikningana sem um ræðir og umboð fyrir beingreiðslu. Úr innheimtufærslu beingreiðslu sem þá myndast er XML-skrá flutt út og hún send eða henni hlaðið upp í netbanka til úrvinnslu. Bankinn lætur vita af greiðslum sem hann getur ekki meðhöndlað og þá þarf að hafna viðkomandi innheimtufærslur fyrir beingreiðslur.  

 > [!NOTE]  
 > Að safna greiðslum með SEPA-beingreiðslur, verður gengið á sölureikningi að vera EVRA.  

### <a name="to-create-a-direct-debit-collection"></a>Til að stofna innheimtu beingreiðslu  

 1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innheimtur með beingreiðslu** og velja síðan viðkomandi tengil.  
 2. Á síðunni **Innheimta beingreiðslu** skaltu velja aðgerðina **Stofna innheimtu beingreiðslu**.  
 3. Á síðunni **Stofna innheimtu beingreiðslu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Frá gjalddaga**|Tilgreina fyrsta gjalddaga greiðslunnar á sölureikningum sem þú vilt stofna innheimtu beingreiðslu fyrir.|  
    |**Til gjalddaga**|Tilgreina síðasta gjalddaga greiðslunnar á sölureikningum sem þú vilt stofna beina innheimtu beingreiðslu fyrir.|  
    |**Gerð viðskiptafélaga**|Tilgreina ef innheimta beingreiðslu er gerð fyrir viðskiptamenn af gerðinni **Fyrirtæki** eða **Einstaklingur**.|  
    |**Aðeins viðskiptamenn með gilt umboð**|Tilgreina ef innheimta beingreiðslu er stofnuð fyrir viðskiptamenn sem hafa gilt umboð fyrir beingreiðslu. **Athugið:** Beingreiðsla er stofnuð þó svo reiturinn **Kenni umboðs með beinni skuldfærslu** sé ekki útfylltur á sölureikningnum.|  
    |**Aðeins reikningar með gilt umboð**|Tilgreina ef innheimta beingreiðslu er stofnuð eingöngu fyrir sölureikninga ef gilt umboð fyrir beingreiðslu er valið í reitnum **Kenni umboðs með beinni skuldfærslu** reitinn á sölureikningnum.|  
    |**Númer bankareiknings**|Tilgreina hvaða bankareikningar fyrirtækis þíns innheimt greiðsla verður flutt til úr bankareikningi viðskiptamanns.|  
    |**Heiti Bankareiknings**|Tilgreinir nafn bankareiknings sem þú velur í **bankareikningsnúmer** reitnum. Þessi reitur er fylltur út sjálfkrafa.|  

 4. Velja hnappinn **Í lagi**.  

Innheimtu beingreiðslu er bætt við síðuna **Innheimta beingreiðslu** og ein eða fleiri innheimtufærsla fyrir beingreiðslu er stofnuð.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Flytja út innheimtufærslu beingreiðslu í bankaskrá

 1. Á síðunni **Innheimta beingreiðslu** skaltu velja aðgerðina **Innheimtufærslur með beinni skuldfærslu**.  
 2. Á síðunni **Innheimtufærslur með beinni skuldfærslu** skal velja færsluna sem á að flytja út og svo aðgerðina **Stofna skrá með beinni skuldfærslu**.  
 3. Vistar útflutningsskrá á staðsetningu þaðan sem hún er send eða henni hlaðið upp í netbanka til úrvinnslu.  

      Á síðunni **Innheimtafærsla fyrir beingreiðslu** breytist reiturinn **Staða innheimtu beingreiðslu** í Skrá stofnuð. Á síðunni **SEPA tilskipun beingreiðslu** er reiturinn **Afgreiðsluborð** uppfærður um einn.  

 Ef ekki er hægt að meðhöndla útfluttu skrána, t.d. vegna þess að viðskiptavinurinn er gjaldþrota, er hægt að hafna innheimtufærslunni fyrir beingreiðslu. Ef útflutta skráin er meðhöndluð af bankanum er gjaldföllnum greiðslum sölureikninganna sjálfkrafa safnað af viðkomandi viðskiptavinum. Í því tilfelli er hægt að loka innheimtunni.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Hafna innheimtufærslu beingreiðslu  

* Á síðunni **Innheimtufærslur með beinni skuldfærslu** skal velja færsluna sem ekki var meðhöndluð og svo aðgerðina **Hafna færslu**.  

    Gildið í reitnum **Staða** á síðunni **Innheimtufærsla fyrir beingreiðslu** er breytt í **Hafnað**.  

### <a name="to-close-a-direct-debit-collection"></a>Loka innheimtu beingreiðslu

* Á síðunni **Innheimtufærslur með beinni skuldfærslu** skal velja færsluna sem var meðhöndluð og svo aðgerðina **Loka innheimtu**.  

    Tengd innheimta beingreiðslu er lokuð.  

 Þá er hægt að bóka greiðslukvittanir fyrir viðkomandi sölureikninga. Hægt er að gera þetta á sama hátt og greiðslukvittanir eru vanalega bókaðar, s.s. á síðunni **Skráning greiðslna**, en einnig er hægt að bóka tengdu greiðslukvittunina beint af síðunni **Innheimtufærslur fyrir beingreiðslu**. Nánari upplýsingar má nálgast á [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)

## <a name="posting-sepa-direct-debit-payment-receipts"></a>Bókun SEPA-greiðslukvittana beingreiðslna

Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna. Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Hægt að bóka greiðslukvittunina beint af síðunni **Innheimta fyrir beingreiðslur** eða af síðunni **Innheimtufærslur fyrir beingreiðslur**. Einnig er hægt að færa verkið á annan notanda með því að undirbúa tengdar færslubókarlínur.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Bóka greiðslukvittun beingreiðslu af síðunni Innheimta beingreiðslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innheimtur með beingreiðslu** og velja síðan viðkomandi tengil.  
2. Veljið línu fyrir innheimtu beingreiðslu sem hefur verið flutt út í bankaskrá og meðhöndluð af bankanum.
3. Valið er **bóka greiðslukvittanir** aðgerð.  
4. Á síðunni **bóka innheimtu beingreiðslu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Númer innheimtu með beinni skuldfærslu**|Tilgreina innheimtu beingreiðslu sem á að bóka greiðslukvittun fyrir.|  
    |**Sniðmát almennrar færslubókar**|Tilgreina hvaða sniðmát almennrar færslubókar á að nota til að bóka greiðslukvittun, svo sem sniðmát fyrir inngreiðslur.|  
    |**Heiti færslubókarkeyrslu**|Tilgreina hvaða færslubókarkeyrslu á að nota til að bóka greiðslukvittun.|  
    |**Stofna aðeins færslubók**|Veljið þennan gátreit ef ekki á að bóka greiðslukvittunina þegar **Í lagi** hnappurinn er valinn. Greiðslukvittunin verður undirbúin í tilgreindri færslubók og mun ekki vera bókuð fyrr en einhver bókar færslubókarlínurnar sem um ræðir.|  

5. Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig

[Stjórnun skulda](receivables-manage-receivables.md)  
[Þjónustukerfi](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]