---
title: Setja upp verð fyrir verk og verkbókunarflokka
description: Lýsir því hvernig almennar upplýsingar um vinnslur eru settar upp.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Setja upp verð fyrir verk og verkbókunarflokka

Sem verkefnisstjóri getur þú sett upp verk sem skilgreina verkefnin sem þú stjórnar í [!INCLUDE[prod_short](includes/prod_short.md)].  **Notaðu síðuna störf Uppsetning**  til að skilgreina hvernig þú notar vinnslueiginleika.

Fyrir hvert starf eru tilgreindar ýmsar upplýsingar:

* Verð fyrir vinnsluvörur
* Vinnslufjármunum
* Fjárhagsreikningar
* Bókunarflokkar vinnslu (nauðsynlegt)

## <a name="to-set-general-information-for-jobs"></a>Til að stilla almennar upplýsingar fyrir verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning verks** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Með því að nota tengilinn sjálfgefið  **að**  skipta á  **uppsetningarsíðu**  vinnslufærslna gefur til kynna hvort verkfærslur séu tengdar við verkáætlanalínur að sjálfgefnu. Snúið á víxl til að beita þessari stillingu á öll ný verk. Hægt er að gera rakningu verknotkunar virka eða óvirka fyrir tiltekna vinnslu með því að  **·**  kveikja eða slökkva á vinnsluspjaldinu á  **síðunni Verkspjald** .

### <a name="to-set-up-job-usage-tracking"></a>Til að setja upp notkunarrakningu verka

Þegar þú ert að vinna í vinnu gætir þú viljað vita hvernig notkun þín er að rekja til áætlunarinnar. Til að kanna notkun er hægt að búa til tengil á milli verkáætlunarlínanna og raunverulegrar notkunar. Tengillinn gerir þér kleift að fylgjast með þínum kostnaði og skilja hversu mikil vinna er eftir. Sjálfgefið er að áætlunarlína verktegundar sé **Áætlun**, en ef línutegundin **Bæði fjárhagsáætlun og reikningshæft** er notuð hefur það svipuð áhrif.

Eftir að Notkunartengill hefur verið settur upp með því að  **kveikja á nota tengilinn sjálfgefið**  skipti er hægt að skoða upplýsingar í verkáætlunarlínunni. Til dæmis er hægt að stilla magn forðarinnar, vörunnar eða almenns fjárhagslykils. Einnig er hægt að stilla magnið sem á að flytja í verkbókina. Reiturinn magn  **sem eftir er**  í verkáætlunarlínunni sýnir hvað á eftir að flytja og bóka í verkbókina.

>[!NOTE]
>  **Ef nota Tengillinn**  er valinn í vinnslunni og  **reiturinn Tegund**  línu í verkbókarlínu eða innkaupalínu er  **rukkaður**, eru nýjar verkáætlunarlínur fyrir línugerðina  **, bæði áætlun og rukkaðar**, stofnaðar þegar Verkbókin eða innkaupaskjalið eru bókaðar.  
>
> Frekari upplýsingar eru í [Skrá notkun vegna verka](projects-how-record-job-usage.md) og [Stjórna verkbirgðum](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Ef ekki er tilgreint gildi í  **reitnum Tegund**  línu á verkbókarlínu eða innkaupalínu eru verkáætlunarlínur ekki stofnaðar þegar verkbók eða innkaupaskjal er bókað.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Til að setja upp verð fyrir tilföng, vörur og fjárhagsreikninga fyrir verk

> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út nýja ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Hægt er að setja upp verð fyrir vörur, tilföng og fjárhagsreikninga sem tengjast starfi. 

#### [Núverandi reynsla](#tab/current-experience)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veldu verkið og veldu síðan aðgerðina **Tilfang**, **Vara** eða **Fjárhagsreikningur**.
3. Á síðunum **Forðaverð verks**, **Vöruverð verks** eða **Verð fjárhagsreiknings verks** skal fylla í reitina eftir þörfum.

Þegar valið er Forði, vara, eða Fjárhagur fyrir vinnslu, eru  [!INCLUDE [prod_short](includes/prod_short.md)]  notaðar upplýsingar í valfrjálsum reitum í verkáætlunarlínum og verkbókum. Eftirfarandi tafla útskýrir hvernig.

|Column1  |Column2  |
|---------|---------|
|**Hjálpargögn**|Reitirnir **Verkhlutanr. verks**, **Tegund verks**, **Gjaldmiðilskóði**, **Línuafsl. %** og **Stuðull einingaverðs**. Gildið í  **reitnum Einingarverð**  fyrir forða er notað í verkáætlunarlínum og verkbókum þegar fært er inn Forði, eða Forði sem er úthlutað forðaflokki. Þetta verð hnekkir verði sem tilgreint er  **á síðu forðaverðs/forðaflokksins** .|
|**Verkatriði**|Reitirnir **Nr. verkhluta**, **Gjaldmiðilskóði** og **Línuafsl. %**. Gildið í reitnum **Einingarverð** fyrir vöruna verður notað í verkáætlunarlínum og verkbókum þegar þessi vara er slegin inn. Þetta verð hnekkir reglulegu verði viðskiptavinar ("besta verð" vélbúnaður) fyrir vörur. Tilgreindu ekki vinnsluvöruverð fyrir vinnsluna til að nota venjulegt verð viðskiptavinar.|
|**Fjárhagsreikningar**|Upplýsingar í reitunum **Verkhlutanr.**, **Gjaldmiðilskóti**, **Línuafsl. %**, **Stuðull einingarverðs** og **Kostn.verð** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er sleginn inn og honum bætt við verk. Þegar fjárhagslykill er valinn, línur í vinnu og verkbækur nota gildið í  **reitnum Einingarverð**  fyrir kostnað fjárhagsvinnslunnar.|

#### [Ný reynsla](#tab/new-experience)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Söluverðlistar**.

---

## <a name="to-set-up-job-posting-groups"></a>Verkbókunarflokkur settur upp

Einn þáttur við að áætla verk er að ákveða hvaða bókunarlykla á að nota í kostnaðarútreikningum vegna verka. Til að hægt sé að bóka verk skal setja upp reikninga fyrir hvern verkbókunarflokk. Bókunarflokkur stendur fyrir tengingar milli verksins og hvernig eigi að meðhöndla það í fjárhag. Þegar verk er stofnað er bókunarflokkur tilgreindur, og allir verkhlutar sem búnir eru til fyrir verkið eru tengdir við þann bókunarflokk að sjálfgefnu. Hins vegar er hægt að hnekkja sjálfgildum þegar verk eru stofnuð og velja þann bókunarflokk sem hentar best.  

> [!NOTE]  
> Nauðsynlegt er að setja upp lykla í bókhaldslyklum áður en Bókunarflokkar eru settir upp. Frekari upplýsingar eru í [Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókunarflokkar verks** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

| Reikningsreitur. | Heimildasamstæða | Notað í VÍV-gerð |
| --- | --- |  --- |
| **Kóði** |Kenni fyrir bókunarflokkinn. Hægt er að færa inn allt að 10 stafi, með bilum. | |
| **VÍV - kostnaðarreikn.** |VÍV reikningur útreiknaðs kostnaðar verksins sem er í vinnslu er eignareikningur á efnahagsreikningi. | Nýttur kostnaður, viðurkenndur kostnaður|
| **VÍV - reikn. uppsafnaðs kostnaðar** |Lykill fyrir kostnaðarvirði eða kostnaðarsama söluaðferð við útreikning VÍV. Þessi lykill er fyrir uppsafnaða útgjaldaábyrgð á efnahagsreikningi þínum. Þegar VÍG leiðrétting krefst hækkunar á notkunarkostnaði sem er bókaður á rekstrarreikning er bókað á þennan lykil. | Uppsafnaður kostnaður|
| **Jöfnunarreikningur verks** |Mótreikningur VÍV kostnaðarreikninga, sem er andstæða neikvæðs kostnaðarreiknings. Notað þegar  **VÍV-bókunaraðferð sem notuð**  er er uppsett á  *verk*. | Notaður kostnaður, viðurkenndur kostnaður|
| **Kostnaðarjöfnunarreikningur vöru** |Sama og   **lykillinn** fyrir jöfnuð Verkkostnaður en notaður þegar  **VÍV-bókunaraðferðin er notuð**  er stillt á  *verkfærslu*.| |
| **Jöfnunarreikningur forða** |Sama og   **lykillinn** fyrir jöfnuð Verkkostnaður en notaður þegar  **VÍV-bókunaraðferðin er notuð**  er stillt á  *verkfærslu*.| |
| **Reikningur notaður fjárhagskostnaður** |Sama og   **lykillinn** fyrir jöfnuð Verkkostnaður en notaður þegar  **VÍV-bókunaraðferðin er notuð**  er stillt á  *verkfærslu*.| |
| **Mótreikningur verks** |Mótreikningur VÍV reiknings uppsafnaðs kostnaðar, sem er kostnaðarreikningur. | Uppsafnaður kostnaður|
| **Fh.reikn. söluútgjalda (Fjárhagsáætlun)** |Sölureikningurinn sem verður notaður fyrir fjárhagsútgjöld verkhluta í þessum bókunarflokki. Sé hann auður er fjárhagsreikningurinn sem er færður inn í verkáætlunarlínuna notaður. | |
| **VÍV - reikningur uppsafn. sölu** |VÍV-lykill fyrir reiknað söluvirði VÍV sem er áfallin tekjulykill fyrir efnahagslykin. Þegar VÍG leiðrétting krefst þess að auka viðurkenndar tekjur er bókað á þennan lykil. | Áfallna sölu, viðurkennd Sala|
| **VÍV - reikningsf. sölureikningur** |Reikningurinn fyrir reikningsfært söluvirði VÍV sem ekki er hægt að samþykkja. Hann er efnahagsreikningur óinnleystra tekna. | Viðurkennd Sala, jöfnuð í sölu|
| **Jöfnunarreikningur verksölu** |Reikningur VÍV reiknings uppsafnaðrar sölu, sem er andstæða tekjureiknings. | Jöfnuð Sala, viðurkennd Sala|
| **Mótreikningur verksölu** |Mótreikningur VÍV sölureiknings, sem er tekjureikningur. | Uppsöfnuð sala|
| **Samþykktur kostnaðarreikningur** |Útgjaldareikningurinn sem inniheldur samþykkt útgjöld verksins. Það er vanalega debetkostnaðarreikningur. | Samþykktur kostnaður|
| **Samþykktur sölureikningur** |Tekjureikningurinn sem inniheldur samþykktar tekjur verksins. Það er vanalega kredittekjureikningur. | Samþykkt sala|

## <a name="see-also"></a>Sjá einnig .

[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Myndband: Hvernig á að stofna verk í Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
