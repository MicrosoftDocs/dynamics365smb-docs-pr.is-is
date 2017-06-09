---
title: "Uppsetning Vídda | Microsoft Docs"
description: "Hægt er að skilgreina víddirnar og víddargildin sem á að nota til að flokka færslubókum og skjölum, t.d. sölupantanir og innkaupapantanir."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Uppsetning vídda
Hægt er að skilgreina víddirnar og víddargildin til að flokka færslubókum og skjölum, t.d. sölupantanir og innkaupapantanir. Þú setur upp víddir í **Víddir** glugganum, þar sem búin er til ein lína fyrir hverja vídd, svo sem *Verkefni*, *Deild*, *Svæði*, og *Sölumaður*.

Þú setur einnig upp gildi fyrir víddir. Gildi gætu til dæmis verið deildirnar í fyrirtækinu. Hægt er að setja víddir upp í stigveldisröð, svipað og bókhaldslykilinn, svo að hægt verði að stigskipta gögnunum og taka saman milliniðurstöður. Hægt er að skilgreina eins margar víddir og víddargildi og þörf er á og allir í fyrirtækinu geta notað þau.

Einnig er hægt að setja upp altækar víddir og flýtivísanir í víddir:  

* **Altækar víddir** eru notaðar sem afmarkanir, t.d. á skýrslur og runuvinnslur. Hægt er að nota eingöngu tvær altækar víddir, svo veldu því víddir sem verða notaðar oft.
* **Flýtivísanir í víddir** eru tiltækar sem reitir í færslubókar- og fylgiskjalslínum. Hægt er að stofna allt að sex af þeim.  

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Setja upp sjálfgefnar víddir fyrir viðskiptavinir, lánardrottinn, og aðra reikninga
Hægt er að setja upp sjálfgefna vídd fyrir tiltekinn stakan reikning. Víddin verður afrituð í færslubókina eða fylgiskjalið þegar reikningsnúmerið er fært inn í línu, en hægt er að eyða eða breyta kóðanum í línunni ef það á við. Einnig er hægt að búa til vídd og krefjast þess að í henni þurfi að bóka færslu með ákveðinni tegund reiknings.  

## <a name="translate-the-names-of-dimensions"></a>Þýða nöfn vídda
Þegar stofnuð er vídd og sérstaklega flýtivísun í vídd, er í raun verið að stofna er hefðbundinn reit eða dálkafyrirsögn. Ef fyrirtækið er alþjóðlegt má bjóða upp á þýðingar á heiti víddarinnar. Skjöl sem innihalda víddina munu nota þýdda heitið þar sem við á.   

## <a name="example"></a>Dæmi
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
**Athugið**: Til að setja upp stigveldi verða kóðarnir að vera í stafrófsröð. Þar á meðal eru kóðarnir fyrir víddargildin sem eru fengin í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Fyrir **DEILD**, skal bæta við eftirfarandi víddargildum:

| Kóði | Name | Tegund víddargildis |
| --- | --- | --- |
| STJÓRN |Stjórnun |Staðlað |
| FRAML |Framleiðsla |Staðlað |
| SALA |Sala |Staðlað |

Með þessa uppsetningu, skal síðan bæta við þínum tveimur víddum sem hinum tveimur altæku víddum í glugganum **Uppsetning Fjárhagsgrunns**. Þetta þýðir að hægt er að nota SVÆÐI og DEILD sem afmarkanir á fjárhagsfærslur og einnig á allar skýrslur og fjárhagsáætlanir. Báðar altæku víddirnar eru líka sjálfkrafa tiltækar til notkunar á færslulínum og skjalahausum sem flýtivísanir í víddir.  

Með þessari uppsetningu má hefjast handa við að bæta víddum við skjöl og færslubækur. Frekari upplýsingar má finna í [Víddir](finance-dimensions.md).  

## <a name="see-also"></a>Sjá einnig
[Víddir](finance-dimensions.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

