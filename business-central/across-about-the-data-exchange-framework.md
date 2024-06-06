---
title: Um gagnaskiptaramma
description: Þessi grein útskýrir hvernig á að nota Data Exchange Framework til að halda utan um skipti á gögnum í viðskiptaskjölum eins og reikningum með viðskiptafélögum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="about-the-data-exchange-framework"></a>Um gagnaskiptaramma

Hægt er að nota Data Exchange Framework til að stjórna skiptum á viðskiptaskjölum, bankaskrám, gengi gjaldmiðla og öllum öðrum gögnum á milli viðskiptafélaga eða yfirvalds.

Sem kerfisstjóri eða Microsoft-samstarfsaðili er hægt að nota rammann í nýjum samþættingaraðgerðum með því að setja upp hvaða gögn á að skiptast á og hvernig. Til dæmis er skráasnið fyrir skipti á gögnum sem er að finna í bankaskrám, rafrænna skráa, gengi gjaldmiðla, og annarra með ERP-kerfi breytilegt eftir birgi gagnaskráarinnar eða straumsins og eftir landi/svæði. [!INCLUDE[prod_short](includes/prod_short.md)] styður ýmis skráarsnið fyrir bankaskrár og gagnaþjónustustaðla. Til að veita stuðning á öðrum rafrænu formi er notaður gagnaskiptarammi.

 Eftirfarandi skýringarmyndir sýna arkitektúr gagnaskiptarammans.  

 ![Gagnaskiptarammi &#45; Innflutningur.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Gagnaskiptarammi &#45; Útflutningur.](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents"></a>Rafræn skjöl

Önnur leið til að senda viðskiptaskjöl sem skráarviðhengi er að senda og taka á móti þeim rafrænt. „Rafrænt skjal“ er stöðluðu skrá sem stendur fyrir viðskiptaskjal, s.s. reikning frá lánardrottni sem hægt er að taka á móti og umbreyta í innkaupareikning í [!INCLUDE[prod_short](includes/prod_short.md)]. Viðskiptafélagar skiptast á rafrænum skjölum gegnum ytri skjalaskiptaþjónustu. [!INCLUDE[prod_short](includes/prod_short.md)] styður sjálfgefið sendingu og móttöku rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er stutt af stærstu skjalaskiptaþjónustukerfunum. Stór þjónustuveitandi skjalaskiptaþjónustu, Tradeshift, er forstilltur og tilbúinn til uppsetningar fyrir fyrirtækið. Til að veita stuðning fyrir önnur snið rafrænna skjala þarf að stofna nýjar skilgreiningar gagnaskipta.  

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[prod_short](includes/prod_short.md)], rétt eins og með rafræn PEPPOL-skjöl. Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu af síðunni **Skjöl á innleið**. Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin. Ef skráin er send í OCR-þjónustu með tölvupósti er ný færsla fyrir skjal á innleið sjálfkrafa stofnum þegar tekið er aftur á móti rafræna skjalinu.  

Til að senda, til dæmis, sölureikning sem rafrænt PEPPOL-skjal skal velja sem **Rafrænt skjal** valkostinn í á **Bóka og senda** svargluggi. Héðan er hægt að einnig setja upp sjálfgefna forstillingu skjalasendingar viðskiptamanns. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og atriði þegar gögnum er umbreytt í reiti í [!INCLUDE[prod_short](includes/prod_short.md)] í einingar í skjalaskrá á útleið. Gagnaumreikningurinn og sending á PEPPOL-sölureikningum eru framkvæmdar af tilteknum kóðaeiningum og XMLports, táknað með **PEPPOL** rafræna skjalasniðinu.  

Til dæmis, til að taka á móti reikningur frá lánardrottinn sem rafrænu PEPPOL-skjali er skjalið unnið á síðunni **Skjöl á innleið** til að breyta því í innkaupareikningi í [!INCLUDE[prod_short](includes/prod_short.md)]. Það er annaðhvort hægt að setja upp verkraðareiginleika til að vinna reglulega úr slíkum skjölum eða hægt er að ræsa ferlið handvirkt. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, lánardrottna, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og atriði þegar gögnum í einingum í skjalaskrá á innleið.er umbreytt í reiti í [!INCLUDE[prod_short](includes/prod_short.md)]. Móttaka og gagnaumbreyting PEPPOL-reikninga er framkvæmt af gagnaskiptaumgjörðinni sem stendur fyrir gagnaskiptaskilgreiningu **PEPPOL - Reikningur**.  

  Til að taka við, til dæmis, reikningi sem rafrænu OCR-skjali, er það meðhöndlað líkt og þegar rafrænt PEPPOL-skjal er móttekið. Móttaka og gagnaumbreyting rafrænna reikninga úr OCR er framkvæmt af gagnaskiptaumgjörðinni sem stendur fyrir gagnaskiptaskilgreiningu **PEPPOL - Reikningur**.  

## <a name="bank-files"></a>Bankaskrár

Skráasnið fyrir skipti bankagagna með viðskiptastjórnunarforritum er breytilegt eftir birgi skráarinnar og landi eða svæði. [!INCLUDE[prod_short](includes/prod_short.md)] styður innflutning og útflutning bankaskráa sameiginlegs evrópsks greiðslusvæðis (SEPA). Auk þess gerir AMC Banking 365 Fundamentals viðbótin þér kleift að tengjast AMC Banking 365 Fundamentals viðbót sem ytri þjónustuaðili, AMC Consult, býður þér upp á. Frekari upplýsingar er að finna í [Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Til að veita stuðning á öðrum rafrænu formi er notað Data Exchange Framework.  

Til að flytja út kreditfærslur SEPA skal velja hnappinn **Flytja greiðslur út í skrá** á síðunni **Greiðslubók** og hlaða svo upp skránni til að vinna úr greiðslunum í bankanum. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. bankareikning, lánardrottna og greiðslumáta. Gagnaumreikningurinn og útflutningur á SEPA-bankagögnum eru framkvæmdar af þartilgerðum codeunit og XMLport, táknað með **SEPA-kreditfærsla** bankauppsetningu innflutningur/útflutningur. Að öðrum kosti er hægt að setja upp viðbótina AMC Banking 365 Fundamentals og láta hana sjá um útflutninginn, táknað með **AMC Banking 365 Fundamentals viðbót - Kreditfærsla** gagnaskiptaskilgreiningu.  

 Til að flytja út leiðbeiningar fyrir SEPA-beingreiðslur skal velja hnappinn **Flytja út beingreiðsluskrá** á síðunni **Innheimta beingreiðslu** og senda hana svo í bankann til að innheimta sjálfkrafa umræddar greiðslur viðskiptamanns. Fyrst þarf að setja upp bankareikninga, lánardrottna, umboð fyrir beingreiðslu og greiðslumáta. Gagnaumreikningurinn og útflutningur á SEPA-bankagögnum eru framkvæmdar af þartilgerðum codeunit og XMLport, táknað með **SEPA-beingreiðsla** bankauppsetningu innflutningur/útflutningur.  

 Til að flytja inn SEPA-bankayfirlit skal velja hnappinn Flytja inn bankayfirlit á síðunni **Greiðsluafstemmingarbók** og **Bankareikn. Afstemming** og halda svo áfram og leggja fram hverja bankayfirlitsfærslu til greiðslu eða í fjárhagsfærslur, handvirkt eða sjálfkrafa. Fyrst þarf að setja upp bankareikninga. Innflutningur og gagnaumbreyting SEPA-bankagagna er framkvæmt af gagnaskiptaumgjörðinni sem stendur fyrir gagnaskiptaskilgreiningu **SEPA CAMT**. Að öðrum kosti er hægt að setja upp AMC Banking 365 Fundamentals viðbótina og látið hana sjá um innflutninginn, táknað með **AMC Banking 365 Fundamentals viðbót - Bankayfirlit** gagnaskiptaskilgreiningu.  

 Auk þess styðja staðbundnar útgáfur [!INCLUDE[prod_short](includes/prod_short.md)] ýmis önnur skráarsnið fyrir innflutning og útflutning á bankagögnum, launafærslum og öðrum gögnum. Frekari upplýsingar er að finna á lendingarsíðunni [Staðbundin virkni](about-localization.md) fyrir landið/svæðið þitt í hjálparefninu.  

## <a name="currency-exchange-rates"></a>Gengi gjaldmiðla

Hægt er að setja upp ytri þjónusta til að gæta þess að gengi gjaldmiðils sé rétt. Þjónustan sem veitir uppfært gengi gjaldmiðils er virk af skilgreiningu gagnaskipta. Til samræmis er síðan **Uppsetningarspjald fyrir uppfærslu gengis** samantekið yfirlit síðunnar **Gagnaskiptaskilgreining** fyrir skilgreiningu gagnaskipta sem um ræðir.  

Fyrir öll gagnaskipti í XML-skrám er hægt að undirbúa gagnaskiptauppsetninguna með því að hlaða tengdum XML-skemaskrám á síðunni **XML-skemaskoðun**. Hér eru fyrst valin gagnastökin sem á að skiptast á við [!INCLUDE[prod_short](includes/prod_short.md)] og svo skal annaðhvort hefja gagnaskiptiskilgreiningu eða mynda XMLport.

## <a name="intrastat"></a>Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] notar Data Exchange Framework fyrir Intrastat-skýrslugerð þar sem þú getur auðveldlega búið til tímastimplaðar skrár á mismunandi sniði fyrir útflutning. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur útbúin snið fyrir staðfærð lönd/svæði og sjálfgefna útgáfu. En þú getur breytt tilbúinni skýrslu eða gert þína eigin.

## <a name="see-also"></a>Sjá einnig .

[Rafræn gagnaskipti](across-data-exchange.md)  
[Nota XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
