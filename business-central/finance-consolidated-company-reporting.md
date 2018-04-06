---
title: "Steypa saman gögnum frá mörgum fyrirtækjum | Microsoft Docs"
description: "Fá yfirlit í formi samantektar á fjárhagslegri stöðu fyrirtækja þinna."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 07/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9309868cbcee8fb969c318acfb6ce8844e78b687
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum
Ef þú ert með fleiri en eitt fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)], getur Sameinuð prófjafnaðarskýrsla í Mitt hlutverk endurskoðanda gefið þér yfirsýn yfir fjárhagslega stöðu fyrirtækja þinna í heild.  

Skýrslan sameinar fjárhagsfærslur frá öllum fyrirtækjum þínum í nýtt fyrirtæki sem þú stofnar til að hýsa sameinuðu gögnin. Venjulega er vísað til þessa fyrirtækis sem „samstæðufyrirtækisins“. Samstæðufyrirtækið er aðeins geymsla fyrir sameinuðu gögnin og inniber engin lifandi viðskiptagögn. Fyrirtækin sem þú setur inn í samstæðufyrirtækið verða að **Viðskiptaeiningum** í skýrslunni.

Að steypa saman fjárhagsgögnum getur einkum haft þýðingu í tengslum við ferla innan samstæða. Nánari upplýsingar er að finna í [Stjórnun samstæðufærslna](intercompany-manage.md).

Hægt er að steypa saman:  

* Tengd fyrirtæki sem hafa ólíka bókhaldslykla.  
* Fyrirtæki sem nota ólík fjárhagsár og gjaldmiðla.  
* Annað hvort öll upphæðin eða tiltekin prósenta af fjárhagsupplýsingum fyrirtækis
* Nota mismunandi gengi gjaldmiðla á einstökum fjárhagsreikningum

Það eru tvær leiðir til að setja upp útlit á skýrslu, út frá margbreytileika fyrirtækja þinna:

* Ef ekki er þörf á ítarlegum stillingum, t.d. þeim sem notaðar eru til að setja upp fyrirtæki sem þú átt aðeins hlut í, geturðu notað **Fyrirtækjasamstæða** leiðsagnarforrit með aðstoð til að setja upp samstæðu með hraði. Leiðbeiningarnar aðstoða þig gegnum grunnatriðin.
* Ef þörf er á fleiri ítarlegum stillingum, geturðu sett upp samstæðufyrirtækið og fyrirtækjaeiningarnar sjálf(ur).

## <a name="to-do-a-simple-consolidation-setup"></a>Að setja upp samstæðu á einfaldan máta
Ef samstæðan er einföld, til dæmis vegna þess að þú ert eigandi allra fyrirtækjaeininganna sem á að steypa saman, munu **Fyrirtækjasamstæða** leiðbeiningar um uppsetningu með aðstoð leiða þig í gegnum eftirfarandi skref:

* Veldur hvort á að stofna nýtt samstæðufyrirtæki, eða steypa gögnunum saman í fyrirtæki sem þú hefur þegar stofnað fyrir samstæðuna. Fyrirtækið ætti ekki að innihalda færslur. 
* Forskoða niðurstöður. [!INCLUDE[d365fin](includes/d365fin_md.md)] staðfestir að hægt sé að flytja aðalgögnin og færslur yfir í samstæðufyrirtækið án vandkvæða.

Fylgið eftirfarandi skrefum til að nota leiðbeiningar um uppsetningu með hjálp:

1. Í Hlutverkamiðstöð **Endurskoðandi** skal velja **Uppsetning með hjálp** aðgerðina.
2. Velja skal **Setja upp samstæðuskýrslugerð** og fylgja svo leiðbeiningunum fyrir hvert skref í uppsetningu með hjálp.

## <a name="to-do-an-advanced-consolidation-setup"></a>Setja upp ítarlegar samstæður
Ef þörf er á fleiri ítarlegum stillingum fyrir samstæðuna, geturðu sett upp samstæðu handvirkt. Ef til dæmis um ræðir fyrirtæki sem þú átt aðeins hlut í, eða fyrirtæki sem þú vilt ekki að séu hluti af samstæðunni. Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] gerir þér kleift að setja upp lista af fyrirtækjum sem steypa á saman, staðfesta bókhaldsgögn áður en þau eru flutt inn í samstæðu, flytja inn skrár og búa til samstæðuskýrslur.  

1. Skráðu þig inn samstæðufyrirtækið.
2. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaeiningar** og velja svo viðeigandi tengil.  
3. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði.  

Ef fyrirtækið þitt notast við erlendan gjaldmiðil, er nauðsynlegt að tiltaka gengið sem nota skal í samstæðunni. Einnig verðu að slá inn samstæðuupplýsingar um fjárhagsreikninga fyrirtækiseiningarinnar. Þessum ferlum er lýst í eftirfarandi hlutum.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Undirbúa fjárhagslykla fyrir samlegð
Ef bókhaldslyklar í fyrirtækjaeiningunni eru ekki þeir sömu og í samstæðufyrirtækinu er nauðsynlegt að búa til fjárhagslykla fyrir samlegðina. Þú getur tilgreint reikninga sem bóka á debet og kredit á, sem og þá aðferð sem nota skal við að umreikna gjaldmiðil í samstæðufyrirtækinu. Þetta er til dæmis gagnlegt ef þú keyrir skýrsluna oft.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.  
2. Opnaðu kortið fyrir reikninginn og fylltu svo út í reitina á **Samstæða** flýtiflipanum.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Að tilgreina gengi gjaldmiðla áður en fyrirtækjum er steypt saman
Ef fyrirtækjaeining notar annan gjaldmiðil en samstæðufyrirtækið, er nauðsynlegt að tiltaka hvaða aðferðir eru notaðar við útreikning gjaldmiðla á hverjum reikningi áður en þú steypir saman. Fyrir hvern fjárhagsreikning ákvarðar innihald reitsins **Umreikniaðferð samstæðunnar** hvaða gengi gjaldmiðla er notað. Á hverju spjaldi fyrirtækiseiningarinnar í **Töflunni Gengi gjaldmiðla** er tilgreint hvort samstæðan noti gengi gjaldmiðla frá fyrirtækiseiningunni eða samstæðufyrirtækinu. Ef notað er gengi gjaldmiðla frá samstæðufyrirtækinu er hægt að breyta gengi gjaldmiðla hjá fyrirtækiseiningunni. Fyrir fyrirtækiseiningu, ef **Gengistafla á spjaldi** fyrirtækjaeiningarinnar inniheldur **Staðbundið**, er hægt að breyta genginu af spjaldi fyrirtækjaeiningarinnar. Gengi er afritað af töflunni **Gengi** en það er hægt að breyta þeim áður en samruni á sér stað.

Í eftirfarandi töflu er gengisaðferðum sem hægt er að nota fyrir lykla lýst.

|Gengi | Dæmigerð notkun |
|---|---|
|Meðalgengi (handvirkt) | Þú reiknar handverk meðalgengi tímabilsins sem á að sameina. Reiknaðu meðaltalið annaðhvort sem reiknað meðaltal eða besta mat og tilgreindu niðurstöðurnar fyrir hverja fyrirtækiseiningu. Notað fyrir rekstrarreikninga.|
|Lokagengi | Notað fyrir efnahagslykla.|
|Síðasta lokagengi | Gengið sem gilti á gengismarkaði á dagsetningunni sem verið er að undirbúa efnahagsreikning og rekstrarreikning fyrir. Gengið er fært inn fyrir hverja fyrirtækiseiningu. Notað fyrir efnahagslykla.|
|Ferill gengis | Gengið sem var í gildi þegar viðskiptin áttu sér stað.|
|Samsett gengi | Upphæðir gildandi tímabils eru umreiknaðar á meðalgengi og bætt við áður skráða stöðu í samstæðufyrirtækinu. Þessi aðferð er iðulega notuð fyrir reikninga óráðstafaðs eigin fjár vegna þess að þeir innihalda upphæðir frá öðrum tímabilum sem eru þar af leiðandi samsettar upphæðir, umreiknaðar út frá ólíku gengi.|
|Gengi eiginfjár | Þetta er svipað og **Samsett**. Mismunur er bókaður á aðra fjárhagsreikninga.|   

Til að tilgreina gengi gjaldmiðla fyrir fyrirtækiseiningar, skal fylgja eftirfarandi skrefum:

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaeiningar** og velja svo viðeigandi tengil.  
2. Á síðunni **Listi yfir fyrirtækiseiningar** skal velja fyrirtækiseininguna, og síðan **Meðalgengi (handvirkt)** aðgerðina.   
3. Á síðunni **Breyta gengi gjaldmiðils** hefur efni í reitnum **Viðmiðunargengi** verið afritað úr töflunni **Gengi gjaldmiðils** en hægt er að breyta því. Lokaðu síðunni.  
4. Veldu aðgerðina **Lokagengi**.  
5. Í reitnum **Upphæð viðmiðunargengis** skal færa inn gengið.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Að útiloka fyrirtæki frá samstæðu
Ef þú vilt ekki að fyrirtæki sé hluti af samstæðunni, geturðu útilokað það. Til að gera það, skal fara í kort fyrirtækiseiningarinnar og hreinsa **Steypa saman** gátreitinn.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Að hafa fyrirtæki í hlutaeign með í samstæðu
Ef þú átt aðeins hlut í fyrirtæki geturðu tengt prósentutölu, sem samsvarar hlutaeigninni í fyrirtækinu, við hverja færslu. Ef þú átt til dæmis 70% hlut í fyrirtækinu, mun samlegðin ná til $70 af reikningi upp á $100. Til að tilgreina prósentutölu eignar þinnar í fyrirtækinu, skal fara í kort fyrirtækiseiningarinnar og slá inn prósentuna í reitnum **Samstæða %**.  

### <a name="to-test-the-data-before-you-consolidate"></a>Gagnaprófun fyrir samsteypu
Þú getur framkvæmt gagnaprófun áður en þú sendir gögnin í samstæðufyrirtækið. [!INCLUDE[d365fin](includes/d365fin_md.md)] athugar muninn á upplýsingunum í fyrirtækiseiningunum og samstæðufyrirtækinu. Til dæmis hvort munur er á reikningsnúmerum og víddarkóðum. Áður en hægt er að keyra skýrsluna verður að leiðrétta villur. Þú getur framkvæmt prófanir á gagnagrunninum, eða skránni, ef þú ert að flytja inn gögn frá XML skrá.   

1. Samsteypufyrirtækið er opnað.  
2. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaeiningar** og velja svo viðeigandi tengil.  
3. Gert er eitt af eftirfarandi:  

    * Til að framkvæma prófun á skrá, skal velja **Prófa skrá** aðgerðina, slá inn nafn skrárinnar sem á að prófa og velja síðan **Prenta**.  
    * Til að framkvæma prófun á gagnagrunni, skal velja **Prófa gagngrunn**.  

## <a name="to-run-the-consolidation"></a>Keyra samstæðuna
Þegar gögn hafa verið prófuð er hægt að senda þau í samstæðufyrirtækið.  

1. Skráðu þig inn samstæðufyrirtækið.  
2. Í **Hlutverkamiðstöð Endurskoðandi** skal velja **Keyra samstæðu** aðgerðina.  
3. Fylltu út nauðsynlega reiti.  
4. Í reitnum **Hvar** skal velja **Nafn fyrirtækis** og síðan velja samstæðufyrirtækið í **er**reitnum.  

## <a name="to-export-and-import-consolidated-data-between-databases"></a>Að flytja út og flytja inn sameinuð gögn milli gagnagrunna
Ef gögn fyrirtækiseiningar eru í öðrum gagnagrunni þarf að flytja gögnin út í skrá áður en hægt er að hafa þau með í samstæðunni. Flytja þarf hvert fyrirtæki fyrir sig. Í þessum tilgangi skal nota runuvinnsluna **Útflutningur samstæðu**.  

Þegar búið er að keyra runuvinnsluna, eru allar færslur í fjárhagsreikninga unnar. Samtala er fengin og flutt út úr efni færslna í reitunum **Upphæð** í sérhverri samsetningu valinnar víddar og dagsetningar. Þá er unnið úr næstu samsetningu valinnar víddar og dagsetningar með sama reikningsnúmeri og síðan úr samsetningu næsta reikningsnúmers og svo framvegis.  

Útfluttar færslur innihalda eftirfarandi reiti: **Reikningur nr.**, **Bókunardags.** og **Upphæð**. Ef upplýsingar um víddir voru líka fluttar út, eru víddarkóðar og víddargildi þar á meðal.  

1. Ef samtala reitanna **Upphæð** er debet er reikningsnúmerið sem sett er upp í reitnum **Samstæðu-debetreikn.** í fyrirtækiseiningunni flutt út í línuna fyrir hverja útflutta línu. Ef samtalan er kredit er samsvarandi númer í reitnum **Samstæðu-kreditreikn.** flutt út í línuna.  
2. Sú dagsetning sem er notuð fyrir útfluttar línu er annaðhvort lokadagsetning tímabils eða sú dagsetning þegar útreikningur fer fram.  
3. Víddargildið sem flutt er út fyrir færsluna verður víddargildi samsteypufyrirtækisins sem sett er upp í reitnum **Kóti samstæðu** fyrir það víddargildi. Ef ekkert víddargildi samsteypufyrirtækis hefur verið fært inn í reitinn **Sameinaður kóti** fyrir þetta víddargildi er víddargildið sjálft flutt út í línuna.   
4. Auk þess innihalda XML-skrárnar gengi gjaldmiðils innan samsteyputímabilsins. Þessi gengi eru innifalin í aðskildum hluta í upphafi skrárinnar.

## <a name="see-also"></a>Sjá einnig
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)

