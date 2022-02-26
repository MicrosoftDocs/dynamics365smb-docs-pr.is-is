---
title: Steypa saman gögnum frá mörgum fyrirtækjum
description: Í þessu efnisatriði er útskýrt hvernig hægt er að sameina fjárhagsfærslur tveggja eða fleiri aðskildra fyrirtækja (dótturfyrirtækja) í samstæðufyrirtæki.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1fd6dbc45dfbbdaa571161a8930d6b23471cac23
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7970701"
---
# <a name="consolidating-financial-data-from-multiple-companies"></a>Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Önnur nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem þarf að tilkynna um í móðurfyrirtækjum. Í báðum tilvikum nota endurskoðendurnir innbyggð verkfæri til að sameina fjárhagsgögn.  

Hægt er að sameina fjárhagsfærslur tveggja eða fleiri fyrirtækja dótturfyrirtæki í samstæðufyrirtæki. Hvert fyrirtæki í samstæðufyrirtæki nefnist fyrirtækiseining. Sameinaða fyrirtækið nefnist samstæðufyrirtæki.  

Hægt er að flytja inn gögn í samstæðufyrirtækið úr öðrum fyrirtækjum í sama [!INCLUDE [prod_short](includes/prod_short.md)]-leigjandanum, úr leigjendum, eða úr skrám.  

Ef fjárhagsskýrslur fyrirtækiseiningarinnar eru í öðrum gjaldmiðli en reikningar samsteypufyrirtækisins þarf að setja upp gengi fyrir samstæðuna.  

Hægt er að steypa saman:  

* Tengd fyrirtæki sem hafa ólíka bókhaldslykla.  
* Fyrirtæki sem nota ólík fjárhagsár og gjaldmiðla.  
* Annað hvort öll upphæðin eða tiltekin prósenta af fjárhagsupplýsingum fyrirtækis
* Nota mismunandi gengi gjaldmiðla á einstökum fjárhagsreikningum
* Fyrirtæki í öðrum bókhalds- og viðskiptastjórnunarforritum

Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Bókhaldslykillinn er óháður bókhaldslyklum í hinum fyrirtækiseiningunum og bókhaldslyklar einstakra fyrirtækja geta verið mismunandi. Settur er upp listi yfir fyrirtæki sem á að steypa saman, votta bókhaldsgögn fyrir samsteypu, flytja inn úr skrám eða gagnagrunnum og búa til samsteypuskýrslur. Frekari upplýsingar er að finna í [Setja upp fyrirtækjasamstæðu](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Að steypa saman fjárhagsgögnum getur einkum haft þýðingu í tengslum við ferla innan samstæða. Nánari upplýsingar er að finna í [Stjórnun samstæðufærslna](intercompany-manage.md).

## <a name="trial-balance"></a>Prófjöfnuður

Ef þú ert með fleiri en eitt fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)], getur skýrslan **Sameinaður prófjöfnuður** gefið þér yfirsýn yfir fjárhagslega stöðu fyrirtækja þinna í heild.  

Skýrslan sameinar fjárhagsfærslur frá öllum fyrirtækjum þínum í nýtt fyrirtæki sem þú stofnar til að hýsa sameinuðu gögnin. Venjulega er vísað til þessa fyrirtækis sem „samstæðufyrirtækisins“. Samstæðufyrirtækið er aðeins geymsla fyrir sameinuðu gögnin og inniber engin lifandi viðskiptagögn. Fyrirtækin sem þú setur inn í samstæðufyrirtækið verða að **Viðskiptaeiningum** í skýrslunni. Frekari upplýsingar er að finna í [Setja upp fyrirtækjasamstæðu](finance-consolidated-company-reporting-setup.md).  

## <a name="consolidate-data"></a>Gögnum steypt saman

Ferlið við að flytja tölur úr fyrirtækiseiningum til samsteypufyrirtækisins er hin raunverulega *sameining*. Áður en það er gert er ágætt að athuga hvort munur sé á grunnupplýsingum í fyrirtækiseiningunni og samstæðufyrirtækinu. Nota má tvær skýrslur til að prófa gagnagrunn og skrá.

### <a name="to-test-the-data-before-you-consolidate"></a>Gagnaprófun fyrir samsteypu

Þú getur framkvæmt gagnaprófun áður en þú sendir gögnin í samstæðufyrirtækið. [!INCLUDE[prod_short](includes/prod_short.md)] athugar muninn á upplýsingunum í fyrirtækiseiningunum og samstæðufyrirtækinu. Til dæmis hvort munur er á reikningsnúmerum og víddarkóðum. Áður en hægt er að keyra skýrsluna verður að leiðrétta villur. Þú getur framkvæmt prófanir á gagnagrunninum, eða skránni, ef þú ert að flytja inn gögn frá XML skrá.  

1. Samsteypufyrirtækið er opnað.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Gert er eitt af eftirfarandi:  

    * Til að framkvæma prófun á skrá, skal velja **Prófa skrá** aðgerðina, slá inn nafn skrárinnar sem á að prófa og velja síðan **Prenta**.  
    * Til að framkvæma prófun á gagnagrunni, skal velja **Prófa gagngrunn**.  

### <a name="run-the-consolidation"></a>Keyra samstæðu

Þegar gögn hafa verið prófuð er hægt að senda þau í samstæðufyrirtækið.  

1. Skráðu þig inn samstæðufyrirtækið.  
2. Í **Hlutverkamiðstöð Endurskoðandi** skal velja **Keyra samstæðu** aðgerðina.  
3. Fylltu út nauðsynlega reiti.  
4. Í síuhlutanum skal stilla síu fyrir viðeigandi fyrirtækiseiningu eða fyrirtækisheiti.  
5. Einnig má tímasetja skýrsluna til að keyra á hentugum tíma.  

## <a name="eliminate-repeated-transactions"></a>Taka út endurteknar færslur

Þegar búið er að steypa saman öllum fyrirtækjum þarf að finna allar færslur sem eru skráðar oftar en einu sinni í öllum fyrirtækjum og síðan bóka losunarfærslur til að fjarlægja þær.

Að vinna með samstæðulosanir er handvirkt ferli.  

Að taka út endurteknar færslur:

1. Finndu færslur sem hugsanlega þarf að leiðrétta og sláðu inn almennar færslubókarlínur til að fjarlægja þær.
2. Keyrðu skýrsluna **Samstæðuútilokanir fjárhags** til að hjálpa þér við að meta áhrif almennu færslubókarlínanna fyrir bókun.
3. Bókaðu leiðréttar færslur.

Skýrslan **Samstæðuútilokanir fjárhags** birtir bráðabirgða prófjöfnuð þar sem hægt er að herma eftir afleiðingum þess að útiloka færslur með því að bera saman færslur í samsteypufyrirtækinu við útilokanir sem hafa verið færðar inn í færslubókina.

Áður en unnt er að taka fyrirtækiseiningu með í skýrslu, verður að setja hana upp á síðunni **Fyrirtækiseiningar** og velja þarf reitinn **Steypa saman**.

Sérhver reikningur birtist einn sér í línu, (í framhaldi af uppbyggingu bókhaldslykils). Reikningur birtist ekki ef allar upphæðir standa á núlli. Eftirfarandi upplýsingar koma fram um hvern reikning:

* Reikningsnúmer
* Nafn lykils.
* Hafi einn eða fleiri kóðar fyrirtækiseiningar verið valdir í reitnum **Kóði fyrirtækiseiningar** á beiðnisíðunni, birtist samtala samsteypufyrirtækis, að undanskildum völdum fyrirtækiseiningum og útilokunum. Hafi reiturinn **Kóði fyrirtækjaeiningar** ekki verið útfylltur birtist samtala samsteypufyrirtækis, að útilokunum undanskildum.
* Hafi kóði fyrirtækiseiningar verið valinn í reitnum **Kóði fyrirtækiseiningar** á beiðnisíðunni, birtist samtala fyrir innfluttar færslur úr fyrirtækiseiningunni. Hafi reiturinn **Kóði fyrirtækjaeiningar** ekki verið útfylltur birtist samtala bókaðra útilokana í bókhaldi samsteypufyrirtækis.
* Samtala samsteypufyrirtækis, að öllum fyrirtækjaeiningum og bókuðum útilokunum meðtöldum.
* Útilokanir sem á að framkvæma í samsteypufyrirtækinu, þ.e. færslurnar í almennu færslubókinni sem er valin á beiðnisíðunni.
* Bókunartexti afritaður eftir færslubók.
* Samtala samsteypufyrirtækis eftir útilokanir, ef þær eru bókaðar.

## <a name="export-and-import-consolidated-data-between-databases"></a>Að flytja út og flytja inn sameinuð gögn milli gagnagrunna

Ef gögn fyrirtækiseiningar eru í öðrum gagnagrunni þarf að flytja gögnin út í skrá áður en hægt er að hafa þau með í samstæðunni. Flytja þarf hvert fyrirtæki fyrir sig. Í þessum tilgangi skal nota runuvinnsluna **Útflutningur samstæðu**.  

> [!TIP]
> Notið sama ferlið til að flytja út sameinuð gögn sem þarf að senda til Dynamics 365 Finance, svo sem ef núverandi fyrirtækiseining er dótturfyrirtæki og móðurfyrirtækið notar Dynamics 365 Finance.

Þegar búið er að keyra runuvinnsluna, eru allar færslur í fjárhagsreikninga unnar. Samtala er fengin og flutt út úr efni færslna í reitunum **Upphæð** í sérhverri samsetningu valinnar víddar og dagsetningar. Þá er unnið úr næstu samsetningu valinnar víddar og dagsetningar með sama reikningsnúmeri og síðan úr samsetningu næsta reikningsnúmers og svo framvegis.  

Útfluttar færslur innihalda eftirfarandi reiti: **Reikningur nr.**, **Bókunardags.** og **Upphæð**. Ef upplýsingar um víddir voru líka fluttar út, eru víddarkóðar og víddargildi þar á meðal.  

1. Ef samtala reitanna **Upphæð** er debet er reikningsnúmerið sem sett er upp í reitnum **Samstæðu-debetreikn.** í fyrirtækiseiningunni flutt út í línuna fyrir hverja útflutta línu. Ef samtalan er kredit er samsvarandi númer í reitnum **Samstæðu-kreditreikn.** flutt út í línuna.  
2. Sú dagsetning sem er notuð fyrir útfluttar línu er annaðhvort lokadagsetning tímabils eða sú dagsetning þegar útreikningur fer fram.  
3. Víddargildið sem flutt er út fyrir færsluna verður víddargildi samsteypufyrirtækisins sem sett er upp í reitnum **Kóti samstæðu** fyrir það víddargildi. Ef ekkert víddargildi samsteypufyrirtækis hefur verið fært inn í reitinn **Sameinaður kóti** fyrir þetta víddargildi er víddargildið sjálft flutt út í línuna.  
4. Auk þess innihalda XML-skrárnar gengi gjaldmiðils innan samsteyputímabilsins. Þessi gengi eru innifalin í aðskildum hluta í upphafi skrárinnar.  

## <a name="see-also"></a>Sjá einnig

[Setja upp sameiningu fyrirtækis](finance-consolidated-company-reporting-setup.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]