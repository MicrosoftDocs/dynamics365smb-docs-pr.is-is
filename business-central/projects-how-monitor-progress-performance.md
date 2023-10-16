---
title: Fylgst með framvindu og afköstum
description: Lýsir því hvernig þú getur búið til verk í vinnslu (VÍV) aðferð og reiknað VÍV til að meta fjárhagslegt gildi verka meðan á þeim stendur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# Fylgst með framvindu og afköstum

Með VÍV-eiginleikanum getur þú áætlað fjárhagslegt virði áframhaldandi vinnu í fjárhagnum.

Þegar verki vindur fram eru efni og tilföng notuð og kostnaður verður til sem þarf að bóka fyrir verkið. Oft er kostnaður bókaður áður en verk er reikningsfært. En ef aðeins kostnaður hefur verið bókaður er fjárhagsyfirlitið ónákvæmt. Til að fylgjast með raunvirði verksins skal reikna út VÍV og bóka það í fjárhagnum. Frekari upplýsingar má finna á [Að skilja VÍV-aðferðir](projects-understanding-wip.md).

VÍV má reikna út byggt á eftirfarandi:

* Kostnaðarvirði
* Söluvirði
* Þekkjanlegur kostnaður
* Hlutfalls frágengins
* Samningslok

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## Búa til VÍV-aðferð fyrir verk

Búðu til VÍV-aðferð verks sem uppfyllir kröfur fyrirtækisins og velur það sem sjálfgefið.  

> [!NOTE]
> Þegar búið er að nota nýju aðferðina til að stofna VÍV-færslur er ekki hægt að breyta eða eyða þeirri aðferð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VÍV-aðferð verks** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lokaðu síðunni.   
4. Til að gera þetta að sjálfgefinni aðferð velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning verks** og velja síðan viðkomandi tengil.  
5. Í reitnum **Sjálfgefin vÍv-aðferð** veljið aðferðina af listanum.

## Skilgreina VÍV aðferð fyrir verk

Þegar nýtt verk er stofnað þarf að tilgreina hvaða VÍV-aðferð skuli eiga við. Í sumum tilvikum er VÍV-aðferð verksins sem þú notar þegar valin sem sjálfgefin.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **verk**, velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**. Frekari upplýsingar eru á [Stofna verk](projects-how-create-jobs.md).  
3. Á síðunni **Verkspjald** skal velja VÍV-aðferð úr listanum í reitnum **VÍV-aðferð**. Ef sjálfgefin aðferð hefur verið skilgreind er hægt að velja annan valkost ef þess gerist þörf.  

### Skilgreina VÍV aðferð fyrir verk

Þú getur skilgreint VÍV aðferð fyrir verk, útilokað sum verk frá VÍV-útreikningi eða flokkað verk saman og reikna út heildina. 

Ef reikna á VÍV fyrir hvert verk fyrir sig er býður VÍV-bókun skilgreindar víddir fyrir tiltekin verk.

**VÍV-samtala** tilgreinir verk sem þú vilt safna saman þegar VÍV og skráning eru reiknuð út. Í hverjum verkhlutahópi þarf að vera eitt verk sem uppfyllir tvö skilyrði:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Er með **VÍV-samtölu** stillta á *Samtals*. (Ef engir verkhlutar eru til staðar með **VÍV-samtölu** stillta á *Samtals*, *Samtals* sjálfkrafa á síðustu verkhlutalínu við fyrsta VÍV-útreikning.)

* Er með **Verknúmer** sem er lokanúmerið í flokknum eða svið verka.

Eftirfarandi tafla lýsir valkostunum þremur:

| Svæði | Lýsing |
|--|--|
| **\<blank\>** | Haft autt ef verkhlutinn er hluti af hópi verkhluta. |
| **Samtals** | Skilgreinir svið eða hóp verkhluta sem eru innifaldir í VÍV og samþykkisútreikningi. Innan flokksins mun hver verkhluti með **Tegund verkhluta** stilltan á **Bókun** tekinn með í VÍV-samtölunni, nema að reiturinn **VÍV-samtala** fyrir verkið sé stilltur á **Útilokað**. |
| **Útilokað** | Á aðeins við verk með **Verkhlutategund verks** sem **Bókun** en þá er verkið ekki haft með þegar VÍV og skráning eru reiknuð út. |

Í eftirfarandi dæmi er verkhlutum skipt niður í tvo flokka af VÍV-samtölum, sem sýnir hvernig reiturinn **VÍV-samtala** virkar:

|Númer verkhluta|Lýsing|Tegund verkhluta|**VÍV-samtala** reitur|  
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

* *1000* til og með *1299*: VÍV eru reiknuð út fyrir þennan verkhlutaflokk sér. Athugaðu samt að tvö verkanna, 1010 og 1110, eru útilokuð frá VÍV-útreikningi því að tegund verkhluta er **Bókun**.

* *1300* til og með *1399*: VÍV eru reiknuð út fyrir þennan verkhlutaflokk sér.

## Reikna VÍV

Hægt er að ákvarða VÍV-upphæðina sem bóka skal á efnahagsreikning fyrir skýrslugjöf við lok tímabils. Þetta má gera með því að nota keyrsluna **Verkreikna VÍV**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk - Reikna VÍV** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Reikna VÍV**.
3. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.
4. Velja hnappinn **Í lagi**.  

> [!NOTE]  
>   Runuvinnslan reiknar aðeins VÍV, hún bókar það ekki í fjárhaginn. Til að bóka það skal keyra runuvinnsluna **Bóka VÍV í fjárhag** eftir að VÍV hefur verið reiknað út. Fáðu frekari upplýsingar í eftirfarandi ferli.

## Bóka VÍV

Þegar VÍV hefur verið reiknað er hægt að bóka það á efnahagsreikning fyrir árslokaskýrslu. Þetta má gera með því að nota keyrsluna **Bóka VÍV á fjárhag**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Verk Bóka í VÍV í fjárhag** og veldu síðan tengda tengilinn.  
2. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.

## Reikna út og bóka verklokafærslur

Þegar öllum aðgerðum verks hefur verið lokið, þar með talin bókun notkunar og reikningsfærsla, þarf að uppfæra verkið svo að **Staða** þess sé **Lokið**. Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **verk**, velja síðan viðkomandi tengil.  
2. Veljið opið verk og veljið svo aðgerðina **Breyta**.
3. Í reitnum **Staða** skal velja **Lokið**.
4. Fylgdu aðstoðarskrefunum til að reikna og bóka VÍV. Eða fylgið skrefum 5 og 6 til að gera það handvirkt.  
5. Veljið aðgerðina **Reikna VÍV**.
6. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.  

     VÍV færslurnar sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær séu lokafærslur.  
7. Velja skal aðgerðina **Verk - Bóka VÍV í fjárhag**.
8. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  

     VÍV-fjárlagsfærslur verks sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær eru lokafærslur.

## Verkfærslur skoðaðar

Allar færslur sem tengjast verki eru skráðar í verkdagbækur og tölusettar í réttri röð, byrjað á 1. Í verkdagbókinni er hægt að fá yfirlit um verkfærslurnar.    

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **verkdagbækur** og velja síðan viðkomandi tengil.
2. Valin er viðeigandi dagbók og síðan skal velja aðgerðina **Verklínur**.

Á síðunni **Verkfærslur** er hægt að fara yfir færslur sem tengjast verki.  

## Sjá einnig .

[Kynning - Útreikningur á VÍV fyrir verk](walkthrough-calculating-work-in-process-for-a-job.md)
[Stjórna verkum](projects-manage-projects.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
