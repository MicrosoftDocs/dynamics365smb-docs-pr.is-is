---
title: 'Setja upp verk, verð og bókunarflokka verka'
description: Lýsir því hvernig almennar upplýsingar um verk eru settar upp.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-projects-prices-and-project-posting-groups"></a>Setja upp verk, verð og bókunarflokka verka

Sem verkefnastjóri er hægt að setja upp verk sem skilgreina hvert þeirra verkefna sem unnið er með í [!INCLUDE[prod_short](includes/prod_short.md)]. Nota skal síðuna **Verkuppsetning** til að skilgreina hvernig nota á verkaðgerðir.

Fyrir hvert verkefni eru tilgreindar ýmsar upplýsingar:

* Verð fyrir verkvörur
* Verktilföng
* Fjárhagsreikningar verks
* Bókunarflokkar verka (nauðsynlegir)

## <a name="to-set-general-information-for-projects"></a>Almennar upplýsingar settar upp fyrir verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkuppsetningu** og velja síðan viðeigandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
>  **Sjálfgefið** er að hólfið Jafna notkunartengil á síðunni **Uppsetning** verka gefur til kynna hvort verkfærslur séu sjálfgefið tengdar verkáætlunarlínum. Kveikja á víbreytunni til að nota þessa stillingu fyrir öll ný verk. Hægt er að gera rakningu verknotkunar virka eða óvirka fyrir tiltekið verkefni með því að kveikja eða slökkva á víkkuninni **Beita notkunartengli** á **síðunni Verkspjald** .

### <a name="to-set-up-project-usage-tracking"></a>Tilgreina sjálfgefna staðsetningu fyrir verkvörur

Hægt er að spara tíma við gagnainnslátt með því að tilgreina sjálfgefna birgðageymslu og hólf fyrir verkefni á síðunni **Verkspjald** . Þegar verkhlutar, verkáætlunarlínur og verkbókarlínur eru stofnaðar fyrir verkið er sjálfgefnu birgðageymslunni og hólfinu sjálfkrafa úthlutað. Hins vegar er hægt að breyta birgðageymslukótanum og hólfinu í verkum og línum ef þörf krefur.

Ef Kóti verkefnahólfs **er skilgreindur** í birgðageymslunni er hólfakótinn fylltur út þegar birgðageymslukótinn er valinn. Ef vöruhúsaflæðið krefst vöruhúsatínslu er einnig hægt að skilgreina önnur hólf sem nota á vörur úr.

Þessir reitir eru sjálfgildin þegar verkhlutar eru stofnaðir. Fyrirliggjandi verkhlutar breytast ekki.

Ýmislegt er hægt að vita um notkun sjálfgefinna birgðageymslna:

* Ef kóti hólfs **verkefnis er skilgreindur** í birgðageymslunni er hólfakótanum úthlutað þegar birgðageymslukótinn er valinn. Ef vöruhúsaflæðið krefst vöruhúsatínslu er einnig hægt að skilgreina önnur hólf sem nota á vörur úr.
* Fyrir verkáætlunarlínur **er Birgðageymslukóti** byggður á gildinu sem valið er í verkáætlunarlínunni þegar vara er valin. Ef hólfakóti er ekki skilgreindur fyrir verkhlutann er hólfið úr sjálfgefna hólfainnihaldinu valið. Hægt er að breyta báðum gildum handvirkt.
* Fyrir verkbókarlínur **er Kóti** birgðageymslu byggður á gildinu sem valið er í verkbókarlínunni þegar vara er valin. Ef hólfakóti er ekki skilgreindur fyrir verkhlutann er hólfið úr sjálfgefna hólfainnihaldinu valið. Hægt er að breyta báðum gildum handvirkt.

### <a name="invoice-multiple-customers-for-project-tasks"></a>Reikningsfæra marga viðskiptavini fyrir verkhluta

Þegar verkefni fela í sér marga viðskiptamenn getur það verið ögrandi að innheimta rétta viðskiptamenn fyrir rétt verk. [!INCLUDE [prod_short](includes/prod_short.md)] gerir innheimtu einfaldari með því að tilgreina reikningsfærslu og selt-til viðskiptavini í hverri verkhlutalínu verks, þannig að hægt er að búa til reikninga sjálfkrafa fyrir rétta viðskiptamenn. Til að fá nánari upplýsingar um reikningsfærslu margra viðskiptamanna er farið á Reikningsfæra á [einn eða fleiri viðskiptavini fyrir verkhluta](projects-how-create-jobs.md#invoice-one-or-more-customers-for-project-tasks).

### <a name="synchronize-the-cost-of-used-items"></a>Til að setja upp rakningu verknotkunar

Þegar unnið er að verkefni gæti notandinn viljað vita hvernig notkunin er rakin samkvæmt áætluninni. Til að kanna notkun er hægt að búa til tengingu milli áætlunarlína verkefnisins og raunnotkunar. Tengillinn gerir þér kleift að rekja kostnað og skilja hversu mikið verk helst. Sjálfgefið er að tegund verkáætlunarlínu sé **Áætlun** en ef línutegundin **Bæði áætlun og Reikningshæft** er hefur svipuð áhrif.

Þegar rakning notkunar hefur verið sett upp með því að kveikja á vífærinu **Nota notkun sjálfgefið** er hægt að skoða upplýsingar í verkáætlunarlínunni. Til dæmis er hægt að stilla magn forðans, vörunnar eða fjárhagsreikningsins. Einnig er hægt að stilla magnið sem á að flytja í verkbókina. Reiturinn **Eftirstöðvar (magn**) í verkáætlunarlínunni sýnir hvað á eftir að flytja og bóka í verkbókina.

>[!NOTE]
>  **Ef Jafna notkunartenging** er valin í verkefninu og **reiturinn Línugerð** í verkbókarlínunni eða innkaupalínunni er Reikningshæft **eru nýjar verkáætlunarlínur af línugerðinni** Bæði áætlun og reikningshæft **stofnaðar þegar verkbókin eða innkaupaskjalið er** bókað.  
>
> Nánari upplýsingar eru í [Skrá notkun vegna verkefna](projects-how-record-job-usage.md) og [unnið með verkbirgðir](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Ef gildi er ekki tilgreint í reitnum **Línutegund** í verkbókarlínunni eða innkaupalínunni eru áætlunarlínur verkefnis ekki stofnaðar þegar verkbókin eða innkaupaskjalið er bókað.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-projects"></a>Til að setja upp verð fyrir forða, vörur og fjárhagsreikninga fyrir verkefni

> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út nýja ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Hægt er að setja upp verð fyrir vörur, forða og fjárhagsreikninga sem tengjast verkefni. 

#### [Núverandi reynsla](#tab/current-experience)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja svo viðeigandi tengil.  
2. Veljið verkefnið og veljið svo aðgerðina **Forði**, **Vara** eða **Fjárhagsreikningur** .
3. Á síðunum **Forðaverð verks**, **Vöruverð verks** eða **Fjárhagsreikningsverð verks** skal fylla út reitina eins og þörf krefur.

Þegar forði, vara eða fjárhagsreikningur er valinn fyrir verkefni eru [!INCLUDE [prod_short](includes/prod_short.md)]  upplýsingar notaðar í valfrjálsum reitum í verkáætlunarlínum og verkbókum. Eftirfarandi tafla útskýrir hvernig.

|Column1  |Column2  |
|---------|---------|
|**Forði verks**|Reitirnir **Verkhlutanr.,** Tegund verks **,** Gjaldmiðilskóti **,** Línuafsl.% **og** Kostnaðarstuðull **kostn.verðs** . Gildið í reitnum **Ein.verð** fyrir forðann er notað í verkáætlunarlínum og verkbókum þegar forði er færður inn eða forði sem úthlutað er á forðaflokkinn. Þetta verð hnekkir verði sem tilgreint er á síðunni **Forðaverð/Forðaflokksverð** .|
|**Verkvörur**|Reitirnir **Verkhlutanr.**, **Gjaldmiðilskóti** og **Línuafsl.%** . Gildið í reitnum **Ein.verð** fyrir vöruna verður notað í verkáætlunarlínum og verkbókum þegar varan er færð inn. Þetta verð hnekkir venjulegu viðskiptamannaverði ("besta verði" vöru. Til að nota venjulegt verð viðskiptamanns skal ekki tilgreina vöruverð fyrir verkið.|
|**Fjárhagsreikningar**|Upplýsingarnar í reitunum **Verkhlutanr.,** Gjaldmiðilskóti **,** Línuafsl. **%**, **Kostnaðarstuðull** kostn.verðs og **Kostnaðarverð** verða notaðar í verkáætlunarlínum og verkbókum þegar þessi fjárhagsreikningur er færður inn og bætt við verk. Þegar fjárhagsreikningur er valinn nota verkáætlunarlínur og verkbækur gildið í reitnum **Ein.verð** fyrir verkkostnað fjárhagsins.|

#### [Ný reynsla](#tab/new-experience)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið viðeigandi verk og veljið svo aðgerðina **Söluverðlistar** .

---

## <a name="to-set-up-project-posting-groups"></a>Uppsetning verkbókunarflokka

Einn þáttur áætlunarverka er að ákveða hvaða bókunarlykla á að nota fyrir kostnaðarútreikning verka. Til að hægt sé að bóka verkefni eru settir upp reikningar fyrir bókun hvers verkbókunarflokks. Bókunarflokkur táknar tengingu milli verksins og hvernig farið skuli með það í fjárhag. Þegar verkefni er stofnað er bókunarflokkur tilgreindur og sjálfgefið er að hver verkhluti sem stofnaður er fyrir verkið er tengdur þeim bókunarflokki. Hins vegar er hægt að hnekkja sjálfgildum þegar verk eru stofnuð og velja þann bókunarflokk sem hentar best.  

> [!NOTE]  
> Setja verður upp reikninga í bókhaldslykli áður en bókunarflokkar eru settir upp. Frekari upplýsingar eru í [Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **verkbókunarflokka** og velja síðan viðeigandi tengil.  
2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

| Reikningsreitur. | Heimildasamstæða | Notað í VÍV-gerð |
| --- | --- |  --- |
| **Kóði** |Kenni fyrir bókunarflokkinn. Hægt er að færa inn allt að 10 stafi, með bilum. | |
| **VÍV - kostnaðarreikn.** |VÍV-reikningur útreiknaðs kostnaðar verksins VÍV, sem er efnahagseignarlykill. | Jafnaður kostnaður, Samþykktur kostnaður|
| **VÍV - reikn. uppsafnaðs kostnaðar** |Reikningur fyrir kostnaðarvirði eða sölukostnað við útreikning VÍV. Þessi reikningur er fyrir uppsafnaða útgjaldaábyrgð á efnahagsreikningi. Þegar VÍV-leiðrétting krefst þess að aukinn notkunarkostnaður sem bókaður er á rekstrarreikning sé bókaður á þennan reikning. | Uppsafnaður kostnaður|
| **Jöfnunarlykill verkkostnaðar** |Mótreikningur VÍV kostnaðarreikninga, sem er andstæða neikvæðs kostnaðarreiknings. Notað þegar **VÍV-bókunaraðferð notuð** er stillt á *Verk*. | Jafnaður kostnaður, Samþykktur kostnaður|
| **Kostnaðarjöfnunarreikningur vöru** |Sama og  **jöfnunarreikningur** verkkostnaðar, en notaður þegar **VÍV-bókunaraðferð notuð** er stillt á *Verkfærsla*.| |
| **Jöfnunarreikningur forða** |Sama og  **jöfnunarreikningur** verkkostnaðar, en notaður þegar **VÍV-bókunaraðferð notuð** er stillt á *Verkfærsla*.| |
| **Jöfnunarreikningur fjárhagskostnaðar** |Sama og  **jöfnunarreikningur** verkkostnaðar, en notaður þegar **VÍV-bókunaraðferð notuð** er stillt á *Verkfærsla*.| |
| **Leiðréttingarlykill verkkostnaðar** |Mótreikningur VÍV reiknings uppsafnaðs kostnaðar, sem er kostnaðarreikningur. | Uppsafnaður kostnaður|
| **Fh.reikn. söluútgjalda (Fjárhagsáætlun)** |Sölureikningurinn sem verður notaður fyrir fjárhagsútgjöld í verkhlutum í þessum bókunarflokki. Ef hann er hafður auður er fjárhagsreikningurinn sem færður er inn í verkáætlunarlínuna notaður. | |
| **VÍV - reikningur uppsafn. sölu** |VÍV-reikningur útreiknaðs söluvirðis VÍV, sem er reikningur uppsafnaðra tekna á efnahagsreikningi notanda. Þegar VÍV-leiðrétting krefst aukningar samþykktra tekna er þessi reikningur bókaður á þennan reikning. | Uppsöfnuð sala, samþykkt sala|
| **VÍV - reikningsf. sölureikningur** |Reikningurinn fyrir reikningsfært söluvirði VÍV sem ekki er hægt að samþykkja. Hann er efnahagsreikningur óinnleystra tekna. | Samþykkt sala, jöfnuð sala|
| **Jöfnunarreikningur verksölu** |Reikningur VÍV reiknings uppsafnaðrar sölu, sem er andstæða tekjureiknings. | Jöfnuð sala, Samþykkt sala|
| **Leiðréttingarlykill verksölu** |Mótreikningurinn við VÍV-verksölureikninginn, sem er tekjureikningur. | Uppsöfnuð sala|
| **Samþykktur kostnaðarreikningur** |Kostnaðarreikningurinn sem inniheldur samþykktan kostnað fyrir verkið. Það er vanalega debetkostnaðarreikningur. | Samþykktur kostnaður|
| **Samþykktur sölureikningur** |Tekjureikningurinn sem inniheldur samþykktar tekjur verkefnisins. Það er vanalega kredittekjureikningur. | Samþykkt sala|

## <a name="see-also"></a>Sjá einnig .

[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Myndband: Hvernig á að stofna verkefni í Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
