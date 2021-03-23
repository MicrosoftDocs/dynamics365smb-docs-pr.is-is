---
title: Skila inn VSK-skýrslum til skattayfirvalda | Microsoft Docs
description: Kynntu þér hvernig skal undirbúa skýrslu sem telur upp VSK-upphæðir af sölu yfir ákveðið tímabil, eða fyrir sölu og innkaup, og senda hana til skattyfirvalda.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 4b2736459372d53eb026c061ed5663f8adc772ad
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388075"
---
# <a name="report-vat-to-tax-authorities"></a>Senda VSK skýrslu inn til skattayfirvalda
Þetta efnisatriði lýsir skýrslunum í [!INCLUDE[prod_short](includes/prod_short.md)] sem þú getur notað til að senda inn upplýsingar um virðisaukaskatt (VSK) upphæðir fyrir sölu og innkaup til skattayfirvalda á þínu svæði. 

Hægt er að nota eftirfarandi skýrslur :

* Í **Sölulisti EC** Evrópubandalag (EC) söluyfirlitsskýrslu eru listar yfir VSK-upphæðir sem þú hefur safnað upp fyrir sölu til VSK-skráðra viðskiptamanna innan landa Evrópusambandsins (EU).  
* **VSK skil** skýrslan inniheldur VSK fyrir sölu og innkaup til viðskiptamanna og frá lánardrottnum í öllum löndum sem notast við VSK.

Ef þú vilt skoða allan feril VSK færslna, þá býr hver VSK-bókun til færslu á **VSK-færslur** síðunni. Þessar færslur eru notaðar til að reikna VSK-upphæðir s.s. greiðslur og endurgreiðslur á tilteknu tímabili. Til að skoða VSK-færslur veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **VSK-færslur** og veldu síðan tengda hlekkinn.

> [!NOTE]
> Hverju [!INCLUDE[prod_short](includes/prod_short.md)] umhverfi er ætlað að halda utan um eftirlitsskýrslugerð í einu landi. Hollenska útgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] sér til dæmis um VSK-skýrslugerð í Hollandi en ekki í öðrum löndum. Á sama hátt höndlar útgáfa í Bandaríkjunum [!INCLUDE[prod_short](includes/prod_short.md)] 1099 skýrslugerð í Bandaríkjunum og styður ekki VAT skýrslur í öðrum löndum, nema með viðbót sem umhverfi samstarfsaðila þíns eða breytingu á kóða tiltekins viðskiptavinar.

## <a name="about-the-ec-sales-list-report"></a>Um EC söluyfirlitsskýrslu
Í Bretlandi þurfa öll fyrirtæki sem selja vörur og þjónustu fyrir meira en tiltekna upphæð á ári hverju til VSK skráðra viðskiptavina, líka þeirra sem eru í öðrum löndum innan ESB, að skila inn rafrænni söluyfirlitsskýrslu Evrópubandalaga (EC) á XML formi í gegnum vefsíðu þarlendra skattayfirvalda (HMRC). Söluyfirlitsskýrsla Evrópubandalaga (EC) virkar aðeins í löndum innan ESB.

Skýrslan inniheldur eina línu fyrir hverja tegund af viðskiptum við viðskiptavini, og sýnir heildarupphæð fyrir hverja tegund viðskipta. Hægt er að skrá þrjár gerðir viðskipta í skýrslunni:  

* B2B vörur  
* B2B þjónusta  
* B2B Þríhliða vörur  

B2B vörur og þjónusta tiltaka hvort þú seldir vörur eða þjónustu, og sért undir stjórn stillingarinnar **ESB Þjónusta** í uppsetningu bókunar á VSK. B2B Þríhliða vörur gefa það til kynna hvort þú stundaðir viðskipti við þriðja aðila og sért undir stjórn stillingarinnar **ESB þríhliða viðskipti** í söluskjölum, eins og sölupantanir, reikningar, kreditreikningar osfrv.  

Eftir að skattayfirvöld fara yfir skýrsluna, munu þau senda tengilið fyrirtækisins tölvupóst. Í [!INCLUDE[prod_short](includes/prod_short.md)] er tengiliðurinn tiltekinn á síðunni **Upplýsingar um fyrirtækið**. Áður en þú sendir inn skýrsluna skaltu vera viss um að tengiliður hafi verið valinn.

## <a name="about-the-vat-return-report"></a>Um skýrsluna um VSK skil
Nota þessa skýrslu til að skila inn VSK fyrir sölu- og innkaupaskjöl, eins og innkaupa- og sölupantanir, reikninga og kreditreikninga. Upplýsingarnar koma fram með sama sniði í skýrslunni og á skýrslublaði frá tolla- og skattayfirvöldum.  

VSK er reiknaður á grundvelli VSK-bókunargrunnur og VSK-bókunarflokkum sem settir hafa verið upp.

Fyrir VSK skilin geturðu tiltekið hvaða færslur skuli teknar með:

* Senda inn aðeins opnar færslur, eða opnar og lokaðar. Til dæmis, þetta er gagnlegt þegar verið er að undirbúa hin árlegu VSK lokaskil.
* Tilgreinir hvort á að taka með VSK-færslur aðeins fyrir tilgreint tímabil eða einnig frá fyrri tímabilum innan tilgreinds árs. Þetta er gagnlegt fyrir uppfærslu VSK skila sem þú hefur þegar sent inn, til dæmis, ef lánardrottin sendir þér síðbúinn reikning.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Til að tengjast vefþjónustu skattayfirvalda býður
[!INCLUDE[prod_short](includes/prod_short.md)] býður upp á þjónustutengingar sem tengjast við vefsíður skattayfirvalda. Ef þú ert t.d. í Bretlandi, er hægt að virkja **GovTalk** þjónustutenginguna til að senda inn EC Sölulista og VSK skýrslum rafrænt. Ef þú vilt senda skýrsluna inn handvirkt, til dæmis með því að færa gögnin inn á vefsíðu skattayfirvalda, er það ekki nauðsynlegt.   

Til að skila VSK til skattayfirvalda á rafrænu formi, þarf að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við vefþjónustu skattayfirvalda. Til þess þarf að setja upp reikning hjá þínum skattayfirvöldum. Þegar þú ert komin(n) með reikning, geturðu virkjað þjónustutengingu sem við bjóðum upp á í [!INCLUDE[prod_short](includes/prod_short.md)].

1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustutengingar** og veldu síðan viðeigandi tengil.
2. Fylltu út nauðsynlega reiti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Ráðlegt er að er að prófa tenginguna. Til að gera það skal velja **Prufustilling** gátreitinn, svo undirbúa og senda inn VSK skýrslurnar eins og lýst er í _Að undirbúa og senda inn VSK skýrslu_ hlutanum. Þegar þjónustan er á Prufustillingu, prófar hún hvort skattayfirvöld geti tekið á móti skýrslunni, og staðan á skýrslunni mun gefa til kynna hvort prufuinnsendingin hafi heppnast. Mikilvægt er að muna að þetta er ekki raunveruleg innsending. Ef senda á skýrsluna inn í raun, þarf að að hreinsa gátreitinn **Prufustilling** og endurtaka innsendingarferlið.

## <a name="to-set-up-vat-reports-in-prod_short"></a>Að setja upp VSK-skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **VSK-skýrsluuppsetning** og veldu síðan tengda tengilinn.  
2. Ef þú vilt láta notendur breyta og endursenda skýrsluna, veldu þá gátreitinn **Breyta innsendum skýrslum**.  
3. Númeraröðin sem á að nota fyrir hverja skýrslu er valin.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Undirbúa og senda inn VSK-skýrslu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **EB-söluyfirlit** eða **VSK skil** og veldu síðan tengda tengilinn.  
2. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að útbúa efni skýrslunnar, veljið aðgerðina **Leggja til línur**.  

    > [!NOTE]  
    >   Hægt er að endurskoða færslurnar varðandi EC söluyfirlit, sem eru innifaldar í skýrslulínunni, áður en þú skilar inn skýrslunni. Til að gera það, skaltu velja línuna og svo aðgerðina **Sýna VSK færslur**.  
4. Til að staðfesta og undirbúa skýrsluna til innsendingar skal velja aðgerðina **Losa**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] staðfestir hvort skýrslan sé rétt sett upp. Ef staðfestingin mistekst, eru villurnar sýndar í **Villur og viðvaranir** svo hægt sé að gera viðeigandi breytingar. Ef skilaboðin snúast um stillingu sem vantar í [!INCLUDE[prod_short](includes/prod_short.md)], geturðu smellt á skilaboðin til að opna síðuna sem inniheldur upplýsingarnar sem þarf að leiðrétta.  
5. Til að senda skýrsluna inn skal velja aðgerðina **Innsending**.  

Eftir að þú skilar inn skýrslunni, fylgist [!INCLUDE[prod_short](includes/prod_short.md)] með þjónustunni og heldur skrá yfir samskipti þín. Reiturinn **Staða** gefur til kynna hvar skýrslan er stödd í ferlinu. Þegar t.d. yfirvöld fara yfir skýrsluna, breytist staða skýrslunnar yfir í **Heppnaðist**. Ef skattayfirvöld finna mistök í skýrslunni sem þú sendir þeim, mun staða skýrslunnar breytast yfir í **Mistókst**. Þú getur skoðað villur undir **Villur og viðvaranir**, leiðrétt þær og svo sent skýrsluna inn aftur. Til að skoða allar EC söluyfirlitsskýrslur þínar, farðu á **EC söluyfirlitsskýrslur** síðuna.  

## <a name="viewing-communications-with-your-tax-authority"></a>Skoða samskipti við skattayfirvöld
Í sumum löndum er skipst á skilaboðum við skattayfirvöld þegar skýrslur eru sendar inn. Hægt er að skoða fyrstu og síðustu skilaboðin sem voru send eða móttekin með því að velja aðgerðirnar **Hala niður innsendingarskilaboðum** og **Hala niður svarskilaboðum**.  

## <a name="submitting-vat-reports-manually"></a>Sendir inn VSK-skýrsla handvirkt
Ef þú notast við aðra aðferð til að senda skýrsluna inn, t.d. með því að flytja út XML og hlaða því svo upp á vefsíðu skattayfirvalda, geturðu eftir á valið **Merkja sem Búið að skila** til að loka skýrslutímabilinu. Eftir að þú merkir skýrsluna sem Búið að skila, er ekki hægt að breyta henni. Ef breyta þarf skýrslunni eftir að hún hefur verið merkt sem útgefin þarf fyrst að enduropna hana.

## <a name="vat-settlement"></a>VSK-uppgjör
Reglulega þarf að greiða nettó-VSK til skattayfirvalda. Ef þú þarft að gera upp VSK oft, er hægt að nota keyrsluna **Reikna og bóka VSK-uppgjör** til að loka opnum VSK-færslum og flytja VSK-upphæðir innkaupa og sölu í VSK-uppgjörsreikning.

Þegar þú færir VSK-upphæðir inn á uppgjörsreikninginn, eru VSK-upphæðirnar sem reiknaðar voru á yfirlitstímabilinu lagðar inn á reikning innskatts og teknar út af reikningi útskatts. Nettóupphæðin er lögð inn eða tekin út, ef innskattsupphæðin er hærri, á VSK-uppgjörsreikninginn. Hægt er að bóka uppgjörið strax eða prenta prófunarskýrslu fyrst.  

> [!Note]
> Ef þú tiltekur ekki **VSK Viðskiptabókunarflokkur** og **VSK Vörubókunarflokkur** þegar notuð er **Reikna út og bóka VSK Uppgjör** runuvinnslan, munu færslur með öllum viðskiptabókunarflokkur og vörubókunarflokkur kóðar teknir með.

## <a name="configuring-your-own-vat-reports"></a>Grunnstilla þínar eigin VSK skýrslur
Hægt er að nota EC Yfirlitsskýrslu sem kemur tilbúin, en líka er hægt að búa til sína eigin skýrslu. Til þess þarftu að stofna nokkrar kóðaeiningar. Ef þú þarft aðstoð við það, hafðu samband við Microsoft tengilið.  

Eftirfarandi tafla lýsir kóðaeiningunum sem þú þarft að stofna fyrir skýrsluna þína.

| Codeunit | Það sem hún þarf að gera |
|----|-----|
|Tillögulínur| Ná í upplýsingar frá VSK færslutöflunni og birta þær í línum VSK skýrslunnar.|
|Efni | Stjórna sniði skýrslunnar. Til dæmis hvort þú notar XML eða JSON. Gerð sniðs sem á að nota fer eftir skilyrðum vefþjónustu skattayfirvalda. |
|Sending | Stjórnaðu því hvernig og hvenær þú sendir inn skýrsluna, með tilliti til skilyrða skattayfirvalda. |
|Svarstjóri | Stýra skilum frá skattayfirvöldum. Þau gætu t.d. sent tengilið fyrirtækisins tölvupóst. |
|Hætta við | Senda inn afturköllun VSK skýrslu sem var send inn áður til skattayfirvalda. |  

> [!Note]
> Þegar stofnaðar eru kóðaeiningar fyrir skýrsluna skal veita gildinu athygli í reitnum **VSK skýrsla útgáfa**. Þessi reitur verður að endurspegla útgáfuna af skýrslunni sem er eða var send til skattayfirvalda. Þú gætir til dæmis fært inn **2017** í reitinn til að gefa til kynna að skýrslan samræmist þeim kröfum sem voru í gildi það ár. Til að finna núgildandi útgáfu skal hafa samband við skattayfirvöld.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]