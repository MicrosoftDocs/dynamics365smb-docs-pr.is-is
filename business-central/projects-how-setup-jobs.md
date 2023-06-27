---
title: Setja upp verð fyrir verk og verkbókunarflokka
description: 'Lýsir því hvernig setja á upp almennar upplýsingar um verk, og setja upp verð fyrir vörur verks, tilföng, og fjárhagsreikninga og verkbókunarflokka.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Setja upp verð fyrir verk og verkbókunarflokka

Sem verkefnisstjóri getur þú sett upp verk sem skilgreina verkefnin sem þú stjórnar í [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **Uppsetning verka** verður að tilgreina hvernig á að nota tiltekna verkeiginleika.

Fyrir hvert verk tilgreinir þú þá einstök verkspjöld með upplýsingum um verð fyrir vörur, forða og fjárhagsreikninga verks og setja þarf upp verkbókunarflokka.

## <a name="to-set-general-information-for-jobs"></a>Til að stilla almennar upplýsingar fyrir verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning verks** og velja síðan viðkomandi tengil.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Reiturinn **Beita notkunartengli að sjálfgefnu** tilgreinir hvort verkfærslur eru tengdar sjálfgefið á verkáætlunarlínur. Veljið reitinn ef nota á þessa stillingu fyrir öll ný verk sem eru stofnuð. Hægt er að gera rakningu verknotkunar virka eða óvirka fyrir tiltekið verk með því að breyta gildinu í **Nota notkunartengil** reitnum á einstaka verkspjaldi. Afleiðingarnar eru útskýrðar í næsta hluta.

### <a name="to-set-up-job-usage-tracking"></a>Til að setja upp notkunarrakningu verka

Þegar unnið er að verki gæti verið gagnlegt að vita hvernig notkunin er rakin á móti áætluninni. Til að gera þetta á auðveldan hátt, er hægt að búa til tengil milli verkáætlunarlínunnar og hinnar eiginlegu notkunar. Þetta leyfir þér að rekja kostnað þinn og sjá auðveldlega hversu mikið af vinnu á eftir að vinna. Sjálfgefið er að áætlunarlína verktegundar sé *Áætlun*, en ef línutegundin **Bæði fjárhagsáætlun og reikningshæft** er notuð hefur það svipuð áhrif.

Þegar búið er að setja upp notkun rakningar með því að velja **Nota notkunartengil**, er hægt að fara yfir upplýsingar um verkáætlunarlínuna. Hægt er að stilla magn forða, vöru eða fjárhagsreiknings og gefa svo upp hvaða magn á að færa í verkbókina. Í reitnum **Eftirstöðvar (magn)** í verkáætlunarlínunni sést hvað á eftir að flytja og bóka í verkbókina.

>[!NOTE]
> Ef reiturinn **Nota notkunartengil** er valinn í einstöku verki og reiturinn **Línutegund** í verkbókarlínunni eða innkaupalínunni er *Reikningshæft* þá eru nýjar verkáætlunarlínur af línugerðinni *Áætlun* búnar til þegar færslubók eða innkaupaskjal er bókað.  
> Frekari upplýsingar eru í [Skrá notkun vegna verka](projects-how-record-job-usage.md) og [Stjórna verkbirgðum](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Ef **Línugerð** reiturinn á færslubókarlínu verka er tómur, þá eru engar verkáætlunarlínur búnar til þegar þú bókar færslubók eða innkaupaskjal.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Til að setja upp verð fyrir tilföng, vörur og fjárhagsreikninga fyrir verk

> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út nýja ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Hægt er að setja upp verð fyrir vörur, tilföng og fjárhagsreikninga sem tengjast starfi. 

#### [Núverandi reynsla](#tab/current-experience)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veldu verkið og veldu síðan aðgerðina **Tilfang**, **Vara** eða **Fjárhagsreikningur**.
3. Á síðunum **Forðaverð verks**, **Vöruverð verks** eða **Verð fjárhagsreiknings verks** skal fylla í reitina eftir þörfum.

Eftirfarandi tafla sýnir hvernig upplýsingarnar í valfrjálsum svæðunum verða notaðar í verkáætlunarlínum og færslubókum þegar tilfang, vara eða fjárhagsreikningur er valið fyrir verkið.

|Column1  |Column2  |
|---------|---------|
|**Hjálpargögn**|Reitirnir **Verkhlutanr. verks**, **Tegund verks**, **Gjaldmiðilskóði**, **Línuafsl. %** og **Stuðull einingaverðs**. Virðið í reitnum **Einingarverð** fyrir forðann verður notað í verkáætlunarlínum og verkbókum þegar þessi forði, forði sem úthlutað er á forðahóp, eða einhver annar forði er færður inn. Athugið að þetta verð mun ávalt hnekkja öllum verðum sem eru sett upp á **Forðaverð/forðaflokkaverð** síðunni sem fyrir er.|
|**Verkatriði**|Reitirnir **Nr. verkhluta**, **Gjaldmiðilskóði** og **Línuafsl. %**. Gildið í reitnum **Einingarverð** fyrir vöruna verður notað í verkáætlunarlínum og verkbókum þegar þessi vara er slegin inn. Athugið að þetta verð hnekkir alltaf hefðbundnu viðskiptamannaverði („besta verð”) vöru. Ef nota skal hefðbundnar verðuppsetningar ætti ekki að stofna verð fyrir verkvöruna.|
|**Fjárhagsreikningar**|Upplýsingar í reitunum **Verkhlutanr.**, **Gjaldmiðilskóti**, **Línuafsl. %**, **Stuðull einingarverðs** og **Kostn.verð** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn og honum bætt við verk. Gildið í reitnum **Einingarverð** fyrir verkkostnað fjárhags verður notað í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn.|

#### [Ný reynsla](#tab/new-experience)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Söluverðlistar**.

---

## <a name="to-set-up-job-posting-groups"></a>Verkbókunarflokkur settur upp

Einn þáttur við að áætla verk er að ákveða hvaða bókunarlykla á að nota í kostnaðarútreikningum vegna verka. Til að hægt sé að bóka verk skal setja upp reikninga fyrir hvern verkbókunarflokk. Bókunarflokkur stendur fyrir tengingar milli verksins og hvernig eigi að meðhöndla það í fjárhag. Þegar verk er stofnað er bókunarflokkur tilgreindur, og allir verkhlutar sem búnir eru til fyrir verkið eru tengdir við þann bókunarflokk að sjálfgefnu. Hins vegar er hægt að hnekkja sjálfgildum þegar verk eru stofnuð og velja þann bókunarflokk sem hentar best.  

> [!NOTE]  
>   Nauðsynlega reikninga verður að stofna í bókhaldslykli áður en bókunarflokkar eru stofnaðir. Frekari upplýsingar eru í [Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókunarflokkar verks** og velja síðan viðkomandi tengil.  
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

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/set-up-jobs-resources/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Myndband: Hvernig á að stofna verk í Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
