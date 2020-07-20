---
title: Skrá reikningshæfa og áætlaða notkun verkforða| Microsoft Docs
description: Lýsir því hvernig á að skrá neyslu eða notkun á vöru eða forða í verkum til að greiða fyrir verkefnastjórnun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/26/2020
ms.author: sgroespe
ms.openlocfilehash: 2e861c3e403ebafb2d9d1c2a4bcf0679a0a715d1
ms.sourcegitcommit: 836b232d0149f9732884c9f44d53928725a8759d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/26/2020
ms.locfileid: "3506232"
---
# <a name="record-usage-for-jobs"></a>Skrá notkun vegna verka

Á síðunni **Áætlunarlínur verks** er hægt að fara yfir og skrá notkun mismunandi hluta verks, sem uppfærist sjálfkrafa þegar breytt er og við flutning upplýsinga milli verka og verkbóka eða verkreikninga. Þetta krefst þess að verk hafi verið sett upp svo kveikt sé á **Nota notkunartengil sjálfgefið**. Frekari upplýsingar eru í [Setja upp verk](projects-how-setup-jobs.md).  

Til dæmis fyrir áætlunarlínurnar af tegundinni **Áætlun** er hægt að setja inn magn forða og tilgreina hvaða magn á að flytja í verkbókina. Ef gerð áætlunarlínurnar er **Reikningshæft** er hægt að færa inn magn forða og tilgreina hvaða magn á að flytja á reikning. Með því að bera saman magn sem hefur verið flutt í færslubókina eða reikning með eftirstöðvarmagni, er fljótlegt að fara yfir notkunarupplýsingarnar.

Eftirfarandi leiðbeiningar lýsa því hvernig á að skrá raunverulegt (reikningshæft) eða áætlað verð og kostnað við verk. Upplýsingar um hvernig skal áætla virði við áætlun er að finna í [Vinna með verkáætlanir](projects-how-manage-budgets.md).  

> [!TIP]
> Í eftirfarandi hlutum er notast við hugtakið *skráð notkun* til að ná yfir tvö verk: skrá verkáætlunarlínur og senda viðskiptavini reikning í samræmi við það.

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Til að skrá notkun fyrir verkáætlunarlínu af gerðinni Áætlun

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Verkáætlunarlínur**.
3. Veljið verkáætlunarlínu af gerðinni **Áætlun** eða **Bæði fjárhagsáætlun og reikningshæft** sem á að skrá notkun fyrir.
4. Í reitinn **Magn til flutnings í færslubók** skal skrá fjöldann sem á að flytja. Sjálfgefna gildið er sama magn og það sem er í reitnum **Magn**.

    Reiturinn **Eftirstöðvar (magn)** sýnir það magn sem eftir er til að ljúka verkinu og flytja í færslubókina.  
5. Velja skal aðgerðina **Stofna verkbókarlínur**.

    > [!TIP]
    > Ef ætlunin er að bæta við fleiri verkáætlunarlínum fyrir þetta verk skal bíða með þetta skref þar til öllum verkáætlunarlínum hefur verið bætt við.
6. Á síðunni **Verk - Flytja verkáætlunarlínu** skal fylla reiti út eftir þörfum og velja síðan hnappinn **Í lagi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velja skal aðgerðina **Opna verkbók**.  
8. Á síðunni **Verkbók** skal velja viðeigandi línu og svo aðgerðina **Bóka**.
9. Á síðunni **Verkáætlunarlínur** skal fara yfir skráða notkun með því að athuga reitina **Magn**, **Eftirstöðvar (magn)** og **Magn til flutnings í færslubók**.  
10. Endurtakið skref 3 til 8 til að skrá frekari notkun.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Til að skrá notkun fyrir verkáætlunarlínu af gerðinni Reikningshæft

Í næsta verkefni skal einnig skrá notkun, en fyrir verkáætlunarlínu af gerðinni **Reikningshæft**. Í þessu tilfelli er notkunin yfirleitt reikningsfærð, en einnig er hægt að flytja hana í bók. Þegar það er gert er stofnuð verkáætlunarlína af gerðinni **Áætlun** sem samsvarar reikningshæfu línunni. Frekari upplýsingar eru í [Umsjón fjárhagsáætlana fyrir eignir](projects-how-manage-budgets.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.
2. Veljið viðeigandi verk og veljið svo aðgerðina **Verkáætlunarlínur**.  
3. Veljið verkáætlunarlínu af gerðinni **Reikningshæft** sem á að skrá notkun fyrir.
4. Í reitinn **Magn til flutnings á reikning** skal skrá fjöldann sem á að flytja. Sjálfgefna gildið er sama magn og það sem er í reitnum **Magn**.

    Reiturinn **Magn á reikning** sýnir það magn sem eftir er til að ljúka verkinu og reikningsfæra.  
5. Veljið aðgerðina **Stofna sölureikning**.

    > [!TIP]
    > Ef ætlunin er að bæta við fleiri verkáætlunarlínum fyrir þetta verk skal bíða með þetta skref þar til öllum verkáætlunarlínum hefur verið bætt við.
6. Á síðunni **Verk - Flytja í sölureikning** skal fylla reiti út eftir þörfum og velja síðan hnappinn **Í lagi**.
7. Farið yfir skráða notkun með því að skoða reitina **Magn**, **Magn á reikning** og **Magn til flutnings á reikning** og einnig reitinn **Reikningsfært magn** ef sölureikningurinn er bókaður.
8. Endurtakið skref 3 til 7 til að skrá frekari notkun.  
9. Til að fara yfir tengdan bókaðan sölureikning skal velja aðgerðina **Sölureikningar/kreditreikningar**.  

    Ef fleiri en einn reikningur eru til fyrir þetta verk verður að velja viðeigandi reikning á síðunni **Verkreikningar** og síðan velja **Opna sölureikning/kreditreikning** aðgerðina.  

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Til að stofna verkbókarlínur úr áætlunarlínum verks

Þegar notandi er tilbúinn að bóka fjárhagslegar upplýsingar fyrir verk, þarf að stofna verkbókarlínur sem hægt er að bóka.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið viðeigandi opið verk og veljið svo aðgerðina **Verkáætlunarlínur**.  
3. Á síðunni **Verkáætlunarlínur** skal slá inn magnið sem flytja skal í verkbók í reitinn **Magn til flutnings í færslubók** í viðeigandi verkáætlunarlínu.  
4. Velja skal aðgerðina **Stofna verkbókarlínur**.
5. Á síðunni **Verkflutningar í áætlunarlínur** skal fylla út reiti eins og þörf krefur.  
6. Velja hnappinn **Í lagi**. Verkbókarlínur eru stofnaðar.
7. Til að staðfesta flutninginn skal opna viðeigandi verkbókarkeyrslu og athuga færslurnar.  
8. Þegar verkbókarlínurnar eru tilbúnar skal velja aðgerðina **Bóka**.  

## <a name="to-create-job-journal-lines-manually"></a>Til að búa til verkbókarlínur handvirkt

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkbækur** og veldu síðan tengda tengilinn.  
2. Í reitnum **Heiti keyrslu** skal velja viðeigandi verkbókarkeyrslu.  
3. Sláið inn skjalanúmer, verknúmer, verkhlutanúmer, tegund og magn tegundarinnar sem verið er að nota í nýja línu.  
4. Þegar verkbókarlínurnar eru tilbúnar skal velja aðgerðina **Bóka**.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Til að fara yfir áætlunarlínur verkfærslu

Þegar verkbókarlínur hafa verið bókaðar er hægt að sjá þær áætlunarlínur sem tengjast þeim verkbókarfærslum sem hafa verið bókaðar.

> [!NOTE]  
> Þetta krefst þess að gátreiturinn **Nota notkunartengil sjálfgefið** sé valinn fyrir verkið eða sé sjálfgefin stilling fyrir öll verk í fyrirtækinu. Frekari upplýsingar eru í [Setja upp verk](projects-how-setup-jobs.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkbækur** og veldu síðan tengda tengilinn.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Færslur**.  
3. Á síðunni **Verkfærslur** er aðgerðin **Sýna áætlunarlínur verks** valin.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
