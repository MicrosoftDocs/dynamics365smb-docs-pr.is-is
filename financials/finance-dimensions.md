---
title: "Vinna með Víddir| Microsoft Docs"
description: "Nota skal víddir til að flokka færslur, til dæmis eftir deild eða verki, svo hægt sé að rekja og greina gögn auðveldlega."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b7b69b3419520c482cbe6a84494bbac7ef35bea1
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="working-with-dimensions"></a>Unnið með víddir
Til að auðvelda greiningu á skjölum, svo sem sölupöntum, geturðu notað stærðir. Víddir eru eiginleikar og gildi sem flokkar færslur svo þú getir fylgst með og greina þær. Til dæmis má vísa til verkefnisins eða deildarinnar sem innganga kom frá.  

Til dæmis, í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað stærðir. Þetta gefur mikið tækifæri til greininga án þess að búa til flókið kort af reikningum. Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).

Annað dæmi er að setja upp vídd sem kallast *Deild* og nota þá vídd þegar þú bókar söluskjöl. Þetta mun leyfa þér að nota viðskipti upplýsingaöflun tól til að sjá hvaða deild selt hvaða atriði.
Því fleiri stærðir sem þú notar, nákvæmari skýrslurnar sem þú getur byggt á viðskiptatengslunum þínum. Til dæmis getur einn sölutilgangur innihaldið upplýsingar um marga vídd, svo sem:  

* Reikningurinn sem vörusalan var sendur til  
* Þar sem hluturinn var seldur
* Hver seldi það
* Tegund viðskiptavina sem keypti hana  

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Greining eftir víddum
Virkni víddarinnar gegnir mikilvægu hlutverki í viðskiptaupplýsingum, eins og t.d. þegar verið er að skilgreina greingaryfirlit. Frekari upplýsingar, sjá [Hvernig skal: Greina gögn eftir víddum](bi-how-analyze-data-dimension.md).

## <a name="dimension-sets"></a>Víddasamstæður
Víddasamstæða er sérstök samsetning víddargilda. Er vistað sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.  

Þegar þú býrð til dagbókarlínu, skjalhaus eða skjalastiku, getur þú tilgreint samsetningu af víddarmörkum. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

## <a name="setting-up-dimensions"></a>Uppsetning vídda
Hægt er að skilgreina víddirnar og víddargildin til að flokka færslubókum og skjölum, t.d. sölupantanir og innkaupapantanir. Þú setur upp víddir í **Víddir** glugganum, þar sem búin er til ein lína fyrir hverja vídd, svo sem *Verkefni*, *Deild*, *Svæði*, og *Sölumaður*.

Þú setur einnig upp gildi fyrir víddir. Gildi gætu til dæmis verið deildirnar í fyrirtækinu. Hægt er að setja víddir upp í stigveldisröð, svipað og bókhaldslykilinn, svo að hægt verði að stigskipta gögnunum og taka saman milliniðurstöður. Hægt er að skilgreina eins margar víddir og víddargildi og þörf er á og allir í fyrirtækinu geta notað þau.

Einnig er hægt að setja upp altækar víddir og flýtivísanir í víddir:  

* **Altækar víddir** eru notaðar sem afmarkanir, t.d. á skýrslur og runuvinnslur. Hægt er að nota eingöngu tvær altækar víddir, svo veldu því víddir sem verða notaðar oft.
* **Flýtivísanir í víddir** eru tiltækar sem reitir í færslubókar- og fylgiskjalslínum. Hægt er að stofna allt að sex af þeim.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Setja upp sjálfgefnar víddir fyrir viðskiptavinir, lánardrottinn, og aðra reikninga
Hægt er að setja upp sjálfgefna vídd fyrir tiltekinn stakan reikning. Víddin verður afrituð í færslubókina eða fylgiskjalið þegar reikningsnúmerið er fært inn í línu, en hægt er að eyða eða breyta kóðanum í línunni ef það á við. Einnig er hægt að búa til vídd og krefjast þess að í henni þurfi að bóka færslu með ákveðinni tegund reiknings.  

### <a name="translating-the-names-of-dimensions"></a>Þýða nöfn vídda
Þegar stofnuð er vídd og sérstaklega flýtivísun í vídd, er í raun verið að stofna er hefðbundinn reit eða dálkafyrirsögn. Ef fyrirtækið er alþjóðlegt má bjóða upp á þýðingar á heiti víddarinnar. Skjöl sem innihalda víddina munu nota þýdda heitið þar sem við á.   

### <a name="example-of-dimension-setup"></a>Dæmi um uppsetningu víddar
Segjum sem svo, að fyrirtækið vilji rekja færslur út frá skipulagseiningum og landfræðilegum staðsetningum. Til þess að gera það, er hægt að setja upp tvær víddir í **Víddir** glugganum:

* **SVÆÐI**  
* **DEILD**  

| Kóði | Name | Texti kóta | Texti afmörkunar |
| --- | --- | --- | --- |
| SVÆÐI |Svæði |Svæðiskóði |Svæðisafmörkun |
| DEILD |Deild |Deildarkóði |Afmörkun deildar |

Fyrir **SVÆÐI**, skal bæta við eftirfarandi víddargildum:

| Kóði | Name | Tegund víddargildis |
| --- | --- | --- |
| 10 |Suður-, Mið- og Norður-Ameríka |Frá-tala |
| 2.0 |Norður-Ameríka |Staðlað |
| 30 |Kyrrahafið |Staðlað |
| 40 |Suður-Ameríka |Staðlað |
| 50 |Norður- og Suður-Ameríka, Samtals |Til-tala |
| 60 |Evrópa |Frá-tala |
| 70 |ESB |Staðlað |
| 80 |Utan-ESB |Staðlað |
| 90 |Evrópa, Samtals |Til-tala |

Fyrir tvö helstu landsvæðin, N- og S-Ameríku og Evrópu, skal bæta við undirflokkum fyrir svæði með því að draga inn víddargildin. Þetta gera notanda kleift að tilkynna á sölu- eða kostnað í svæðum og fá samtölur fyrir stærri landfræðileg svæði. Einnig er væri hægt að velja að nota lönd og svæðum sem víddargildi, eða sýslur og borgir, það fer eftir gerð fyrirtækisins.  
> [!NOTE]  
>   Til að setja upp stigveldi verða kóðarnir að vera í stafrófsröð. Þar á meðal eru kóðarnir fyrir víddargildin sem eru fengin í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Fyrir **DEILD**, skal bæta við eftirfarandi víddargildum:

| Kóði | Name | Tegund víddargildis |
| --- | --- | --- |
| STJÓRN |Stjórnun |Staðlað |
| FRAML |Framleiðsla |Staðlað |
| SALA |Sala |Staðlað |

Með þessa uppsetningu, skal síðan bæta við þínum tveimur víddum sem hinum tveimur altæku víddum í glugganum **Uppsetning Fjárhagsgrunns**. Þetta þýðir að hægt er að nota SVÆÐI og DEILD sem afmarkanir á fjárhagsfærslur og einnig á allar skýrslur og fjárhagsáætlanir. Báðar altæku víddirnar eru líka sjálfkrafa tiltækar til notkunar á færslulínum og skjalahausum sem flýtivísanir í víddir.  

## <a name="using-dimensions"></a>Notkun vídda
Í skjalinu eins og sölupöntun, er hægt að bæta við víddaupplýsingum fyrir bæði einstaka fylgiskjalslínu og skjalið sjálft. Til dæmis, í **Sölupöntun** glugganum getur þú slegið inn víddarmörk fyrir fyrstu tvær flýtivísanirnar á einstökum sölulínum og þú getur bætt við stærri víddarupplýsingum ef þú velur hnappinn **Víddir**.  

Ef þú vinnur í dagbók í staðinn geturðu bætt við víddargögn við færslu á sama hátt ef þú hefur sett upp flýtileiðarmörk sem reitir beint á blaðalínum.  

Hægt er að setja upp sjálfgefnar víddir fyrir reikninga eða reikningstegundir, svo að víddir og víddargildi eru fyllt út sjálfkrafa.  

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

