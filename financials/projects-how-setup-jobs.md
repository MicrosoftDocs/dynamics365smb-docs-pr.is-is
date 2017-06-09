---
title: "Hvernig á að: setja upp verk| Microsoft Docs"
description: "Lýsir því hvernig á að undirbúa kerfið til að nota verk til að stjórna verkefnum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f228e520f1140243a6fd305173200ff5637272a5
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-jobs"></a>Hvernig á að setja upp verk
Í glugganum **Uppsetning verka** þarf að tilgreina hvernig eigi að nota tiltekin verk.

Á einstökum verkspjöldum þarf að setja upp verð fyrir vörur, forða og fjárhagsreikninga verks og setja þarf upp verkbókunarflokka.

## <a name="to-set-general-information-for-jobs"></a>Til að stilla almennar upplýsingar fyrir verk
1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Uppsetning verka**, og velja síðan viðeigandi tengil.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Til athugunar**: Gátreiturinn **Beita notkunartengli** er frekar flókinn og því er hann útskýrður í eftirfarandi hluta.

## <a name="to-set-up-job-usage-tracking"></a>Til að setja upp notkunarrakningu verka
Þegar verið er að framkvæma verk gæti verið gagnlegt að vita hvernig notkunin er rakin á móti áætluninni. Til að gera þetta á auðveldan hátt, er hægt að búa til tengil milli verkáætlunarlínunnar og hinnar eiginlegu notkunar. Þetta leyfir þér að rekja kostnað þinn og sjá auðveldlega hversu mikið af vinnu á eftir að vinna. Sjálfgefið er að áætlunarlína verktegundar sé **Áætlun**, en ef línutegundin **Bæði fjárhagsáætlun og reikningshæft** er notuð hefur það svipuð áhrif.

Ef hakað er í gátreitinn **Beita notkunartengli** er hægt að yfirfara upplýsingar um verkáætlunarlínuna. Hægt er að stilla magn forða, vöru eða fjárhagsreiknings og gefa svo upp hvaða magn á að færa í verkbókina. Í reitnum **Eftirstöðvar (magn)** í verkáætlunarlínunni sést hvað á eftir að flytja og bóka í verkbókina.

Þegar gátreiturinn **Nota notkunartengil** er valinn, og verkáætlunarlínugerðin er **Reikningshæft**, stofnar Financials verkáætlunarlínu af tegundinni **Áætlun** eftir að færslubókarlínan er bókuð.

**Til athugunar**: Ef gátreiturinn **Beita notkunartengli** er valinn á verkspjaldinu og reiturinn **Tegund línu** í verkbókinni er auður, eru nýjar verkáætlunarlínur af tegundinni **Áætlun** stofnaðar þegar verkáætlunarlínur eru bókaðar. Ef gátreiturinn **Beita notkunartengli** er ekki valinn á verkspjaldi og reiturinn **Tegund línu** í verkbókarlínunni er auður eru engar verkáætlunarlínur stofnaðar þegar verkbókarlínur eru bókaðar. Nánari upplýsingar eru í [Hvernig á að: Skrá notkun vegna verka](projects-how-record-job-usage.md).

1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Uppsetning verka**, og velja síðan viðeigandi tengil.
2. Veljið eða afveljið gátreitinn **Beita notkunartengli**.

**Til athugunar**: Hægt er að stilla gátreitinn **Beita notkunartengli** með ólíkum hætti fyrir einstök verkspjöld. Í slíkum tilvikum hnekkir stilling viðkomandi verks sjálfgefnum stillingum sem lýst er hér að ofan.

## <a name="to-set-up-prices-for-job-resources"></a>Til að setja upp verð fyrir verkforða
Sérstök verð má setja upp fyrir forða verks. Glugginn **Forðaverð verks** er notaður til þess.

1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verk**, og velja síðan viðeigandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Forði**.
3. Í glugganum **Forðaverð verks** skal fylla reitina út eins og þörf krefur.

Viðbótarupplýsingar í reitunum **Verkhlutanr.**, **Tegund vinnu**, **Gjaldmiðilskóti**, **Línuafsl. %** og **Stuðull einingarverðs** verða notaðar í verkáætlunarlínum og notkunarbókum þegar þessi forði er sleginn inn og honum bætt við verkið.  

Virðið í reitnum **Einingarverð** fyrir forðann verður notað í verkáætlunarlínum og verkbókum þegar þessi forði, forði sem úthlutað er á forðahóp, eða einhver annar forði er færður inn.  

**Til athugunar**: Þetta verð hnekkir ávallt öllu verði sem sett er fram í glugganum **Forðaverð eða forðaflokksverð**.

## <a name="to-set-up-prices-for-job-items"></a>Til að setja upp verð fyrir vörur verks
Sérstök verð má setja upp fyrir vörur verka. Glugginn **Verð verkvara** er notaður til þess.

1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verk**, og velja síðan viðeigandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Vara**.
3. Í glugganum **Vöruverð verks** skal fylla reitina út eins og þörf krefur.

Viðbótarupplýsingarnar í reitunum **Verkhlutanr.**, **Gjaldmiðilskóti** og **Línuafsl.** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi vara er slegin inn eða henni bætt við verk.  

Gildið í reitnum **Einingarverð** fyrir vöruna verður notað í verkáætlunarlínum og verkbókum þegar þessi vara er slegin inn.  

**Til athugunar**: Þetta verð hnekkir alltaf hefðbundnu viðskiptamannaverði („besta verði“) vöru. Ef nota skal hefðbundnar verðuppsetningar ætti ekki að stofna verð fyrir verkvöruna.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>að setja upp verð í fjárhagsreikningi fyrir verk
Hægt er að setja upp ákveðið verð fyrir fjárhagsleg útgjöld í verki. Glugginn **Verð fjárhagsreiknings verks** er notaður til þess.

1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verk**, og velja síðan viðeigandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Fjárhagsreikningur**.  
3. Í glugganum **Fjárhagsreikningsverð verks** skal fylla reitina út eins og þörf krefur.

Viðbótarupplýsingar í reitunum **Verkhlutanr.**, **Gjaldmiðilskóti**, **Línuafsl. %**, **Stuðull einingarverðs** og **Kostn.verð** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn og honum bætt við verk.  

Gildið í reitnum **Einingarverð** fyrir verkkostnað fjárhags verður notað í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn.

## <a name="to-set-up-job-posting-groups"></a>Verkbókunarflokkur settur upp
Einn þáttur við að áætla verk er að ákveða hvaða bókunarlykla á að nota í kostnaðarútreikningum vegna verka. Til að hægt sé að bóka verk skal setja upp reikninga fyrir hvern verkbókunarflokk. Bókunarflokkur stendur fyrir tengingar milli verksins og hvernig eigi að meðhöndla það í fjárhag. Þegar verk er stofnað er bókunarflokkur tilgreindur, og allir verkhlutar sem búnir eru til fyrir verkið eru tengdir við þann bókunarflokk að sjálfgefnu. Hins vegar er hægt að hnekkja sjálfgildum þegar verk eru stofnuð og velja þann bókunarflokk sem hentar best.  

**Til athugunar**: Setja þarf upp nauðsynlega reikninga í bókhaldslykli áður en bókunarflokkar eru settir upp. Frekari upplýsingar eru í [Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md).  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Bókunarflokkar verka**, og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið út reiti reiknings eins og lýst er í eftirfarandi töflu.  

| Reikningsreitur. | Lýsing |
| --- | --- |
| **Kóði** |Kóti er fyrir bókunarflokkinn. Hægt er að færa inn allt að 10 stafi, með bilum. |
| **VÍV - kostnaðarreikn.** |VÍV reikningur útreiknaðs kostnaðar verksins sem er í vinnslu er eignareikningur á efnahagsreikningi. |
| **VÍV - reikn. uppsafnaðs kostnaðar** |Reikningur fyrir kostnaðarvirðis- eða sölukostnaðaraðferð útreiknings VÍV, sem er skuldareikningur uppsafnaðs kostnaðar á efnahagsreikningi. Á hann er bókað þegar leiðrétting á VÍV krefst þess að bókaður notkunarkostnaður á rekstrarreikning sé aukinn. |
| **Jöfnunarreikningur verks** |Mótreikningur VÍV kostnaðarreikninga, sem er andstæða neikvæðs kostnaðarreiknings. |
| **Kostnaðarjöfnunarreikningur vöru** |Mótreikningur VÍV kostnaðarreikninga, sem er andstæða neikvæðs kostnaðarreiknings. |
| **Jöfnunarreikningur forða** |Mótreikningur VÍV kostnaðarreikninga, sem er andstæða neikvæðs kostnaðarreiknings. |
| **Kostnaðarjöfnunarreikningur** |Mótreikningur VÍV kostnaðarreikninga, sem er andstæða neikvæðs kostnaðarreiknings. |
| **Mótreikningur verks** |Mótreikningur VÍV reiknings uppsafnaðs kostnaðar, sem er kostnaðarreikningur. |
| **Fh.reikn. söluútgjalda (Fjárhagsáætlun)** |Sölureikningurinn sem verður notaður fyrir fjárhagsútgjöld verkhluta í þessum bókunarflokki. Sé hann auður er fjárhagsreikningurinn sem er færður inn í verkáætlunarlínuna notaður. |
| **VÍV - reikningur uppsafn. sölu** |VÍV reikningur útreiknaðs söluvirðis verksins sem er í vinnslu, sem er reikningur uppsafnaðra tekna á efnahagsreikningi. Á hann er bókað þegar leiðrétting á VÍV krefst aukningar samþykktra tekna. |
| **VÍV - reikningsf. sölureikningur** |Reikningurinn fyrir reikningsfært söluvirði VÍV sem ekki er hægt að samþykkja. Hann er efnahagsreikningur óinnleystra tekna. |
| **Jöfnunarreikningur verksölu** |Reikningur VÍV reiknings uppsafnaðrar sölu, sem er andstæða tekjureiknings. |
| **Mótreikningur verksölu** |Mótreikningur VÍV sölureiknings, sem er tekjureikningur. |
| **Samþykktur kostnaðarreikningur** |Útgjaldareikningurinn sem inniheldur samþykkt útgjöld verksins. Það er vanalega debetkostnaðarreikningur. |
| **Samþykktur sölureikningur** |Tekjureikningurinn sem inniheldur samþykktar tekjur verksins. Það er vanalega kredittekjureikningur. |

## <a name="see-also"></a>Sjá einnig
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

