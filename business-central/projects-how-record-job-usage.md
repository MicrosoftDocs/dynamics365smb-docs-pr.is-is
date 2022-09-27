---
title: Skrá neyslu eða notkun á tilföngum og hlutum verks
description: Lýsir því hvernig á að skrá neyslu eða notkun á vöru eða forða í verkum til að greiða fyrir verkefnastjórnun.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.search.form: 89, 92, 201, 1007, 1014
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c948845c535474ccd5fb8c3d6e031e5467c9de2f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532080"
---
# <a name="record-consumption-or-usage-for-jobs"></a>Skrá neyslu eða notkun fyrir verk

Á síðunni **Áætlunarlínur verks** er hægt að fara yfir og skrá notkun mismunandi hluta verks, sem uppfærist sjálfkrafa þegar breytt er og við flutning upplýsinga milli verka og verkbóka eða verkreikninga. Þetta krefst þess að verk hafi verið sett upp svo kveikt sé á **Beita notkunartengli**. Frekari upplýsingar eru í [Setja upp verk](projects-how-setup-jobs.md).  

Til dæmis fyrir áætlunarlínurnar af tegundinni **Áætlun** er hægt að setja inn magn forða og tilgreina hvaða magn á að flytja í verkbókina. Ef gerð áætlunarlínurnar er **Reikningshæft** er hægt að færa inn magn forða og tilgreina hvaða magn á að flytja á reikning. Frekari upplýsingar um reikningsfærslu á viðskiptavininn er að finna á [Reikningsfærsla verka](projects-how-invoice-jobs.md). Með því að bera saman upphaflegt magn, eftirstöðvar magns eða bókað magn er fljótlegt að fara yfir notkunarupplýsingarnar. Upplýsingar um hvernig skal áætla virði við áætlun er að finna í [Vinna með verkáætlanir](projects-how-manage-budgets.md).  

Eftirfarandi ferli lýsa því hvernig á að skrá raunverulegt (áætlað) magn og kostnað með verkbók. Einnig er hægt að nota innkaupaskjöl til að skrá innkaup fyrir verk. Sjá [Stjórna verkbirgðum](projects-how-manage-project-supplies.md) fyrir frekari upplýsingar.

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Til að skrá notkun fyrir verkáætlunarlínu af gerðinni Áætlun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Verkáætlunarlínur**.
3. Veljið verkáætlunarlínu af gerðinni **Áætlun** eða **Bæði fjárhagsáætlun og reikningshæft** sem á að skrá notkun fyrir.  

    > [!NOTE]
    > Þú getur einnig skráð notkun fyrir verkáætlunarlínu af gerðinni **Reikningshæf**. Þessar línur eru yfirleitt notaðar til að búa til reikninga, en einnig er hægt að flytja þær í fæslubók. Frekari upplýsingar eru í [Reikningsfærsla verka](projects-how-invoice-jobs.md) <!--However, when you do that, a job planning line of type **Budget** is created to match the billable line. For more information, see [Manage Job Budgets](projects-how-manage-budgets.md).-->

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

## <a name="to-create-job-journal-lines-manually"></a>Til að búa til verkbókarlínur handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Í reitnum **Heiti keyrslu** skal velja viðeigandi verkbókarkeyrslu.  
3. Sláið inn skjalanúmer, verknúmer, verkhlutanúmer, tegund og magn tegundarinnar sem verið er að nota í nýja línu.  
4. Þegar verkbókarlínurnar eru tilbúnar skal velja aðgerðina **Bóka**.  

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Til að skoða áætlanir um verknotkun og bóka uppfærslur

Skoða má verknotkun allt að lokum verkefnis í einu skrefi. Til þess er notuð keyrslan **Verk - Reikna eftirstandandi notkun** fyrir alla verkhluta allt að og með lokum verks.  

Á þennan hátt má rekja og bera saman upprunalega áætlun við raunverulegar niðurstöður og gera breytingar eða bæta við færslum eftir þörfum. Taka má dæmi af notanda sem hefur áætlað að verk taki 10 klukkustundir en það hefur þegar tekið 15 klukkustundir. Hann getur bætt klukkustundunum fimm við færslubókarlínu sem fyrir er eða búið til nýja færslubókarlínu til að skilgreina þessa fimm tíma sem yfirvinnu, sem er önnur tegund vinnu. Raunkostnaður og verð eru reiknuð út, sem svo er hægt að bóka í færslubókina.  

> [!NOTE]  
>   Birgðafærslur stofna færslur í birgðahöfuðbók og minnka birgðamagn. Keyrslan **Bóka birgðabreytingar** færir kostnaðinn úr birgðum í fjárhag. Forðafærslur stofna forðafærslur.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Reikna eftirstandandi notkun**.  
3. Á síðunni **Verk - Reikna eftirstandandi notkun** skal slá inn númer skjalsins og bókunardagsetninguna sem færa skal í bókina og velja svo hnappinn **Í lagi**.  
4. Uppfærið bókina með þeim breytingum sem kann að vera þörf á.  
5. Veljið **Bókun**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Stofna birgðir og vöruhúsatínsluskjöl fyrir vinnslu

Ef stofna á tínsluskjöl birgða og vöruhúss fyrir vinnslur verður kerfisstjórinn að gera **uppfærsluaðgerðina virka: Virkja birgðatínslu og vöruhúsatiltekt frá vinnslum** á **síðunni Feature Management**.

Aðgerðin bætir **birgðatínslu** og **Stofna vöruhúsatínsluaðgerðir** á **vinnsluspjaldið**. Til að stofna eða skrá tínsluskjal eru notaðar **frágangs-/tínslulínur/hreyfingalínur** eða **skráðar aðgerðir tínslulínur**. Nánari upplýsingar um tínslur er að finna [í tínsluvörum](warehouse-pick-items.md)

Hægt er að nota aðgerðirnar undir eftirfarandi skilyrðum:
* **Staða** vinnslunnar er **opin**.
* **Línugerð** verkáætlunarlínunnar er **áætlun** eða **bæði áætlun og innheimt**.
* **Gerð** verkáætlanalínuna er **Vara**.
* **Krefjast tínslu** er virkjað fyrir tengda staðsetningu.
* **Beinn tínsla og frágangur** er óvirkur.

> [!NOTE] 
> Þrátt fyrir að stillingin sé kölluð **krefjast tínslu** er enn hægt að bóka notkun beint úr verkbókarlínunni fyrir birgðageymsluna. Ef birgðageymslan er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu er síðan Birgðatínsla **notuð** til að skipuleggja og prenta tiltektarupplýsingar. Einnig er hægt að nota síðuna til að færa inn og bóka tínsluna sem aftur bókar notkun varanna. 
> 
> Ef birgðageymslan er sett upp þannig að krafist sé bæði tínslu-og afhendingarvinnslu sem valin var bæði **krefjast tínslu** og **þarfnast afhendingar** á **síðunni Birgðageymsluspjald** Notið **síðuna Vöruhúsatínsla** til að sjá um tínsluna. Vöruhúsatínslur eru svipaðar og Birgðatínslur. Munurinn er sá að frekar en að bóka tiltektarupplýsingarnar sem tínslan er skráð í. Þessi skráning bókar ekki notkun, það gerir bara þær vörur sem eru tiltækar til bókunar. Sem vöruhúsastjóri er hægt að nota tínsluvinnublað til að skipuleggja tínsluupplýsingar áður en leiðbeiningar fyrir einstakar vöruhúsatínslur eru stofnaðar


## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Til að fara yfir áætlunarlínur verkfærslu

Þegar verkbókarlínur hafa verið bókaðar er hægt að sjá þær áætlunarlínur sem tengjast þeim verkbókarfærslum sem hafa verið bókaðar.

> [!NOTE]  
> Þetta krefst þess að gátreiturinn **Nota notkunartengil** sé valinn fyrir verkið. Frekari upplýsingar eru í [Setja upp verk](projects-how-setup-jobs.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Færslur**.  
3. Á síðunni **Verkfærslur** er aðgerðin **Sýna áætlunarlínur verks** valin.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/post-job-usage-sales/)

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
