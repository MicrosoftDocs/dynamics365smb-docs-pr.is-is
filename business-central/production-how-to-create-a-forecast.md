---
title: Búa til eftirspurnarspá
description: Kynntu þér eiginleika eftirspurnarspár og hvernig hægt er að búa til sölu- og framleiðsluspár.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9245, 99000919, 99000921, 99000922'
ms.date: 03/11/2022
ms.author: edupont
---
# <a name="create-a-demand-forecast"></a><a name="create-a-demand-forecast"></a>Búa til eftirspurnarspá

Þú getur búið til sölu- og framleiðsluspár á listasíðunni **Eftirspurnarspár**. Síðan, fyrir hverja spá, tilgreinir þú ýmsar stillingar fyrir þá spá á síðunni **Yfirlit eftirspurnarspár**.  

Spárvirkni er notuð til að skapa áætlaða eftirspurn; raunveruleg eftirspurn er gerð eftir sölu- og framleiðslupöntunum. Á meðan verið er að stofna aðalframleiðsluáætlun er spáin reiknuð saman við söluna og framleiðslupantanirnar. Reiturinn **Tegund spár** í spánni ákvarðar hvers konar skilyrði á að taka tillit til í útreikningsferlinu. Ef spáin er fyrir *söluvöru* eru bara sölupantanir reiknaðar saman við spána. Ef hún er fyrir *íhluti* er aðeins háð eftirspurn úr íhlutum framleiðslupöntunar reiknuð saman við spána.  

Spá gerir fyrirtækinu kleift að búa til "hvað ef" atburðarásir og áætla og mæta eftirspurn á skilvirkan máta sem borgar sig. Nákvæm spá getur breytt miklu um það hversu ánægðir viðskiptavinir eru hvað varðar dagsetningar pöntunarloforða og tímanlega afgreiðslu.  

Með 2022 útgáfutímabil 1 er einnig hægt að skilgreina rétt stig upplýsinga í reitunum **Spá eftir staðsetningu** og **Spá eftir afbrigði** á síðunni **Yfirlit eftirspurnarspár**. Síur og aðrar stillingar eru geymdar í töflunni **Heiti eftirspurnarspár**. Þú getur því auðveldlega stoppað og haldið vinnunni áfram síðar. Ef fyrirtækið þitt hefur verið uppfært í 2022 útgáfutímabil 1 verður þú að kveikja á nýju upplifuninni á síðunni [Eiginleikastjórnun](admin-feature-management.md).  

## <a name="sales-forecasts-and-production-forecasts"></a><a name="sales-forecasts-and-production-forecasts"></a>Söluspár og Framleiðsluspár

Hægt er að nota spárvirknina í forritinu til að búa til sölu- eða framleiðsluspár, saman eða hvort í sínu lagi. Til dæmis hafa flest fyrirtæki sem framleiða tilbúnar vörur ekki fullbúna birgðaskrá af því að hver vara er framleidd þegar hún er pöntuð. Það að gera ráð fyrir pöntunum (söluspáraðgerðir) skiptir máli varðandi ásættanlegan biðtíma eftir tilbúnu vörunum (framleiðsluspáraðgerðir). Til dæmis geta íhlutar með langa afhendingartíma tafið framleiðsluna ef þeir eru hvorki á pöntuninni né á birgðaskránni.  

- Söluspáin er besta tillaga söludeildarinnar um hvað verði selt í framtíðinni, tilgreind eftir vörum og tímabili. Hvað sem því líður er söluspáin ekki alltaf næg fyrir framleiðslu.  
- Framleiðsluspáin er vörn þess sem gerir áætlunina yfir magn vörunnar og skyldra undirtegunda framleiða skal á ákveðnum tímabilum til að standast áætlaða sölu.  

Í flestum tilfellum breytir framleiðslustjórinn söluspánni svo að hún passi saman við framleiðsluskilyrðin en uppfylli samt söluspána.  

Þú býrð til spá handvirkt á síðunni **Eftirspurnarspá**. Margar spár geta verið til í kerfinu og þeim er skipt eftir nafni og tegund. Hægt er að afrita og breyta spám eftir þörfum. 

> [!NOTE]
> Aðeins ein spá er gild til að gera áætlun hverju sinni.

Spáin samanstendur af fjölda færslna sem taka hver fyrir sig fram vörunúmer, spárdagsetningu og spáð magn. Spá vöru nær yfir tímabil sem skilgreinist eftir spárdagsetningunni og spárdagsetningu næstu (seinni) spárfærslu. Út frá áætlunarsjónarmiði ætti spáð magn að vera fyrir hendi í upphafi eftirspurnartímabilsins.  

Gefa verður spá til kynna sem *Söluvöru*, *Íhlut* eða *Bæði*. Spártegundin *Söluvara* er notuð í söluspá. Framleiðsluspáin er búin til með því að nota tegundina *Íhlutur*. Spártegundin *Bæði* er bara notuð til að veita stjórnandanum yfirsýn yfir bæði söluspána og framleiðsluspána. Þegar þessi valkostur hefur verið valinn er ekki hægt að breyta spárfærslunum. Með því að gefa til kynna þessar spártegundir hérna er hægt að nota sama vinnublað til að setja inn söluspá sem notað er til að setja inn framleiðsluspá og nota sama blað til að skoða báðar spár samtímis. Athuga skal að kerfið fer með ílögin tvö (sölu og framleiðslu) á mismunandi hátt þegar áætlanir eru reiknaðar út, eftir vöru, framleiðslu og framleiðsluuppsetningu.  

## <a name="component-forecast"></a><a name="component-forecast"></a>Íhlutaspá

Hægt er að líta á íhlutaspána sem valkostaspá í sambandi við yfirvöru. Þetta getur til dæmis verið hentugt ef stjórnandinn getur áætlað eftirspurn eftir íhlutnum.  

Þar sem íhlutaspáin er hönnuð til að skilgreina valkosti fyrir yfirvöru ætti íhlutaspáin að vera jöfn eða lægri en magn söluvöruspárinnar. Ef íhlutaspáin er hærri en söluvöruspáin þá fer kerfið með mismuninn á milli þessara tveggja spártegunda sem sjálfstæða eftirspurn.  

## <a name="forecasting-periods"></a><a name="forecasting-periods"></a>Spártímabil

Spártímabilið er í gildi frá upphafsdagsetningu þess og til þeirrar dagsetningar sem næsta spá byrjar. Tímabilssíðan gefur marga valkosti til að setja eftirspurnina inn á sérstökum degi innan tímabils. Þess vegna mælum við ekki með því að umfangi spártímabilsins sé breytt nema æskilegt þyki að færa allar spárfærslur til upphafsdagsetningar þess tímabils.  

## <a name="forecast-by-locations"></a><a name="forecast-by-locations"></a>Spá eftir birgðageymslum

Á síðunni **Uppsetning framleiðslu** er hægt að tilgreina hvort eigi að taka til greina staðsetningarnar sem eru skilgreindar í spám þegar þú reiknar út áætlanir. 

### <a name="use-forecast-by-locations"></a><a name="use-forecast-by-locations"></a>Nota spá eftir staðsetningum

Ef kveikt er á víxlhnappnum **Nota spá eftir staðsetningu** mun [!INCLUDE[prod_short](includes/prod_short.md)] taka til greina alla staðsetningarkóða sem eru tilgreindir fyrir hverja færslu eftirspurnarspár og reikna út eftirstandandi spá fyrir hverja staðsetningu.  

Skoðið þetta dæmi: Fyrirtækið þitt kaupir og selur vörur á tveimur staðsetningum: AUSTUR og VESTUR. Fyrir báðar staðsetningarnar ertu búin(n) að skilgreina endurpöntunarstefnu frá lotu til lotu. Þú býrð til spá fyrir tvær staðsetningar:

- 10 stykki fyrir staðsetningu AUSTUR
- 4 stykki fyrir staðsetningu VESTUR

Síðan stofnarðu sölupöntun með magn upp á 12 á staðsetningu VESTUR. Áætlanakerfið stingur upp á því að þú gerir eftirfarandi:

- Fylla á 10 stykki fyrir staðsetningu AUSTUR, samkvæmt gögnum frá spánni.  
- Fylla á 12 stykki fyrir staðsetningu VESTUR, samkvæmt sölupöntuninni. Stykkin fjögur sem voru tilgreind í spánni eru að fullu notuð af raunverulegri eftirspurn sölupöntunarinnar. Frekari upplýsingar eru í [Spá um eftirspurn er minnkuð eftir sölupöntunum](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

> [!NOTE]  
> Ef staðsetningamiðaðar spár eru skoðaðar einar og sér gæti verið að spáin í heild sinni sýni ekki rétta mynd.

### <a name="do-not-use-forecast-by-locations"></a><a name="do-not-use-forecast-by-locations"></a>Ekki nota spá eftir staðsetningum

Ef slökkt er á víxlhnappnum **Nota spá eftir staðsetningu** mun [!INCLUDE[prod_short](includes/prod_short.md)] hunsa staðsetningarkóða sem eru tilgreindir fyrir hverja færslu eftirspurnarspár og safna spánum saman í spá fyrir tómar staðsetningar.  

Skoðið þetta dæmi: Fyrirtækið þitt kaupir og selur vörur á tveimur staðsetningum: AUSTUR og VESTUR. Fyrir báðar staðsetningarnar ertu búin(n) að skilgreina endurpöntunarstefnu frá lotu til lotu. Þú býrð til spá fyrir tvær staðsetningar:

- 10 stykki fyrir staðsetningu AUSTUR
- 4 stykki fyrir staðsetningu VESTUR

Síðan stofnarðu sölupöntun með magn upp á 12 á staðsetningu VESTUR. Áætlanakerfið stingur upp á því að þú gerir eftirfarandi:

- Fylla á 12 stykki fyrir staðsetningu VESTUR, samkvæmt sölupöntuninni.  
- Fylla á 2 stykki fyrir tómu staðsetninguna. Þau 10 og 4 stykki sem voru tilgreind í spánni eru að notuð að hluta til af raunverulegri eftirspurn sölupöntunarinnar. [!INCLUDE[prod_short](includes/prod_short.md)] hunsaði staðsetningarkóðana sem voru tilgreindir af notandanum og notar tóma staðsetningu í staðinn.  

> [!NOTE]  
> Hægt er að setja upp afmörkun eftir staðsetningum en niðurstöður staðsetninga samræmast ekki endilega niðurstöðum áætlanagerðar án afmörkunar.

## <a name="to-create-a-demand-forecast"></a><a name="to-create-a-demand-forecast"></a>Til að búa til eftirspurnarspá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eftirspurnarspá** og velja síðan viðkomandi tengil.  
2. Á **Almennt** flýtiflipanum skaltu velja spá í **Heiti eftirspurnarpár** reitnum. Margar spár geta verið til í kerfinu og þeim er skipt eftir heiti og spártegund.  
3. Í reitnum **Afmörkun staðsetningar** er staðsetningin valin sem þessi spá mun eiga við um.
4. Á reitnum **Skoða eftir** til að skipta um það tímabil sem sýnt er í hverjum dálki . Eftirfarandi tímabil eru í boði: **Dagur**, **Vika**, **Mánuður**, **Fjórðungur**, **Ár** eða **Reikningstímabil** sem sett er upp á fjármálasvæði notanda.

> [!NOTE]  
> Íhuga skal hvaða tímabil á að nota við seinni tíma spár, þannig að samræmi verði á milli tímabila. Þegar magn er fært inn í spá er það í gildi á fyrsta degi tímabilsins sem valið er. Ef t.d. mánuður er valinn, þá er magnið fært inn í spána á fyrsta degi mánaðarins. Ef fjórðungur er valin, er magn fært inn í spána á fyrsta degi fyrsta mánaðar fjórðungsins.

5. Í reitnum **Skoða sem** er magn spár valið sem á að sýna fyrir tímabilið. Ef valin er **Hreyfing**, þá birtist staða hreyfingar fyrir viðkomandi tímabil. Ef valin er **Staða til dags.**, þá birtist staða síðasta dags tímabilsins.  
6. Í reitnum **Tegund spár** er valið **Vörusala**, **Íhlutur** eða  **Bæði**. Ef valin er **Vörusala** eða **Íhlutur**, er hægt að breyta magninu eftir tímabili. Ef þú velur **Bæði**, þá er ekki hægt að breyta magninu, en þú getur valið fellilistann og skoðað eftirspurnarspáfærslurnar.  
7. Tilgreind er **Dags.afmörkun** ef takmarka á það gagnamagn sem er sýnt.  
8. Á flýtiflipanum **Fylki fyrir eftirspurnarspá** skal færa inn áætlað magn með því að slá inn magnið í reitnum sem stendur fyrir vöru á tiltekinni dagsetningu eða tímabili. Athugið að í tómum reitum opnar uppflettihnappurinn auða síðu sem gefur til kynna að færa þurfi inn gildi handvirkt.   

> [!NOTE]  
> Einnig er hægt að breyta núverandi spá. Á síðunni **Fylki eftirspurnarspár** veldu **Afrita eftirspurnarspá** aðgerðina og fylltu út síðuna **Eftirspurnarspá** með fyrirliggjandi spá. Hægt er að gera breytingar á magni eins og við á.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
