---
title: Steypa saman gögnum frá mörgum fyrirtækjum
description: Þessi grein útskýrir hvernig hægt er að sameina fjárhagsfærslur tveggja eða fleiri fyrirtækja (dótturfyrirtæki) í samstæðufyrirtæki.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Önnur nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem þarf að tilkynna um í móðurfyrirtækjum. [!INCLUDE [prod_short](includes/prod_short.md)] gefur endurskoðendum verkfæri sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfyrirtækjum) í samsteypufyrirtæki.  

Hvert fyrirtæki í samstæðufyrirtæki nefnist fyrirtækiseining. Fyrirtækið sem gögnin eru sameinuð í kallast samsteypufyrirtæki.  

Hægt er að flytja fjárhagsgögn frá dótturfélögum til samsteypufyrirtækis, jafnvel þótt dótturfyrirtækin noti [!INCLUDE [prod_short](includes/prod_short.md)] í mismunandi umhverfi. Nánari upplýsingar um hvernig á að tengjast öðrum umhverfi er farið í [Setja upp samstæðu fyrirtækis](finance-consolidated-company-reporting-setup.md#busunit).

Ef ársreikningar fyrirtækiseiningar nota annan gjaldmiðil en samsteypufyrirtækið verður að setja upp gengi gjaldmiðla fyrir samsteypu. Nánari upplýsingar um gengi samsteypu eru í [Setja upp samstæðufyrirtæki](finance-consolidated-company-reporting-setup.md#exchrates).  

Hægt er að steypa saman:  

* Tengd fyrirtæki sem hafa ólíka bókhaldslykla.  
* Fyrirtæki sem nota ólík fjárhagsár og gjaldmiðla.  
* Annaðhvort heildarupphæð eða prósentuhlutfall af fjárhagsupplýsingum fyrirtækis.
* Notkun mismunandi gengis gjaldmiðla í einstökum fjárhagsreikningum.
* Fyrirtæki í öðrum bókhalds- og viðskiptastjórnunarforritum.
* Fyrirtæki í ólíku [!INCLUDE [prod_short](includes/prod_short.md)] umhverfi.

Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Bókhaldslykillinn er óháður bókhaldslyklinum í fyrirtækiseiningunum. Bókhaldslykillinn í fyrirtækiseiningunum getur verið frábrugðinn öðrum. Nánari upplýsingar um uppsetningu samsteypu eru í [Setja upp samstæðu fyrirtækis](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Sameining fjárhagsgagna getur skipt máli fyrir ferli milli fyrirtækja. Nánari upplýsingar um aðgerðir milli fyrirtækja eru notaðar til að [vinna með færslur](intercompany-manage.md) milli fyrirtækja.

## Gögnum steypt saman

Áður en steypa er saman er ágætt að prófa gögnin áður en það er flutt til samsteypufyrirtækis. [!INCLUDE[prod_short](includes/prod_short.md)] athugar muninn á upplýsingunum í fyrirtækiseiningunum og samstæðufyrirtækinu. Til dæmis hvort munur er á reikningsnúmerum og víddarkóðum. Leiðrétta allar villur sem finnast áður en skýrslan er keyrð. Hægt er að prófa gagnagrunninn eða skrána ef verið er að flytja inn gögn úr XML-skrá.

### Prófa gögnin áður en þú sameinar

1. Samsteypufyrirtækið er opnað.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Prófa skrána og gagnagrunninn á eftirfarandi hátt:  

    * Til að framkvæma prófun á skrá, skal velja **Prófa skrá** aðgerðina, slá inn nafn skrárinnar sem á að prófa og velja síðan **Prenta**.  
    * Til að framkvæma prófun á gagnagrunni, skal velja **Prófa gagngrunn**.  

### Keyra samstæðu

Þegar gögn hafa verið prófuð er hægt að flytja það til samsteypufyrirtækis. Leiðsagnarforrit með hjálp hjálpar þér í gegnum ferlið.

> [!NOTE]
> Þegar samsteypan er keyrð er hægt að velja fyrirtækin sem taka á með. Ef samsteypufyrirtækið hefur ekki aðgang að einu eða fleiri dótturfyrirtækjum leyfir leiðarvísirinn aðgang að þeim.

1. Skráðu þig inn samstæðufyrirtækið.  
2. Á síðunni Fyrirtækiseiningar **skal velja aðgerðina Sameina**  **.**   
3. Fylltu út nauðsynlega reiti.  

## Nota skýrsluna Samstæða - Prófjöfnuður

Skýrslan **Samstæða - Prófjöfnuður** getur gefið yfirsýn yfir almenna fjárhagslega heilsu fyrirtækisins. Skýrslan sameinar fjárhagsfærslur frá hverju fyrirtæki í nýju fyrirtæki sem stofnað er fyrir samsteypugögnin. Samsteypufyrirtækið er bara geymir fyrir samsteypugögnin og hefur engin viðskiptagögn í beinni. Fyrirtækin sem þú setur inn í samstæðufyrirtækið verða að **Viðskiptaeiningum** í skýrslunni. Ef fyrirtækiseiningar eru fjórar eða færri er einnig hægt að nota skýrsluna **Samstæða - Prófjöfnuður (4).** .  

Skýrslan sýnir línu fyrir hvern reikning og fylgir uppbyggingu bókhaldslykilsins. Reikningur birtist ekki ef allar upphæðir í línunni eru 0. Í skýrslunni eru eftirfarandi upplýsingar um hvern reikning:

* Reikningsnúmer og heiti reikningsins.
* Samtölur samsteypufyrirtækis og hverrar fyrirtækiseiningar. Samtölur geta annaðhvort sýnt sem hreyfingu eða stöðu til dags.
* Útilokanir, gerðar í bókhaldi samsteypufyrirtækis. Útilokanir sýna alltaf tímabil sem samsvarar reikningsári samsteypufyrirtækis.
* Samtala samsteypufyrirtækis eftir útilokanir sýna annaðhvort sem hreyfingu eða stöðu til dags.

## Taka út endurteknar færslur

Þegar fyrirtækin hafa verið sameinuð þarf að finna og losa allar færslur sem skráðar eru oftar en einu sinni á milli fyrirtækja. Að vinna með samstæðulosanir er handvirkt ferli.  

Að taka út endurteknar færslur:

1. Finna færslur sem þarfnast leiðréttingar og færa inn færslubókarlínur til að losa þær.
2. Keyrðu skýrsluna **Samstæðuútilokanir fjárhags** til að hjálpa þér við að meta áhrif almennu færslubókarlínanna fyrir bókun.
3. Bókaðu leiðréttar færslur.

Skýrslan **Útilokanir** fjárhags sýnir prófjöfnuð þar sem hægt er að líkja eftir afleiðingum þess að útiloka færslur. Skýrslan ber saman færslur samsteypufyrirtækis og útilokanir sem færðar eru inn í færslubókina.

Áður en hægt er að taka fyrirtækiseiningu með í skýrslu verður að setja upp einingu á síðunni **Fyrirtækiseiningar** . Ganga þarf úr skugga um að kveikja á **vífærinu Samstykkja** .

Lína er búin til fyrir hvern reikning í kjölfar uppbyggingar bókhaldslykilsins. Reikningur birtist ekki ef allar upphæðir í línunni eru 0. Í skýrslunni eru eftirfarandi upplýsingar um hvern reikning:

* Reikningsnúmer.
* Nafn lykils.
* Ef einn eða fleiri kótar fyrirtækjaeiningar voru valdir í reitnum **Kóti** fyrirtækjaeiningar á beiðnisíðunni tekur samtala samsteypufyrirtækisins ekki með völdum fyrirtækiseiningum og útilokunum. Hafi reiturinn Kóti **fyrirtækjaeiningar ekki verið fylltur út** útilokar samtala samsteypufyrirtækis útilokanir.
* Ef valinn var kóti fyrirtækjaeiningar í reitnum **Kóti** fyrirtækjaeiningar á beiðnisíðunni sýnir samtala innfluttra færslna frá fyrirtækiseiningunni. Hafi reiturinn Kóti **fyrirtækjaeiningar ekki verið fylltur** út sýnir samtala bókaðra útilokana í samstæðufyrirtækinu.
* Samtala samsteypufyrirtækis, að öllum fyrirtækjaeiningum og bókuðum útilokunum meðtöldum.
* Útilokanir sem gerðar eru í samsteypufyrirtækinu. Það er, færslurnar í færslubókinni sem valdar eru á beiðnisíðunni.
* Bókunartexti afritaður eftir færslubók.
* Samtala samsteypufyrirtækis eftir útilokanir, ef þær eru bókaðar.

## Að flytja út og flytja inn sameinuð gögn milli gagnagrunna

Ef gögn fyrirtækiseiningar eru í öðrum gagnagrunni er hægt að gera handvirka skráamiðaða millifærslu eða gera ferlið sjálfvirkt með því að nota API. Til að fræðast meira um API er farið í [Notkun API okkar til að deila gögnum sjálfkrafa í umhverfinu](#use-our-api-to-automatically-share-data-across-environments).

Í þessum hluta er lýst handvirku ferli sem byggir á skrám.

Gögnin eru flutt út í skrá áður en þau eru tekin með í samsteypuna. Flytja hvert fyrirtæki út sérstaklega með keyrslunni **Flytja út samstæðu** .  

> [!TIP]
> Sama ferlið er notað til að flytja út samsteypugögn sem þarf að senda Dynamics 365 Finance. Ef fyrirtækiseiningin er t.d. dótturfyrirtæki og móðurfyrirtækið notar Dynamics 365 Finance.

Þegar búið er að keyra runuvinnsluna, eru allar færslur í fjárhagsreikninga unnar. Samtala er fengin og flutt út úr efni færslna í reitunum **Upphæð** í sérhverri samsetningu valinnar víddar og dagsetningar. Unnið er úr næstu samsetningu valinnar víddar og dagsetningar með sama reikningsnúmeri. Þá er unnið úr samsetningum næsta reikningsnúmers og svo fram vegar.  

Útfluttar færslur innihalda eftirfarandi reiti: **Reikningur nr.**, **Bókunardags.** og **Upphæð**. Ef upplýsingar um víddir voru líka fluttar út, eru víddarkóðar og víddargildi þar á meðal.  

1. Ef samtala reitanna **Upphæð** er debet er reikningsnúmerið sem sett er upp í reitnum **Samstæðu-debetreikn.** í fyrirtækiseiningunni flutt út í línuna fyrir hverja útflutta línu. Ef samtalan er kredit er samsvarandi númer í reitnum **Samstæðu-kreditreikn.** flutt út í línuna.  
2. Sú dagsetning sem er notuð fyrir útfluttar línu er annaðhvort lokadagsetning tímabils eða sú dagsetning þegar útreikningur fer fram.  
3. Víddargildið sem flutt er út fyrir færsluna verður víddargildi samsteypufyrirtækisins sem er tilgreint í reitnum **Kóti** samstæðu fyrir það víddargildi. Hafi víddargildi samsteypufyrirtækis ekki verið fært inn í reitinn **Sameinaður kóti** fyrir víddargildið verður víddargildið sjálft flutt út í línuna.  
4. Auk þess innihalda XML-skrárnar gengi gjaldmiðils innan samsteyputímabilsins. Þessi gengi eru innifalin í aðskildum hluta í upphafi skrárinnar.  

## Notaðu API okkar til að deila gögnum sjálfkrafa í umhverfi

[!INCLUDE [prod_short](includes/prod_short.md)] veitir API sem gerir kleift að gera samnýtingu fjárhagslegra gagna frá fyrirtækiseiningum sjálfvirka til samsteypufyrirtækis. API er ókeypis í notkun og auðvelt að setja upp. Við skulum jafnvel deila gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] umhverfinu. Til dæmis gæti þurft að deila umhverfinu þegar fyrirtækiseiningar eru ekki í sömu Azure-landfræði. Nánari upplýsingar um notkun API eru notaðar til að gera samsteypuferlið sjálfvirkt með því að fara í [Setja upp samsteypufyrirtæki](finance-consolidated-company-reporting-setup.md#busunit).

## Sjá einnig

[Setja upp fyrirtækjasamstæðu](finance-consolidated-company-reporting-setup.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]