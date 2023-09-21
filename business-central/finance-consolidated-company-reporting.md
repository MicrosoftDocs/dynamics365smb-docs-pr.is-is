---
title: Steypa saman gögnum frá mörgum fyrirtækjum
description: Í greininni er útskýrt hvernig hægt er að sameina fjárhagsfærslur tveggja eða fleiri aðskilins félaga (dótturfyrirtækja) í samstæðufyrirtæki.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Önnur nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem þarf að tilkynna um í móðurfyrirtækjum. Í báðum tilvikum nota endurskoðendurnir innbyggð verkfæri til að sameina fjárhagsgögn.  

Hægt er að sameina fjárhagsfærslur tveggja eða fleiri fyrirtækja dótturfyrirtæki í samstæðufyrirtæki. Hvert fyrirtæki í samstæðufyrirtæki nefnist fyrirtækiseining. Sameinaða fyrirtækið nefnist samstæðufyrirtæki.  

Hægt er að flytja gögn inn í samstæðureikningsskil frá öðrum félögum í sama  [!INCLUDE [prod_short](includes/prod_short.md)]  leigjanda frá leigjendum eða úr skrám.  

Ef Fjárhagsleg Yfirlit fyrirtækiseiningar eru í öðrum gjaldmiðli en þeim gjaldmiðli sem notaður er í samstæðufyrirtækinu verður að setja upp gengi fyrir samstæðu.  

Hægt er að steypa saman:  

* Tengd fyrirtæki sem hafa ólíka bókhaldslykla.  
* Fyrirtæki sem nota ólík fjárhagsár og gjaldmiðla.  
* Annað hvort öll upphæðin eða tiltekin prósenta af fjárhagsupplýsingum fyrirtækis
* Nota mismunandi gengi gjaldmiðla á einstökum fjárhagsreikningum
* Fyrirtæki í öðrum bókhalds- og viðskiptastjórnunarforritum

Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Bókhaldslykillinn er óháður bókhaldslyklum á fyrirtækiseiningum. Bókhaldslyklar í fyrirtækiseiningum geta verið frábrugðnir einum öðrum. Settur er upp listi yfir fyrirtæki sem á að steypa saman, votta bókhaldsgögn fyrir samsteypu, flytja inn úr skrám eða gagnagrunnum og búa til samsteypuskýrslur. Frekari upplýsingar er að finna í [Setja upp fyrirtækjasamstæðu](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Að steypa saman fjárhagsgögnum getur einkum haft þýðingu í tengslum við ferla innan samstæða. Nánari upplýsingar er að finna í [Stjórnun samstæðufærslna](intercompany-manage.md).

## Nota skýrsluna staða Prófstöðu samstæðunnar

 **Skýrslan Samstæða Reynslustaða**  getur gefið þér yfirlit yfir fjárhagslegt heilsufar fyrirtækisins. Skýrslan sameinar fjárhagsfærslur frá hverju fyrirtæki í nýju fyrirtæki sem stofnað var fyrir samstæðugögnin. Þessi fyrirtæki eru gjarnan nefnd  *Samstæðureikningsskil*. Samstæðufyrirtækið er bara geymir fyrir samstæðugögnin og er ekki með nein búgögn í viðskiptum. Fyrirtækin sem þú setur inn í samstæðufyrirtækið verða að **Viðskiptaeiningum** í skýrslunni. Frekari upplýsingar er að finna í [Setja upp fyrirtækjasamstæðu](finance-consolidated-company-reporting-setup.md). Ef fjórar fyrirtækiseiningar eða færri eru í skýrslunni er einnig hægt að  **nota skýrsluna steypa Prufustöðu (4)** .  

Í skýrslunni kemur fram lína fyrir hvern lykil og fylgir skipulagi bókhaldslykilsins. Lykill er ekki sýndur ef allar upphæðirnar í línunni eru 0. Í skýrslunni koma fram eftirfarandi upplýsingar um hvern lykil:

* Lykilnúmer og heiti lykils.
* Samtölur fyrir samstæðufyrirtækið og hverja fyrirtækiseiningu. Samtölur geta birt annað hvort sem hreyfing eða staða til dagsetningar.
* Útilokanir, gerðar í bókhaldi samsteypufyrirtækis. Losunarskýrslur Sýna alltaf fyrir tímabil sem samsvarar reikningsári samstæðufyrirtækis.
* Samtala fyrir samstæðufyrirtækið eftir útilokanir Sýna annað hvort sem hreyfingar eða staða til dags.

## Gögnum steypt saman

Ef tölurnar sem eru fluttar úr fyrirtækiseiningum yfir í samstæðufyrirtækið eru raunverulegar  *samstæðurnar*. Áður en þú sameinar er ágætt að athuga hvort munur er á grunnupplýsingum í fyrirtækiseiningum og í samstæðufyrirtækinu. Nota má tvær skýrslur til að prófa gagnagrunn og skrá.

### Gagnaprófun fyrir samsteypu

Prófa gögnin áður en það er flutt í samstæðufyrirtækið. [!INCLUDE[prod_short](includes/prod_short.md)] athugar muninn á upplýsingunum í fyrirtækiseiningunum og samstæðufyrirtækinu. Til dæmis hvort munur er á reikningsnúmerum og víddarkóðum. Áður en hægt er að keyra skýrsluna verður að leiðrétta villur. Hægt er að prófa gagnagrunninn eða ef gögn eru flutt inn úr XML-skrá er hægt að prófa skrána.  

1. Samsteypufyrirtækið er opnað.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Prófið skal skrá og gagnasafnið á eftirfarandi hátt:  

    * Til að framkvæma prófun á skrá, skal velja **Prófa skrá** aðgerðina, slá inn nafn skrárinnar sem á að prófa og velja síðan **Prenta**.  
    * Til að framkvæma prófun á gagnagrunni, skal velja **Prófa gagngrunn**.  

### Keyra samstæðu

Þegar gögnin hafa verið prófuð er hægt að flytja það í samstæðufyrirtækið.  

1. Skráðu þig inn samstæðufyrirtækið.  
2. Í **Hlutverkamiðstöð Endurskoðandi** skal velja **Keyra samstæðu** aðgerðina.  
3. Fylltu út nauðsynlega reiti.  
4. Í síuhlutanum skal stilla síu fyrir viðeigandi fyrirtækiseiningu eða fyrirtækisheiti.  
5. Einnig má tímasetja skýrsluna til að keyra á hentugum tíma.  

## Taka út endurteknar færslur

Eftir að félög hafa verið steypt þarf að finna og fella niður allar færslur sem eru skráðar oftar en einu sinni á milli fyrirtækja. Að vinna með samstæðulosanir er handvirkt ferli.  

Að taka út endurteknar færslur:

1. Finna má færslur sem gætu þurft að leiðrétta og færa inn almenna færslubókarlínurnar til að útrýma þeim.
2. Keyrðu skýrsluna **Samstæðuútilokanir fjárhags** til að hjálpa þér við að meta áhrif almennu færslubókarlínanna fyrir bókun.
3. Bókaðu leiðréttar færslur.

 **Skýrslan losunarskýrsla**  fyrir fjárhagssameiningu birtir stöðu fyrir prófjöfnunar þar sem hægt er að líkja eftir afleiðingum af útrýmingu færslna. Skýrslan ber saman færslur í samstæðufyrirtækinu við útilokanir sem færðar hafa verið inn í færslubókina.

Áður en hægt er að taka fyrirtækiseiningu með í skýrsluna verður að setja upp eininguna á  **síðunni fyrirtækiseiningar** .  **Velja verður reitinn Samstæða** .

Lína er stofnuð fyrir hvern lykil og fylgir skipulagi bókhaldslykilsins. Lykill er ekki sýndur ef allar upphæðir í línunni eru 0. Eftirfarandi upplýsingar koma fram um hvern reikning:

* Reikningsnúmer.
* Nafn lykils.
* Ef einn eða fleiri fyrirtækiseiningar voru valdir í reitnum kóti  **fyrirtækiseiningar í**  beiðninnar birtist Samtala sem sýnd er fyrir samstæðufyrirtækið út fyrir valdar fyrirtækiseiningar og útilokanir. Ef reiturinn Fyrirtækiseiningin  **var ekki fylltur út**  er Samtala fyrir samstæðufyrirtækið útilokanir.
* Ef fyrirtækiseiningarkóti var valinn í  **reitnum fyrirtækiseiningarkóti**  á beiðingarsíðunni eru heildarsýnir fyrir innfluttar færslur í fyrirtækiseiningareiningunni. Ef reiturinn Fyrirtækiskóti  **var ekki fylltur út**  sjást heildarsýnir fyrir bókuðu útilokanir í samstæðufyrirtækinu.
* Samtala samsteypufyrirtækis, að öllum fyrirtækjaeiningum og bókuðum útilokunum meðtöldum.
* Útrýmingar sem gera á í samstæðufyrirtækinu. Þ.e. færslurnar í almennu færslubókinni sem er valin á beiðblaðsíðunni.
* Bókunartexti afritaður eftir færslubók.
* Samtala samstæðufyrirtækis eftir útilokanir ef þær eru bókaðar.

## Að flytja út og flytja inn sameinuð gögn milli gagnagrunna

Ef gögn fyrirtækiseiningar eru í öðrum gagnagrunni þarf að flytja gögnin út í skrá áður en hægt er að hafa þau með í samstæðunni. Flytja þarf hvert fyrirtæki fyrir sig. Í þessum tilgangi skal nota runuvinnsluna **Útflutningur samstæðu**.  

> [!TIP]
> Notaðu sama ferlið til að flytja út sameinuð gögn sem þarf að senda á Dynamics 365 Finance, t.d. ef núverandi fyrirtækiseining er dótturfyrirtæki og móðurfyrirtækið notar Dynamics 365 Finance.

Þegar búið er að keyra runuvinnsluna, eru allar færslur í fjárhagsreikninga unnar. Samtala er fengin og flutt út úr efni færslna í reitunum **Upphæð** í sérhverri samsetningu valinnar víddar og dagsetningar. Næsta samsetning valinna vídda og dagsetningar er unnin með sama lykilnúmeri. Þá eru settar inn samsetningar í næsta lykilnúmeri o. þ. frv.  

Útfluttar færslur innihalda eftirfarandi reiti: **Reikningur nr.**, **Bókunardags.** og **Upphæð**. Ef upplýsingar um víddir voru líka fluttar út, eru víddarkóðar og víddargildi þar á meðal.  

1. Ef samtala reitanna **Upphæð** er debet er reikningsnúmerið sem sett er upp í reitnum **Samstæðu-debetreikn.** í fyrirtækiseiningunni flutt út í línuna fyrir hverja útflutta línu. Ef samtalan er kredit er samsvarandi númer í reitnum **Samstæðu-kreditreikn.** flutt út í línuna.  
2. Sú dagsetning sem er notuð fyrir útfluttar línu er annaðhvort lokadagsetning tímabils eða sú dagsetning þegar útreikningur fer fram.  
3. Víddargildið sem er flutt út fyrir færsluna verður víddargildið í fyrirtækjasamstæðu sem tilgreint er í  **reitnum kóti**  samstæðu fyrir víddargildið. Ef víddargildið fyrir samstæðufyrirtæki hefur ekki verið fært inn í  **reitinn samstæður**  fyrir víddargildið verður víddargildið sjálft flutt út í línuna.  
4. Auk þess innihalda XML-skrárnar gengi gjaldmiðils innan samsteyputímabilsins. Þessi gengi eru innifalin í aðskildum hluta í upphafi skrárinnar.  

## Sjá einnig

[Setja upp sameiningu fyrirtækis](finance-consolidated-company-reporting-setup.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]