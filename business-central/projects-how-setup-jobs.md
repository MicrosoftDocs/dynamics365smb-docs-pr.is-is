---
title: Setja upp verð fyrir verk og verkbókunarflokka| Microsoft Docs
description: Lýsir því hvernig setja á upp almennar upplýsingar um verk, og setja upp verð fyrir vörur verks, tilföng, og fjárhagsreikninga og verkbókunarflokka.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 34dfdb463d3423d823b8f1439361d05296ca3c8a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "918825"
---
# <a name="set-up-jobs"></a>Setja upp verk

Sem verkefnisstjóri getur þú sett upp verk sem skilgreina verkefnin sem þú stjórnar í [!INCLUDE [prodshort](includes/prodshort.md)]. Á síðunni **Uppsetning verka** verður að tilgreina hvernig á að nota tiltekna verkeiginleika.

Fyrir hvert verk tilgreinir þú þá einstök verkspjöld með upplýsingum um verð fyrir vörur, forða og fjárhagsreikninga verks og setja þarf upp verkbókunarflokka.

## <a name="to-set-general-information-for-jobs"></a>Til að stilla almennar upplýsingar fyrir verk
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning verka** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Áhrif reitsins **Beita notkunartengli að sjálfgefnu** er frekar flókinn og er því útskýrður í eftirfarandi kafla.

### <a name="to-set-up-job-usage-tracking"></a>Til að setja upp notkunarrakningu verka

Þegar verið er að framkvæma verk gæti verið gagnlegt að vita hvernig notkunin er rakin á móti áætluninni. Til að gera þetta á auðveldan hátt, er hægt að búa til tengil milli verkáætlunarlínunnar og hinnar eiginlegu notkunar. Þetta leyfir þér að rekja kostnað þinn og sjá auðveldlega hversu mikið af vinnu á eftir að vinna. Sjálfgefið er að áætlunarlína verktegundar sé **Áætlun**, en ef línutegundin **Bæði fjárhagsáætlun og reikningshæft** er notuð hefur það svipuð áhrif.

Ef þú velur reitinn **Beita notkunartengli að sjálfgefnu** getur þú skoðað upplýsingar á verkáætlunarlínu. Hægt er að stilla magn forða, vöru eða fjárhagsreiknings og gefa svo upp hvaða magn á að færa í verkbókina. Í reitnum **Eftirstöðvar (magn)** í verkáætlunarlínunni sést hvað á eftir að flytja og bóka í verkbókina.

> [!TIP]  
> Hægt er að gera rakningu verknotkunar virka eða óvirka fyrir tiltekið verk. Gildi reitsins **Nota notkunartengil** á stöku verkspjaldinu hunsar stillinguna á síðunni **Uppsetning verka**.  

Þegar **Beita notkunartengli að sjálfgefnu** gátreiturinn er valinn og gerð verkáætlunarlínu er **Reikningshæf**, er búin til verkáætlunarlína af gerðinni **Fjárhagsáætlun** eftir að þú hefur bókað færslubókarlínu verks.

> [!IMPORTANT]
> Ef rakning verknotkunar er virk, annaðhvort á síðunni **Uppsetning verka** eða í tilteknu verki og reiturinn **Línugerð** í færslubókarlínu verks er auður mun nýjar verkáætlunarlínur af línugerðinni **Fjárhagsáætlun** vera stofnaðar þegar bókaðar eru færslubókarlínur verks.  
>  
> Ef rakning verknotkunar er *ekki* virk, annaðhvort á síðunni **Uppsetning verka** eða í tilteknu verki og reiturinn **Línugerð** í færslubókarlínu verks er auður munu engar verkáætlunarlínur vera stofnaðar þegar bókaðar eru færslubókarlínur verks. Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning verks** og velja svo viðeigandi tengil.
2. Veldu **Beita notkunartengli að sjálfgefnu** gátreitinn.

## <a name="to-set-up-prices-for-job-resources"></a>Til að setja upp verð fyrir verkforða
Sérstök verð má setja upp fyrir forða verks. Síðan **Forðaverð verks** er notuð til þess.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Forði**.
3. Á síðunni **Forðaverð verks** þarf að fylla reitina út eftir þörfum.

Viðbótarupplýsingar í reitunum **Verkhlutanr.**, **Tegund vinnu**, **Gjaldmiðilskóti**, **Línuafsl. %** og **Stuðull einingarverðs** verða notaðar í verkáætlunarlínum og notkunarbókum þegar þessi forði er sleginn inn og honum bætt við verkið.  

Virðið í reitnum **Einingarverð** fyrir forðann verður notað í verkáætlunarlínum og verkbókum þegar þessi forði, forði sem úthlutað er á forðahóp, eða einhver annar forði er færður inn.  

> [!NOTE]  
>   Þetta verð mun ávalt hnekkja öllum verðum sem eru sett upp á **Forðaverð/forðaflokkaverð** síðunni sem fyrir er.

## <a name="to-set-up-prices-for-job-items"></a>Til að setja upp verð fyrir vörur verks
Sérstök verð má setja upp fyrir vörur verka. Síðan **Verð vöru** er notup til þess.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Vara**.
3. Á síðunni **Vöruverð verks** þarf að fylla reitina út eftir þörfum.

Viðbótarupplýsingarnar í reitunum **Verkhlutanr.**, **Gjaldmiðilskóti** og **Línuafsl.** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi vara er slegin inn eða henni bætt við verk.  

Gildið í reitnum **Einingarverð** fyrir vöruna verður notað í verkáætlunarlínum og verkbókum þegar þessi vara er slegin inn.  

> [!NOTE]  
>   Þetta verð hnekkir alltaf hefðbundnu viðskiptamannaverði („besta verð”) vöru. Ef nota skal hefðbundnar verðuppsetningar ætti ekki að stofna verð fyrir verkvöruna.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>að setja upp verð í fjárhagsreikningi fyrir verk
Hægt er að setja upp ákveðið verð fyrir fjárhagsleg útgjöld í verki. Síðan **Verð fjárhagsreiknings verks** er notuð til þess.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Fjárhagsreikningur**.  
3. Á síðunni **Fjárhagsreikningsverð verks** þarf að fylla reitina út eftir þörfum.

Viðbótarupplýsingar í reitunum **Verkhlutanr.**, **Gjaldmiðilskóti**, **Línuafsl. %**, **Stuðull einingarverðs** og **Kostn.verð** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn og honum bætt við verk.  

Gildið í reitnum **Einingarverð** fyrir verkkostnað fjárhags verður notað í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn.

## <a name="to-set-up-job-posting-groups"></a>Verkbókunarflokkur settur upp
Einn þáttur við að áætla verk er að ákveða hvaða bókunarlykla á að nota í kostnaðarútreikningum vegna verka. Til að hægt sé að bóka verk skal setja upp reikninga fyrir hvern verkbókunarflokk. Bókunarflokkur stendur fyrir tengingar milli verksins og hvernig eigi að meðhöndla það í fjárhag. Þegar verk er stofnað er bókunarflokkur tilgreindur, og allir verkhlutar sem búnir eru til fyrir verkið eru tengdir við þann bókunarflokk að sjálfgefnu. Hins vegar er hægt að hnekkja sjálfgildum þegar verk eru stofnuð og velja þann bókunarflokk sem hentar best.  

> [!NOTE]  
>   Nauðsynlega reikninga verður að stofna í bókhaldslykli áður en bókunarflokkar eru stofnaðir. Frekari upplýsingar eru í [Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókunarflokkar verka** og veldu síðan tengda tengilinn.  
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
[Myndband: Hvernig á að stofna verk í Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
