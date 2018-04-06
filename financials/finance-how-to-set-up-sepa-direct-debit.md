---
title: "Setja upp SEPA-beingreiðslur | Microsoft Docs"
description: "Lærið hvernig á að setja upp SEPA-beingreiðslur í Finance and Operations, Business Edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 28958f1f090e5adad69cb21d30727fcbd6a7fef8
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-direct-debit"></a>Setja upp SEPA-beingreiðslur
Úr glugganum **Innheimta beingreiðslu** er hægt að flytja út leiðbeiningar fyrir rafrænan banka til að innheimta beingreiðslu af bankareikningi viðskiptamanns á þinn bankareikning. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður SEPA-beingreiðslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.  

Til að opna fyrir útflutning af skráasniði bankaskrár sem ekki eru studdar af [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að setja upp gagnaskiptaskilgreiningu með því að nota gagnaskiptaumgjörð. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en hægt er að afgreiða greiðslu viðskiptamanna rafrænt með því að flytja innheimtu beingreiðslu út í SEPA-beingreiðslusnið, verður að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp útflutningssnið bankaskráarinnar með leiðbeiningum til bankans um innheimtu beingreiðslu af bankareikningi viðskiptamanns yfir á eigin bankareikning.  
* Setja upp greiðslumáta viðskiptamanns.  
* Setja upp umboð fyrir beingreiðslu sem endurspeglar samning þinn við viðskiptavininn um söfnun greiðslna á tilteknu samningstímabili.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Setja upp bankareikning fyrir SEPA-beingreiðslu  
1. Í reitinn **Leita** skal færa inn **Bankareikningar** og velja síðan viðkomandi tengi.  
2. Opnið bankareikning sem á að nota fyrir beingreiðslur.  
3. Á flýtiflipanum **Færsla** í reitnum **SEPA – Útflutningssnið beinnar skuldfærslu** skal velja valkostinn fyrir SEPA-beingreiðslur.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Setja upp greiðslumáta viðskiptamanns fyrir SEPA-beingreiðslu  
1. Í reitnum **Leit** skal færa inn **Greiðsluhættir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Setjið upp greiðsluaðferð. Fylla inn í reitina eins\- og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Bein skuldfærsla**|Tilgreina ef greiðsluaðferð er fyrir SEPA innheimtu beingreiðslu.|  
    |**Greiðsluskilmálakóti beinnar skuldfærslu**|Tilgreina greiðsluskilmála eins og EKKI BORGA sem eru birtir á sölureikningum sem eru borgaðir með SEPA-beingreiðslu til að auðkenna fyrir viðskiptamanninn að greiðslan verður innheimt sjálfkrafa. Einnig er hægt að skilja þennan reit eftir auðan.|  

    > [!NOTE]  
    >  Sláið ekki inn gildi í **Mótreikningur nr.** reitinn.  

4. Velja hnappinn **Í lagi** til að loka glugganum **Greiðslumátar**.  
5. Í reitinn **Leita** skal færa inn **Viðskiptamenn** og velja síðan viðkomandi tengi.  
6. Opnið viðskiptamannaspjaldið fyrir viðskiptamanninn sem setja á upp innheimtu fyrir SEPA-beingreiðslur.  
7. Veljið **Kóði greiðslumáta** reitinn og svo kóðann fyrir greiðslumátann sem var tilgreindur í skrefi 3.  
8. Endurtakið skref 6 til 7 fyrir alla viðskiptamenn sem á að setja upp fyrir innheimtu SEPA-beingreiðslu.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Setja upp umboð fyrir beingreiðslu sem stendur fyrir samning viðskiptamannsins  
1. Í reitinn **Leita** skal færa inn **Viðskiptamenn** og velja síðan viðkomandi tengi.  
2. Opnið spjaldið fyrir viðskiptamanninn sem á að setja upp fyrir SEPA-beingreiðslur.  
3. Veldu aðgerðina **Bankareikningar**.  
4. Í glugganum **Bankareikn.listi viðskiptam.** skal velja bankareikning viðskiptamanns sem mun nota beingreiðslu og svo, á flipanum **Heim** í flokknum **Vinnsla** skal velja **Umboð beingreiðslu**.  
5. Í glugganum **SEPA-umboð fyrir beint debet** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

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

6.  Endurtakið skref 1 til 5 fyrir alla viðskiptamenn sem á að setja upp fyrir SEPA-beingreiðslur.  

 Umboðið fyrir beingreiðslur er sjálfkrafa sett inn í **Kenni umboðs fyrir beint debet** reitinn þegar sölureikningur er stofnaður fyrir viðskiptamann sem var valinn í skrefi 2. Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Sjá einnig  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  
[Setja upp gagnaskiptaskilgreiningu](across-how-to-set-up-data-exchange-definitions.md)
[Stofna ítrekaðar sölu- og innkaupalínur](sales-how-work-standard-lines.md)
[Rafræn gagnaskipti](across-data-exchange.md)

