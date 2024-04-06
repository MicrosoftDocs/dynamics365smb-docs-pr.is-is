---
title: Fylgjast með framvindu og afköstum verkefnis
description: Lýsir því hvernig hægt er að búa til aðferð fyrir verk í vinnslu (VÍV) og reikna VÍV til að meta fjárhagslegt virði verka á meðan þau eru í vinnslu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---
# <a name="monitor-project-progress-and-performance"></a>Fylgjast með framvindu og afköstum verks

Með aðgerðinni Verk í vinnslu (VÍV) er hægt að meta fjárhagslegt virði verkefna sem eru í fjárhag.

Þegar verk er unnið er efni og forði notaður og útgjöld sem þarf að bóka á verkið. Oft er hægt að bóka kostnað vegna verks áður en reikningsfært er. En ef aðeins kostnaður hefur verið bókaður er fjárhagsyfirlitið ónákvæmt. Til að rekja raunvirði verksins skal reikna VÍV og bóka það í fjárhag. Frekari upplýsingar má finna á [Að skilja VÍV-aðferðir](projects-understanding-wip.md).

VÍV má reikna út byggt á eftirfarandi:

* Kostnaðarvirði
* Söluvirði
* Auðkennanlegur kostnaður
* Hlutfalls frágengins
* Samningslok

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-project-wip-method"></a>Stofna VÍV-aðferð verks

Búa til VÍV-aðferð verks sem uppfyllir þarfir fyrirtækisins og stilla hana sem sjálfgildi.  

> [!NOTE]
> Þegar búið er að nota nýju aðferðina til að stofna VÍV-færslur er ekki hægt að breyta eða eyða þeirri aðferð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **VÍV-aðferðir verks** og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lokaðu síðunni.   
4. Til að gera þetta að sjálfgefinni aðferð velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Tákn, slá inn **verkuppsetningu** og velja síðan viðeigandi tengil.  
5. Í reitnum **Sjálfgefin vÍv-aðferð** veljið aðferðina af listanum.

## <a name="define-a-wip-method-for-a-project"></a>Skilgreina VÍV-aðferð fyrir verk

Þegar nýtt verk er stofnað verður að tilgreina hvaða VÍV-aðferð verks á við. Í sumum tilvikum er VÍV-aðferð verksins sem notuð er þegar sjálfgefin.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.
2. Valið er aðgerðin **Nýtt**. Fræðast meira um [stofnun verkefna](projects-how-create-jobs.md).  
3. Á síðunni **Verkspjald** í reitnum **VÍV-aðferð** skal velja VÍV-aðferð af listanum. Ef sjálfgefin aðferð hefur verið skilgreind er hægt að velja annan valkost ef þess gerist þörf.  

### <a name="define-a-wip-method-for-a-project-task"></a>Skilgreina VÍV-aðferð fyrir verkverk

Hægt er að skilgreina VÍV-aðferð fyrir verkhluta, útiloka verkhluta frá VÍV-útreikningi eða flokka verk sem á að reikna saman. 

Eigi að reikna VÍV fyrir hvern verkhluta sérstaklega býður VÍV-bókun upp á skilgreindar víddir fyrir tiltekna verkhluta.

 **VÍV-samtalan** tilgreinir verkhluta sem á að flokka saman við útreikning VÍV og samþykkis. Í hverjum verkhlutahópi þarf að vera eitt verk sem uppfyllir tvö skilyrði:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Er með **VÍV-samtölu** stillta á *Samtals*. (Ef engir verkhlutar eru til staðar með **VÍV-samtala** stillt *á Samtals*, *Samtals* er stillt sjálfkrafa á síðustu verkhlutalínu þegar VÍV er reiknað í fyrsta skipti.)

* Er með **verkhlutanr.** númer sem er lokatölur í hópnum eða svið verkhluta.

Eftirfarandi tafla lýsir valkostunum þremur:

| Svæði | Heimildasamstæða |
|--|--|
| **\<blank\>** | Hafðu autt ef verkhlutinn er hluti af hópi verkhluta. |
| **Samtals** | Skilgreinir svið eða hóp verkhluta sem eru innifaldir í VÍV og samþykkisútreikningi. Innan flokksins eru allir verkhlutar með **verkhlutagerð verks** sem stilltir **eru á Bókun** tekin með í VÍV-samtölunni, nema VÍV-samtala **verksins** sé stillt á **Útilokað**. |
| **Útilokað** | Á aðeins við um verk með **bókun**  verkhluta **·**, í því tilviki er verkið ekki tekið með þegar VÍV og samþykki eru reiknuð. |

Í eftirfarandi dæmi er verkhlutum skipt í tvo VÍV-heildarflokka sem sýna hvernig reiturinn **VÍV-samtala** vinnur:

|Verkhlutanr.|Heimildasamstæða|Verkhlutagerð verks|**VÍV-samtala** reitur|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Undirbúningur|Byrja-Samtals|\<blank\>|
|1010|.    Þrif|Bóka|**Útilokað**|
|1099|Undirbúningur í heild|Enda-Samtals|\<blank\>|
|1100|Teppalagning|Byrja-Samtals|\<blank\>|
|1110|.    Límbera gólf|Bóka|**Útilokað**|
|1120|.    Leggja teppi|Bóka|\<blank\>|
|1199|Teppalagning í heild|Enda-Samtals|\<blank\>|
|1200|Ljúka|Byrja-Samtals|\<blank\>|
|1210|.    Ryksuga teppi|Bóka|\<blank\>|
|1299|Frágangur í heild|Enda-Samtals|**Samtals**|
|1300|Villuleiðrétting|Byrja-Samtals|\<blank\>|
|1310|.    Villuleiðrétting|Bóka|\<blank\>|
|1399|Villuleiðrétting í heild|Enda-Samtals|**Samtals**|

Þú munt taka eftir:

* *1000* til og með *1299*: VÍV er reiknað út sérstaklega fyrir þennan verkhlutaflokk. Bent er á að tvö af verkunum, 1010 og 1110, eru undanskilin frá VÍV-útreikningnum vegna þess að verkhlutategund þeirra er **Bókun**.

* *1300* til *og með 1399*: VÍV er reiknað út sérstaklega fyrir þennan verkhlutaflokk.

## <a name="calculate-wip"></a>Reikna VÍV

Hægt er að ákvarða VÍV-upphæðina sem bóka skal á efnahagsreikning fyrir skýrslugjöf við lok tímabils. Nota keyrsluverkefnið **Verk - Reikna VÍV** til þess.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **verkútreiknað VÍV** og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Reikna VÍV**.
3. Á síðunni **Verk - Reikna VÍV** skal fylla út reitina eins og þörf krefur.
4. Velja hnappinn **Í lagi**.  

> [!NOTE]  
> Keyrsluverkið reiknar aðeins VÍV, það bókar það ekki í fjárhag. Til að bóka það skal keyra **keyrsluverkið Bóka VÍV í fjárhag** eftir að VÍV hefur verið reiknað. Fáðu frekari upplýsingar í eftirfarandi ferli.

## <a name="post-wip"></a>Bóka VÍV

Þegar VÍV hefur verið reiknað er hægt að bóka það á efnahagsreikning fyrir árslokaskýrslu. Keyrsluverkefnið **Verk - Bóka VÍV í fjárhag** er notað til þess.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verk - Bóka VÍV í fjárhag** og velja síðan viðeigandi tengil.  
2. Á síðunni **Verkbóka VÍV í fjárhag** skal fylla út reitina eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.

## <a name="calculate-and-post-project-completion-entries"></a>Reikna og bóka verklokafærslur

Þegar öllum aðgerðum verks er lokið, þ.m.t. bókun notkunar og reikningsfærsla, verður að uppfæra stöðu **verksins í Lokið**. Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið opið verkefni og veljið svo aðgerðina **Breyta** .
3. Í reitnum **Staða** skal velja **Lokið**.
4. Fylgið aðstoðarskrefunum til að reikna út og bóka VÍV eða fylgja skrefum 5 og 6 til að gera það handvirkt.  
5. Veljið aðgerðina **Reikna VÍV**.
6. Á síðunni **Verk - Reikna VÍV** skal fylla út reitina eins og þörf krefur.  

     VÍV-færslur verksins sem stofnaðar eru með keyrslunni munu hafa gátreitinn **Ljúka** verki valið til að sýna að þær séu lokafærslur.  
7. Velja skal Aðgerðina **Bóka VÍV í fjárhag** .
8. Á síðunni **Verkbóka VÍV í fjárhag** skal fylla út reitina eins og þörf krefur.  

     VÍV-fjárhagsfærslur verksins sem stofnaðar eru með því að keyra keyrsluverkið fá gátreitinn **Verk lokið** til að sýna að þær eru lokafærslur.

## <a name="view-project-ledger-entries"></a>Skoða verkfærslur

Allar færslur sem tengjast verki eru skráðar í verkdagbækur og tölusettar í röð og byrja á 1. Í verkdagbókinni er hægt að fá yfirlit yfir allar verkfærslur.    

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkdagbækur** og velja viðeigandi tengil.
2. Veljið viðeigandi dagbók og veljið **svo verkhöfuðbókaraðgerð** .

Á síðunni **Verkfærslur** er hægt að fara yfir færslurnar sem eru tengdar hvaða verkefni sem er.  

## <a name="see-also"></a>Sjá einnig .

[Kynning - Útreikningur verks í vinnslu fyrir verkefni](walkthrough-calculating-work-in-process-for-a-job.md)
[sem stjórnar verkefnum](projects-manage-projects.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
