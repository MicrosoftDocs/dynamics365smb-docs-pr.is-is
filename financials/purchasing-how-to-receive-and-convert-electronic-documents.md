---
title: "Taka við og umbreyta rafrænum skjölum | Microsoft Docs"
description: "Þú getur fengið rafræn skjöl beint frá viðskiptafélögum eða frá OCR þjónustu."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 8ae02f7a55f822751ae66b5b62013455aac87e48
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-receive-and-convert-electronic-documents"></a>Hvernig á að: Taka við pg umbreyta rafræn skjölum
Almenn útgáfa [!INCLUDE[d365fin](includes/d365fin_md.md)] styður sendingu rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er stutt af stærstu skjalaskiptaþjónustukerfunum. Til að taka á móti reikningur frá lánardrottinn sem rafrænu PEPPOL-skjali er skjalið unnið í glugganum Fylgiskjal á innleið til að breyta því í innkaupareikning eða almenna færslubókarlínu í [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Auk þess að fá rafræn skjöl beint úr viðskiptafélögum geturðu fengið rafræn skjöl frá OCR þjónustu sem hefur breytt PDF eða myndskrá í rafræn skjöl.  

 Áður en hægt er að taka við rafrænum skjölum gegnum skjalaskiptaþjónustu þarf fyrst að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, lánardrottna, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og atriði þegar gögnum er umbreytt í reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)] í einingar í skjalaskrá á innleið. Frekari upplýsingar, sjá [Hvernig á að setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md).  

 Áður en hægt er að taka við rafrænum skjölum gegnum OCR-þjónustu verður þú að setja upp og virkja almenna þjónustu tengingu. Nánari upplýsingar er að finna í [Hvernig á að setja upp skjöl á innleið](across-how-setup-income-documents.md).  

 Umferð rafrænna skjala í og ​​úr [!INCLUDE[d365fin](includes/d365fin_md.md)] er stjórnað af verkraðareiginleikanum. Áður en þú getur fengið rafræn skjöl þarf viðkomandi verkröð að hefjast.  

 Þú getur annað hvort byrjað umbreytingu á rafrænum skjölum handvirkt, eins og lýst er í þessari aðferð, eða virkjað verkflæði til að umbreyta rafrænum skjöl sjálfkrafa þegar þau berast. Almenn útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] verkflæðissniðmátið *Úr rafrænu skjali á innleið gegnum OCR í verkflæði opins innkaupareiknings*, sem afrita má í verkflæði og virkja. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
>  Þegar rafrænum skjölum sem koma úr OCR-þjónustu er breytt í skjöl eða færslubókarlínur í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður mörgum línum í upprunaskjalinu safnað saman í eina línu. Staka línan verður af gerðinni fjárhagsreikningur og **Lýsing** og **Nr.** (fjárhagsreiknings) reitir verða auðir. Gildið í reitnum **Upphæð** verður heildarupphæð, fyrir utan VSK, allra lína í upprunaskjalinu.  
>   
>  Til að vera viss um að reitirnir **Lýsing** og **nr.** hafi verið fylltir út geturðu valið hnappinn **Varpa texta á reikning** í glugganum **Fylgiskjöl á innleið** til að ákvarða að tilteknum reikningstexta sé alltaf varpað á tiltekinn debit- eða kreditreikning í fjárhagnum. Í framhaldinu verður reiturinn **Lýsing** í skjali eða færslubókarlínum sem stofnaður er úr rafrænu skjali fyrir þann lánardrottinn eða viðskiptamann fylltur út með viðkomandi texta og fjárhagsreikningurinn **Nr.** reiturinn með lyklinum.  
>   
>  Í stað þess að varpa á fjárhagsreikning er líka hægt að varpa á bankareikning. Þetta er hagkvæmt, til dæmis, fyrir rafræn skjöl tengd útgjöldum sem eru nú þegar greitt þegar þú vilt stofna færslubókarlíni sem er tilbúin til að bóka á bankareikning.  

 Eftirfarandi ferli lýsir því hvernig á að taka við lánardrottinsreikningi og breyta honum í staðlaðan innkaupareikning í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aðferðin er sú sama og þegar reikningi lánardrottins er breytt í færslubókarlínu.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Til að taka við og umbreyta rafrænum reikningi í innkaupareikning.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **skjöl á innleið** og velja svo viðeigandi tengil.  

2.  Velja línuna fyrir skjal á innleið sem táknar nýjan rafrænan reikning á innleið og svo, á flipanum **Heim** í hópnum **Stjórna** velja **Breyta**.  

     Í glugganum **Fylgiskjalsspjald á innleið** er tengd XML skrá fest við og flestir reitir forútfylltir með upplýsingum frá rafrænum reikningi. Frekari upplýsingar eru í [Hvernig á að stofna færslur fyrir skjal á innleið](across-how-create-income-document-records.md).  

3.  Í reitnum **Gaganskiptagerð** veljið **PEPPOL reikningur** eða **OCR - reikningur** eftir uppruna rafræna skjalsins.  

4.  Til að varpa texta á lánardrottinsreikningi á tiltekinn debetreikning skal, á flipanum **Aðgerðir** í flokknum **Almennt** velja **Varpa texta á reikning**, og fylla svo út gluggann **Vinnublað textavörpun á reikning**.  

5.  Á flipanum **Aðgerðir** í flokknum **Almennt** veljið **Stofna skjal**.  

     Innkaupareikningur verður stofnaður í [!INCLUDE[d365fin](includes/d365fin_md.md)] og byggist á upplýsingar í rafrænt skjal.  

     Allar villur við villuleit, sem tengjast gjarnan gölluðum eða skemmdum gögnum í [!INCLUDE[d365fin](includes/d365fin_md.md)], verða sýndar á flýtiflipanum **Villuboð**.  

## <a name="see-also"></a>Sjá einnig  
[Stjórna skuldum](payables-manage-payables.md)  
[Skjöl á innleið](across-income-documents.md)  
[Hvernig á að: Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Rafræn gagnaskipti](across-data-exchange.md)   
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

