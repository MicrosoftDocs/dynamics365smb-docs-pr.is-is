---
title: Setja upp greiðsluaðferðir
description: 'Þú notar greiðsluaðferðir, til dæmis tékka, bankamillifærslu, reiðufé eða PayPal, til að skilgreina hvernig sölu- og innkaupareikningar eru greiddir.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.search.form: '427,'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Setja upp greiðsluaðferðir

Greiðsluhættir skilgreina hvernig þú vilt að viðskiptavinir greiði þér og hvernig þú vilt greiða lánardrottnum þínum. Greiðslumátinn getur verið breytilegur fyrir hvern viðskiptavin eða lánardrottin. Dæmi um dæmigerða greiðsluhætti eru **banki**, **reiðufé**, **ávísun** eða **reikningur**.

Þú getur úthlutað greiðslumáta til viðskiptavina og lánardrottna þannig að sama aðferðin sé alltaf notuð á sölu- og innkaupskjölunum sem þú býrð til fyrir þá. Hægt er að breyta greiðslumátanum í sölu- og innkaupaskjalinu ef þörf krefur. Til dæmis, ef þú vilt greiða ákveðinn innkaupareikning í reiðufé frekar en með ávísun. Sjálfgefinn greiðsluháttur sem úthlutað er á lánardrottin breytist ekki.

Sömu greiðsluaðferðir eru notaðar fyrir sölu- og innkaupaskjöl. Greiðsluháttur í reiðufé _er_ til dæmis notaður til að inna af hendi greiðslur og til að taka á móti þeim. [!INCLUDE[prod_short](includes/prod_short.md)] veit að þegar búinn er til sölureikningur er búist við því að fá greiðslu og öfugt við innkaupareikninga.

Kreditreikningar vegna skila eru þó undantekningar vegna þess að peningar flæða í gagnstæða átt, frá þér til viðskiptavina og frá lánardrottni til þín. Því er sjálfgefinni greiðsluaðferð ekki úthlutað á kreditreikninga. Það er hins vegar til ræktun. Hægt er að tilgreina greiðsluskilmála viðskiptamanns eða lánardrottins. Þó að reiturinn **Reikn. staðgr.afsl. á kreditreikningum** sé ekki ætlaður fyrir þessa vinnu er sjálfgefnum **greiðsluaðferðum** bætt við þegar kreditreikningur er stofnaður. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## Greiðsluaðferðir settar upp

[!INCLUDE[prod_short](includes/prod_short.md)] veitir nokkrar greiðsluaðferðir sem fyrirtæki nota oft. Þó er hægt að bæta við eins mörgum og þörf krefur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslumátar** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Þú getur einnig bætt við greiðsluskilmálum við greiðslumátann þinn. Nánari upplýsingar um það eru í [Setja upp greiðsluskilmála](finance-payment-terms.md).  

## Viðskiptavinum eða lánardrottnum úthlutaður greiðslumáti

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** eða **Lánardrottinn** og velja síðan viðkomandi tengil.
2. Í reitnum **Kóði greiðslumáta** skal velja greiðslumátann sem á að nota að sjálfgefnu viðskiptavin eða lánardrottin.

## Sjá einnig .

[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Setja upp greiðsluskilmála](finance-payment-terms.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
