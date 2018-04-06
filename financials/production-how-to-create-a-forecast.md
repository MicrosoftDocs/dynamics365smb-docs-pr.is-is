---
title: "Hvernig skal búa til framleiðsluspá | Microsoft Docs"
description: "Sölu- og framleiðsluspár eru búnar til í glugganum **Framleiðsluspá** ."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fea8af85518d608f051be154e551c4c8645ed42a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-production-forecast"></a>Stofna framleiðsluspá
Sölu- og framleiðsluspár eru búnar til í glugganum **Framleiðsluspá** .  

Spárvirkni er notuð til að skapa áætlaða eftirspurn; raunveruleg eftirspurn er gerð eftir sölu- og framleiðslupöntunum. Á meðan verið er að stofna aðalframleiðsluáætlun er spáin reiknuð saman við söluna og framleiðslupantanirnar. Valkosturinn  *Íhlutur* á spánni ákvarðar hvers konar skilyrði á að taka tillit til í útreikningsferlinu. Ef spáin er fyrir söluvöru eru bara sölupantanir reiknaðar saman við spána. Ef hún er fyrir íhluti er aðeins háð eftirspurn úr íhlutum framleiðslupöntunar reiknuð saman við spána.  

Spá gerir fyrirtækinu kleift að búa til "hvað ef" atburðarásir og áætla og mæta eftirspurn á skilvirkan máta sem borgar sig. Nákvæm spá getur breytt miklu um það hversu ánægðir viðskiptavinir eru hvað varðar dagsetningar pöntunarloforða og tímanlega afgreiðslu.  

## <a name="sales-forecasts-and-production-forecasts"></a>Söluspár og Framleiðsluspár  
Hægt er að nota spárvirknina í kerfinu til að búa til sölu- eða framleiðsluspár, saman eða hvort í sínu lagi. Til dæmis hafa flest fyrirtæki sem framleiða tilbúnar vörur ekki fullbúna birgðaskrá af því að hver vara er framleidd þegar hún er pöntuð. Það að gera ráð fyrir pöntunum (söluspáraðgerðir) skiptir máli varðandi ásættanlegan biðtíma eftir tilbúnu vörunum (framleiðsluspáraðgerðir). Til dæmis geta íhlutar með langa afhendingartíma tafið framleiðsluna ef þeir eru hvorki á pöntuninni né á birgðaskránni.  

-   Söluspáin er besta tillaga söludeildarinnar um hvað verði selt í framtíðinni, tilgreind eftir vörum og tímabili. Hvað sem því líður er söluspáin ekki alltaf næg fyrir framleiðslu.  
-   Framleiðsluspáin er vörn þess sem gerir áætlunina yfir magn vörunnar og skyldra undirtegunda framleiða skal á ákveðnum tímabilum til að standast áætlaða sölu.  

Í flestum tilfellum breytir framleiðslustjórinn söluspánni svo að hún passi saman við framleiðsluskilyrðin en uppfylli samt söluspána.  

Þú býrð til framleiðsluspár handvirkt í **Framleiðsluspá** glugganum. Margar spár geta verið til í kerfinu og þeim er skipt eftir nafni og tegund. Hægt er að afrita og breyta spám eftir þörfum. Athuga ber að aðeins er hægt að nota eina skrá í einu til að gera áætlanir.  

Spáin samanstendur af fjölda færslna sem taka hver fyrir sig fram vörunúmer, spárdagsetningu og spáð magn. Spá vöru nær yfir tímabil sem skilgreinist eftir spárdagsetningunni og spárdagsetningu næstu (seinni) spárfærslu. Út frá áætlunarsjónarmiði ætti spáð magn að vera fyrir hendi í upphafi eftirspurnartímabilsins.  

Gefa verður spá til kynna sem *Söluvöru*, *Íhlut* eða *Bæði*. Spártegundin *Söluvara* er notuð í söluspá. Framleiðsluspáin er búin til með því að nota tegundina *Íhlutur*. Spártegundin *Bæði* er bara notuð til að veita stjórnandanum yfirsýn yfir bæði söluspána og framleiðsluspána. Þegar þessi valkostur hefur verið valinn er ekki hægt að breyta spárfærslunum. Með því að gefa til kynna þessar spártegundir hérna er hægt að nota sama vinnublað til að setja inn söluspá sem notað er til að setja inn framleiðsluspá og nota sama blað til að skoða báðar spár samtímis. Athuga skal að kerfið fer með ílögin tvö (sölu og framleiðslu) á mismunandi hátt þegar áætlanir eru reiknaðar út, eftir vöru, framleiðslu og framleiðsluuppsetningu.  

## <a name="component-forecast"></a>Íhlutaspá  
Hægt er að líta á íhlutaspána sem valkostaspá í sambandi við yfirvöru. Þetta getur til dæmis verið hentugt ef stjórnandinn getur áætlað eftirspurn eftir íhlutnum.  

Þar sem íhlutaspáin er hönnuð til að skilgreina valkosti fyrir yfirvöru ætti íhlutaspáin að vera jöfn eða lægri en magn söluvöruspárinnar. Ef íhlutaspáin er hærri en söluvöruspáin þá fer kerfið með mismuninn á milli þessara tveggja spártegunda sem sjálfstæða eftirspurn.  

## <a name="forecasting-periods"></a>Spártímabil  
 Spártímabilið er í gildi frá upphafsdagsetningu þess og til þeirrar dagsetningar sem næsta spá byrjar. Tímabilsglugginn gefur marga valkosti til að setja eftirspurnina inn á sérstökum degi innan tímabils. Þess vegna mælum við ekki með því að umfangi spártímabilsins sé breytt nema æskilegt þyki að færa allar spárfærslur til upphafsdagsetningar þess tímabils.  

## <a name="forecast-by-locations"></a>Spá eftir birgðageymslum  
Hægt er að taka það fram í framleiðsluuppsetningunni ef. Athuga ber samt að ef birgðageymslugrundvallaðar spár eru skoðaðar einar og sér gæti verið að spáin í heild sinni sé ekki nothæf sem úttak.

## <a name="to-create-a-production-forecast"></a>Framleiðsluspá stofnuð

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Framleiðsluspá** og velja svo viðeigandi tengil.  
2.  Á flýtiflipanum **Almennt** er spá valin í reitnum **Heiti framleiðsluspár**. Margar spár geta verið til í kerfinu og þeim er skipt eftir heiti og spártegund.  
3.  Í reitnum **Afmörkun staðsetningar** er staðsetningin valin sem þessi spá mun eiga við um.  
4.  Í reitnum **Tegund spár** er valið **Vörusala**, **Íhlutur** eða  **Bæði**. Ef valin er **Vörusala** eða **Íhlutur**, er hægt að breyta magninu eftir tímabili. Ef **Bæði** er valið er ekki hægt að breyta magninu en hægt er að velja hnappinn með felliörinni og skoða færslur framleiðsluáætlunarinnar.  
5.  Tilgreind er **Dags.afmörkun** ef takmarka á það gagnamagn sem er sýnt.  
6.  Á flýtiflipanum **Framleiðsluspá - fylki** er fært inn áætlað magn **vörusölu** eða **íhluta** samkvæmt spá fyrir mismunandi tímabil.  
7.  Á flýtiflipanum **Valkostir fylkis** er tímabilið stillt í reitnum **Skoða eftir** til að skipta um það tímabil sem sýnt er í hverjum dálki . Eftirfarandi tímabil eru í boði: **Dagur**, **Vika**, **Mánuður**, **Fjórðungur**, **Ár** eða **Reikningstímabil** sem sett er upp í Fjármálastjórnun.  

    > [!NOTE]  
    >  Íhuga skal hvaða tímabil á að nota við seinni tíma spár, þannig að samræmi verði á milli tímabila. Þegar magn er fært inn í spá er það í gildi á fyrsta degi tímabilsins sem valið er. Ef t.d. mánuður er valinn, þá er magnið fært inn í spána á fyrsta degi mánaðarins. Ef fjórðungur er valin, er magn fært inn í spána á fyrsta degi fyrsta mánaðar fjórðungsins.  

8.  Í reitnum **Skoða sem** er magn spár valið sem á að sýna fyrir tímabilið. Ef valin er **Hreyfing**, þá birtist staða hreyfingar fyrir viðkomandi tímabil. Ef valin er **Staða til dags.**, þá birtist staða síðasta dags tímabilsins.  

> [!NOTE]  
>  Einnig er hægt að breyta núverandi spá. Í glugganum **Framleiðsluspá fylki** er smellt á **Afrita framleiðsluspá** aðgerðina fylla **Framleiðsluspá** gluggann með fyrirliggjandi Framleiðsluspá. Hægt er að gera breytingar á magni eins og við á.  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

