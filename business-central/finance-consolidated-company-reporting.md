---
title: Steypa saman gögnum frá mörgum fyrirtækjum
description: Í greininni er útskýrt hvernig hægt er að sameina fjárhagsfærslur tveggja eða fleiri aðskilins félaga (dótturfyrirtækja) í samstæðufyrirtæki.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
---

# Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Önnur nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem þarf að tilkynna um í móðurfyrirtækjum. [!INCLUDE [prod_short](includes/prod_short.md)] gefur bókhaldstæki sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfélögum) í samstæðufyrirtæki.  

Hvert fyrirtæki sem sér um sameiningu er kallað viðskiptaeining. Fyrirtækið sem þú blandar saman gögnum er kallað samstæðufyrirtækið.  

Hægt er að millifæra Fjárhagsleg gögn frá dótturfélögum til samstæðunnar, jafnvel þótt dótturfélag noti  [!INCLUDE [prod_short](includes/prod_short.md)]  í mismunandi umhverfi. Til að fræðast nánar um tengingu við annað umhverfi er farið í að  [Setja upp samstæðufyrirtæki](finance-consolidated-company-reporting-setup.md#busunit).

Ef Fjárhagsleg Yfirlit fyrirtækiseiningar nota annan gjaldmiðil en samstæðufyrirtækið verður að setja upp gengi fyrir samstæðu. Til að fræðast meira um gengi fyrir sameiningu er farið að  [Setja upp samstæðufyrirtæki](finance-consolidated-company-reporting-setup.md#exchrates).  

Hægt er að steypa saman:  

* Tengd fyrirtæki sem hafa ólíka bókhaldslykla.  
* Fyrirtæki sem nota ólík fjárhagsár og gjaldmiðla.  
* Annað hvort heildarupphæðin eða hlutfall af fjárhagsupplýsingum fyrirtækis.
* Notað mismunandi gengi gjaldmiðla í einstökum fjárhagsreikningum.
* Fyrirtækjum í öðrum bókhalds-og fyrirtækjaforritum.
* Fyrirtækjum í ólíku  [!INCLUDE [prod_short](includes/prod_short.md)]  umhverfi.

Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Bókhaldslykillinn er óháður bókhaldslyklum á fyrirtækiseiningum. Bókhaldslyklar í fyrirtækiseiningum geta verið frábrugðnir einum öðrum. Til að fræðast meira um uppsetningu á samstæðu, er farið í að  [Setja upp samstæðufyrirtæki](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Sameining fjárhagslegra gagna getur einkum átt við um samstæðuferla. Til að fræðast meira um eiginleika innan samstæðu er farið til að  [stjórna samstæðufærslum](intercompany-manage.md).

## Gögnum steypt saman

Áður en þú sameinar er gott ráð að prófa gögnin áður en það er flutt í samstæðufyrirtækið. [!INCLUDE[prod_short](includes/prod_short.md)] athugar muninn á upplýsingunum í fyrirtækiseiningunum og samstæðufyrirtækinu. Til dæmis hvort munur er á reikningsnúmerum og víddarkóðum. Leiðréttið villur sem þú finnur áður en þú keyrir skýrsluna. Hægt er að prófa gagnagrunninn eða ef gögn eru flutt inn úr XML-skrá er skráin.

### Prófa gögnin áður en þú sameinar

1. Samsteypufyrirtækið er opnað.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Prófið skal skrá og gagnasafnið á eftirfarandi hátt:  

    * Til að framkvæma prófun á skrá, skal velja **Prófa skrá** aðgerðina, slá inn nafn skrárinnar sem á að prófa og velja síðan **Prenta**.  
    * Til að framkvæma prófun á gagnagrunni, skal velja **Prófa gagngrunn**.  

### Keyra samstæðu

Þegar gögnin hafa verið prófuð er hægt að flytja það í samstæðufyrirtækið. Uppsetningarhandbók fyrir hjálpartæki mun hjálpa þér í gegnum ferlið.

> [!NOTE]
> Þegar samstæðan er keyrð er hægt að velja fyrirtækin með. Ef samstæðufyrirtækið þitt hefur ekki aðgang að einu eða fleiri dótturfélögum mun handbókin veita þér aðgang að þeim.

1. Skráðu þig inn samstæðufyrirtækið.  
2.  **Á síðunni fyrirtækiseiningar**  skal velja  **aðgerðina sameina** .  
3. Fylltu út nauðsynlega reiti.  

## Nota skýrsluna staða Prófstöðu samstæðunnar

 **Skýrslan Samstæða Reynslustaða**  getur gefið þér yfirlit yfir fjárhagslegt heilsufar fyrirtækisins. Skýrslan sameinar fjárhagsfærslur frá hverju fyrirtæki í nýju fyrirtæki sem stofnað var fyrir samstæðugögnin. Samstæðufyrirtækið er bara geymir fyrir samstæðugögnin og er ekki með nein búgögn í viðskiptum. Fyrirtækin sem þú setur inn í samstæðufyrirtækið verða að **Viðskiptaeiningum** í skýrslunni. Ef fjórar fyrirtækiseiningar eða færri eru í skýrslunni er einnig hægt að  **nota skýrsluna steypa Prufustöðu (4)** .  

Í skýrslunni kemur fram lína fyrir hvern lykil og fylgir skipulagi bókhaldslykilsins. Lykill er ekki sýndur ef allar upphæðirnar í línunni eru 0. Í skýrslunni koma fram eftirfarandi upplýsingar um hvern lykil:

* Lykilnúmer og heiti lykils.
* Samtölur fyrir samstæðufyrirtækið og hverja fyrirtækiseiningu. Samtölur geta birt annað hvort sem hreyfing eða staða til dagsetningar.
* Útilokanir, gerðar í bókhaldi samsteypufyrirtækis. Losunarskýrslur Sýna alltaf fyrir tímabil sem samsvarar reikningsári samstæðufyrirtækis.
* Samtala fyrir samstæðufyrirtækið eftir útilokanir Sýna annað hvort sem hreyfingar eða staða til dags.

## Taka út endurteknar færslur

Eftir að félög hafa verið steypt þarf að finna og fella niður allar færslur sem eru skráðar oftar en einu sinni á milli fyrirtækja. Að vinna með samstæðulosanir er handvirkt ferli.  

Að taka út endurteknar færslur:

1. Finna má færslur sem gætu þurft að leiðrétta og færa inn almenna færslubókarlínurnar til að útrýma þeim.
2. Keyrðu skýrsluna **Samstæðuútilokanir fjárhags** til að hjálpa þér við að meta áhrif almennu færslubókarlínanna fyrir bókun.
3. Bókaðu leiðréttar færslur.

 **Skýrslan losunarskýrsla**  fyrir fjárhagssameiningu birtir stöðu fyrir prófjöfnunar þar sem hægt er að líkja eftir afleiðingum af útrýmingu færslna. Skýrslan ber saman færslur í samstæðufyrirtækinu við útilokanir sem færðar hafa verið inn í færslubókina.

Áður en hægt er að hafa fyrirtækiseiningu í skýrslunni þarf að setja eininguna upp á  **síðunni fyrirtækiseiningar** . Ganga skal úr skugga um að kveikt sé  **á samstæðu**  skipta.

Lína er stofnuð fyrir hvern lykil og fylgir skipulagi bókhaldslykilsins. Lykill er ekki sýndur ef allar upphæðir í línunni eru 0. Í skýrslunni koma fram eftirfarandi upplýsingar um hvern lykil:

* Reikningsnúmer.
* Nafn lykils.
* Ef einn eða fleiri fyrirtækiseiningar voru valdir í reitnum kóti  **fyrirtækiseiningar í**  beiðninnar birtist Samtala sem sýnd er fyrir samstæðufyrirtækið út fyrir valdar fyrirtækiseiningar og útilokanir. Ef reiturinn Fyrirtækiseiningin  **var ekki fylltur út**  er Samtala fyrir samstæðufyrirtækið útilokanir.
* Ef fyrirtækiseiningarkóti var valinn í  **reitnum fyrirtækiseiningarkóti**  á beiðingarsíðunni eru heildarsýnir fyrir innfluttar færslur í fyrirtækiseiningareiningunni. Ef reiturinn Fyrirtækiskóti  **var ekki fylltur út**  sjást heildarsýnir fyrir bókuðu útilokanir í samstæðufyrirtækinu.
* Samtala samsteypufyrirtækis, að öllum fyrirtækjaeiningum og bókuðum útilokunum meðtöldum.
* Útrýmingar sem gera á í samstæðufyrirtækinu. Þ.e. færslurnar í almennu færslubókinni sem er valin á beiðblaðsíðunni.
* Bókunartexti afritaður eftir færslubók.
* Samtala samstæðufyrirtækis eftir útilokanir ef þær eru bókaðar.

## Að flytja út og flytja inn sameinuð gögn milli gagnagrunna

Ef gögn fyrir fyrirtækiseiningu eru í öðru gagnasafni er hægt að gera handbók um skráaflutning eða sjálfvirka vinnslu með API. Til að fræðast meira um API skaltu fara að  [nota API okkar til að deila gögnum sjálfkrafa yfir umhverfi](#use-our-api-to-automatically-share-data-across-environments).

Í þessum kafla er lýst handbókinni, skráarmiðinu.

Gögnin eru flutt út í skrá áður en hún er innifalin í samstæðunni. Flytja hvert fyrirtæki sérstaklega með því að  **nota keyrsluna útflutningur samstæðu** .  

> [!TIP]
> Notaðu sama ferli til að flytja út samstæður gagna sem þú verður að senda til Dynamics 365 Finance. Til dæmis, ef Fyrirtækiseining er dótturfyrirtæki og móðurfyrirtæki notar Dynamics 365 Finance.

Þegar búið er að keyra runuvinnsluna, eru allar færslur í fjárhagsreikninga unnar. Samtala er fengin og flutt út úr efni færslna í reitunum **Upphæð** í sérhverri samsetningu valinnar víddar og dagsetningar. Næsta samsetning valinna vídda og dagsetningar er unnin með sama lykilnúmeri. Þá eru settar inn samsetningar í næsta lykilnúmeri o. þ. frv.  

Útfluttar færslur innihalda eftirfarandi reiti: **Reikningur nr.**, **Bókunardags.** og **Upphæð**. Ef upplýsingar um víddir voru líka fluttar út, eru víddarkóðar og víddargildi þar á meðal.  

1. Ef samtala reitanna **Upphæð** er debet er reikningsnúmerið sem sett er upp í reitnum **Samstæðu-debetreikn.** í fyrirtækiseiningunni flutt út í línuna fyrir hverja útflutta línu. Ef samtalan er kredit er samsvarandi númer í reitnum **Samstæðu-kreditreikn.** flutt út í línuna.  
2. Sú dagsetning sem er notuð fyrir útfluttar línu er annaðhvort lokadagsetning tímabils eða sú dagsetning þegar útreikningur fer fram.  
3. Víddargildið sem er flutt út fyrir færsluna verður víddargildið í fyrirtækjasamstæðu sem tilgreint er í  **reitnum kóti**  samstæðu fyrir víddargildið. Ef víddargildið fyrir samstæðufyrirtæki hefur ekki verið fært inn í  **reitinn samstæður**  fyrir víddargildið verður víddargildið sjálft flutt út í línuna.  
4. Auk þess innihalda XML-skrárnar gengi gjaldmiðils innan samsteyputímabilsins. Þessi gengi eru innifalin í aðskildum hluta í upphafi skrárinnar.  

## Notaðu API okkar til að deila gögnum sjálfkrafa yfir umhverfi

[!INCLUDE [prod_short](includes/prod_short.md)] gefur API sem gerir það kleift að samnýta fjárhagsgögn úr fyrirtækiseiningum á samstæðufyrirtækið. API er laust til notkunar og auðvelt að setja upp. Við skulum jafnvel deila gögnum í öllu  [!INCLUDE [prod_short](includes/prod_short.md)]  umhverfi. Til dæmis gæti þurft að deila yfir umhverfi þegar fyrirtækiseiningar eru ekki í sömu Azure landsgratíum. Til að fá frekari upplýsingar um notkun API til að gera samstæðuferlið sjálfvirka er farið í að  [Setja upp samstæðufyrirtæki](finance-consolidated-company-reporting-setup.md#busunit).

## Sjá einnig

[Setja upp fyrirtækjasamstæðu](finance-consolidated-company-reporting-setup.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]