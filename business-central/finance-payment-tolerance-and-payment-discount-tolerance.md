---
title: Greiðsluvikmörk og greiðsluafsláttarvikmörk | Microsoft Docs
description: Hægt er að setja upp afsláttarvikmörkin til að loka reikningi þegar greiðsla nær ekki upp í fulla upphæð á reikningnum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 823403fc34ad57cb170fc39bd9533b53c4008950
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910881"
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Unnið með greiðsluvikmörk og greiðsluafsláttarvikmörk
Hægt er að setja upp afsláttarvikmörkin til að loka reikningi þegar greiðsla nær ekki upp í fulla upphæð á reikningnum. Til dæmis eru greiðsluvikmörk yfirleitt fyrir litlar upphæðir sem myndi kosta meira að leiðrétta en að samþykkja. Hægt er að nota vikmörk greiðsluafsláttar til að veita greiðsluafslátt eftir að afsláttarmörk eru liðin.  

Hægt er að nota greiðsluvikmörk þannig að allar útistandandi upphæðir hafa leyfilegt hámark greiðsluvikmarka. Ef greiðsluvikmörk eru uppfyllt verður greiðsluupphæðin greind. Ef greiðsluupphæðin er vangreiðsla mun vangreiðslan loka öllum eftirstöðvum. Sundurliðuð fjárhagsfærsla er bókuð á greiðslufærsluna þannig að engar eftirstöðvar eru eftir á jöfnuðu reikningsfærslunni. Ef skilyrði um greiðsluvikmörk eru uppfyllt og greiðsluupphæðin er ofgreiðsla þá verður sundurliðuð fjárhagsfærsla bókuð á greiðslufærsluna þannig að engar eftirstöðvar eru eftir á greiðslufærslunni.

Hægt er að nota vikmörk greiðsluafsláttar þannig, að ef greiðsluafsláttur er veittur eftir dagsetningu greiðsluafsláttar verður hann bókaður á greiðslureikning eða greiðsluvikmarkareikning.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Nota greiðsluvikmörkin á mörg skjöl  
Stakt fylgiskjal hefur sömu greiðsluvikmörk hvort sem það er jafnað eitt og sér eða með öðrum fylgiskjölum. Samþykki á síðbúnum greiðsluafslætti þegar notuð eru afsláttarvikmörk á mörg fylgiskjöl, gerist sjálfkrafa fyrir hvert fylgiskjal þar sem eftirfarandi regla er rétt:  

*dagsetning greiðsluafsláttar < greiðsludagsetning (í aðalfærslu) <= dagsetning greiðsluvikmarka*  

Þessi regla gildir einnig til að ákvarða hvort birta eigi viðvaranir þegar greiðsluvikmörk eru notuð á mörg skjöl. Viðvörun um vikmörk greiðsluafsláttar birtist fyrir hverja færslu sem uppfyllir dagsetningarskilyrðin. Frekari upplýsingar er að finna í [Dæmi 2 - Útreikningur vikmarka fyrir mörg skjöl](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Hægt er að velja að birta viðvörun sem byggist á mismunandi aðstæðum fyrir vikmörk.  

- Fyrsta viðvörunin er fyrir vikmörk veitts greiðsluafsláttar. Tilkynnt er að hægt sé að samþykkja afslátt af síðbúnum greiðslum. Þá er hægt að velja hvort samþykkja skuli vikmörk frá greiðsludegi.  
- Önnur viðvörunin er fyrir greiðsluvikmörkin. Tilkynnt er að hægt sé að loka öllum færslum þar sem mismunurinn er innan samtölu hámarksgreiðsluvikmarka fyrir jöfnuðu færslurnar. Þá er hægt að velja hvort samþykkja skuli vikmörk frá greiðsluupphæð.

> [!NOTE]
> Ef viðvörunarboðin eru virkjuð er hægt að velja hvernig á að vinna úr greiðslum sem eru innan vikmarka. Ef skilaboðin eru ekki virkjuð og vikmörk eru ekki tilgreind verður reikningum með upphæðum sem eru innan vikmarka lokað sjálfkrafa og ekki er hægt að velja að skilja eftir upphæðina sem eftir er. 

Nánari upplýsingar er að finna í [Að gera viðvaranir greiðsluvikmarka virkar eða óvirkar](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## <a name="to-set-up-tolerances"></a>Vikmörk sett upp  
Með vikmörkum á dögum og upphæðum er hægt að loka reikningi þó að greiðsla nái ekki alveg upphæðinni á reikningnum, hvort sem um er að ræða að gjalddagi sé liðinn, vörum hafi verið skilað eða smávillu. Þetta á einnig við um endurgreiðslur og kreditreikninga.  

Svo hægt sé að setja upp vikmörk þarf að setja upp vikmarkareikninga, tilgreina bókunaraðferðir fyrir vikmörk greiðsluafsláttar og greiðsluvikmörk og keyra síðan keyrsluna **Breyta greiðsluvikmörkum** .  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Almennur bókunargrunnur** og veldu síðan tengda tengilinn.  
2. Á síðunni **almennur bókunargrunnur** eru settir upp debet- og kreditreikningar greiðsluvikmarka sölu og debet- og kreditreikningar greiðsluvikmarka innkaupa.  
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókunarflokkar viðskiptamanns** og veldu síðan tengda tengilinn.    
4. Á síðunni **Bókunarflokkar viðskiptamanna** eru debet og kredit greiðsluvikmarkareikningar settir upp. Nánari upplýsingar er að finna í [Uppsetning Bókunarflokka](finance-posting-groups.md).  
5. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókunarflokkur lánardrottins** og veldu síðan tengda tengilinn.  
6. Á síðunni **Bókunarflokk lánardrottna** eru debet og kredit greiðsluvikmarkareikningar settir upp.  
7. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsgrunnur** og veldu síðan tengda tengilinn.  
8. Opna síðuna **Uppsetning fjárhags** .  
9. Á flýtiflipanum **Jöfnun** fyllið út **Greiðsluafslátt greiðsluvikmarka** , **Greiðsluafslátt biðtíma** og svæðið **Bókun greiðsluvikmarka** .   
10. Veljið aðgerðina **Breyta greiðsluvikmörkum** .
11. Á síðunni **Breyta greiðsluvikmörkum** þarf að fylla út reitina **Vikmarkaprósenta greiðslu** og **Hám.upph. greiðsluvikmarka** og smella síðan á **Í lagi** .

> [!IMPORTANT]  
>  Nú hafa verið sett upp vikmörk fyrir heimagjaldmiðilinn eingöngu. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] á að vinna með frávik á greiðslum, kreditreikningum og endurgreiðslum í erlendum gjaldeyri þarf að keyra keyrsluna **Breyta greiðsluvikmörkum** með gildi í reitnum **Gjaldmiðilskóði** .  

> [!NOTE]  
>  Ef fá á viðvörunarboð um greiðsluvikmörk í hvert skipti sem jöfnun er bókuð í vikmörkunum þarf að virkja viðvörun um greiðsluvikmörk. Nánari upplýsingar er að finna í hlutanum [Að gera viðvaranir greiðsluvikmarka virkar eða óvirkar](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
>  Ef gera á vikmörk viðskiptamanns eða lánardrottins óvirk þarf að loka á vikmörk á spjaldi viðkomandi viðskiptamanns eða lánardrottins. Frekari upplýsingar er að finna í [Lokað á greiðsluvikmörk fyrir viðskiptavini](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
>  Þegar vikmörk eru sett upp athugar [!INCLUDE[d365fin](includes/d365fin_md.md)] hvort einhverjar færslur séu opnar og reiknar vikmörk fyrir þær færslur að auki.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Til að virkja eða slökkva á greiðsluvikmarkaviðvörun
Viðvörun um vikmörk greiðslu birtist þegar jöfnun er bókuð með stöðu sem er innan heimilla vikmarka. Hægt er að velja um hvernig staðan skuli bókuð og skráð.    
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsgrunnur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Fjárhagsgrunnur** á flipanum **Jöfnun** skaltu kveikja á **Viðvörun um greiðsluvikmörk** til að virkja viðvörunina. Til að gera viðvörunina óvirka skaltu slökkva á þessu.  

> [!NOTE]  
>  Sjálfgefinn valkostur fyrir **Viðvörun um greiðsluvikmörk** síðuna er **Láta stöðu standa sem eftirstöðvar** . Sjálfgefinn valkostur fyrir **Viðvörun um vikmörk greiðsluafsláttar** síðuna er **Hafna síðbúnum greiðsluafslætti** .

## <a name="to-block-payment-tolerance-for-customers"></a>Lokað á greiðsluvikmörk viðskiptavina  
Sjálfgildið fyrir greiðsluvikmörk er heimilað. Ef greiðsluvikmörk eiga ekki að vera heimil fyrir tiltekin viðskiptamann eða lánardrottinn skal loka á vikmörk á viðkomandi viðskiptamanns- eða lánardrottinsspjaldi. Eftirfarandi sýnir hvernig farið er að þessu fyrir viðskiptamann. Skrefin eru svipuð fyrir lánardrottinn.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamaður** eða **Lánardrottinn** og veldu síðan tengda tengilinn.  
2. Á flýtiflipanum **Greiðslur** skal velja gátreitinn **Loka fyrir vikmörk greiðslu** .  

> [!NOTE]  
>  Ef viðskiptamaður eða lánardrottinn hafa opnar færslur verður að loka á greiðsluvikmörk í opnum færslum.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Dæmi 1 - útreikningur vikmarka fyrir eitt fylgiskjal
Hér á eftir koma nokkur dæmi sem sýna áætlaða vikmarkaútreikninga og bókanir sem upp geta komið við mismunandi aðstæður.  

Síðan **Uppsetning fjárhags** inniheldur eftirfarandi uppsetningu:
- Biðtími greiðsluafsláttar: 5D  
- Hámarks greiðsluvikmörk: 5  

Í dæmum með valmöguleikunum A og B tákna þeir eftirfarandi:  

- **A** Í þessu tilviki hefur viðvörun um vikmörk greiðsluafsláttar verið gerð óvirk EÐA notandinn hefur viðvörunina virka og hefur valið að heimila afslátt af síðbúinni greiðslu (Bóka stöðu sem greiðsluvikmörk).  
- **B** Í þessu tilviki hefur notandinn viðvörunina virka og hefur valið að heimila ekki afslátt af síðbúinni greiðslu (Láta stöðu standa sem eftirstöðvar).  

|—|Reikn.|Staðgr.afsl.|Hám. stgr.vikm.|Mörk staðgr.afsl.|Vikm. staðgr.afsl. Dagsetning|Greiðsludagur|Stgr.|Tegund vikmarka|Allar færslur lokaðar|Vikm. staðgr.afsl. GL/CL|Gr.vikm. Fjárhagur|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1,000|20|5|15/01/03|20/01/03|<=15/01/03|985|Stgr.vikm.|Já|0|-5|  
|2|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**<=15/01/03**|**980**|**Ekkert**|**Já**|**0**|**0**|  
|3|1,000|20|5|15/01/03|c|<=15/01/03|975|Stgr.vikm.|Já|0|5|  
|4A|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|Stgr.afsl.vikm.|Nei, 25 við greiðslu|20/-20|0|  
|5A|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1000|Stgr.afsl.vikm.|Nei, 20 við greiðslu|20/-20|0|  
|6A|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|Stgr.afsl.vikm.|Nei, 15 við greiðslu|20/-20|0|  
|4B|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|Stgr.vikm.|Já|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**16/01/03 20/01/03**|**1000**|**Ekkert**|**Já**|**0**|**0**|  
|6B|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|Stgr.vikm.|Já|0|5|  
|7|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|985|Stgr.afsl.vikm. & Stgr.vikm.|Já|20/-20|-5|  
|8|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|980|Stgr.afsl.vikm.|Já|20/-20|0|  
|9|1,000|20|5|15/01/03|20/01/03|16/01/03 20/01/03|975|Stgr.afsl.vikm. & Stgr.vikm.|Já|20/-20|5|  
|10|1,000|20|5|15/01/03|20/01/03|>20/01/03|1005|Stgr.vikm.|Já|0|-5|  
|**11**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**>20/01/03**|**1000**|**Ekkert**|**Já**|**0**|**0**|  
|12|1,000|20|5|15/01/03|20/01/03|>20/01/03|995|Stgr.vikm.|Já|0|5|  
|13|1,000|20|5|15/01/03|20/01/03|>20/01/03|985|Ekkert|Nei, 15 við reikning|0|0|  
|14|1,000|20|5|15/01/03|20/01/03|>20/01/03|980|Ekkert|Nei, 20 við reikning|0|0|  
|15|1,000|20|5|15/01/03|20/01/03|>20/01/03|975|Ekkert|Nei, 25 við reikning|0|0|  

### <a name="payment-range-diagrams"></a>Skýringar greiðslusviða  
Í tengslum við dæmið að ofan eru skýringar á greiðslusviðum sem hér segir:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Greiðsludagsetning <=15/01/03 (Dæmi 1-3)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol eingreiðslu 1](media/singlePmtTolRules(Pre1503).gif "Reglur um greiðsluþol eingreiðslu 1")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Greiðsludagsetning er á milli 16/01/03 og 20/01/03 (dæmi 4-9)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol eingreiðslu 2](media/singlePmtTolRules(GracePeriod).gif "Reglur um greiðsluþol eingreiðslu 2")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Greiðsludagsetning er eftir 20.01.03 (Dæmi 10-15)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol eingreiðslu 3](media/singlePmtTolRules(Post0120).gif "Reglur um greiðsluþol eingreiðslu 3")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Dæmi 2 útreikningur vikmarka fyrir fjölda fylgiskjala
Hér á eftir koma nokkur dæmi sem sýna áætlaða vikmarkaútreikninga og bókanir sem upp geta komið við mismunandi aðstæður. Dæmin eru takmörkuð við þau tilvik sem enda með því að öllum færslum í jöfnuninni sé lokað.  

Síðan **Uppsetning fjárhags** inniheldur eftirfarandi uppsetningu:
- Biðtími greiðsluafsláttar: 5D  
- Hámarks greiðsluvikmörk 5  

Í dæmum með valmöguleikunum A, B, C og D tákna þeir eftirfarandi:  

- **A** Í þessu tilviki hefur viðvörun um vikmörk greiðsluafsláttar verið gerð óvirk EÐA notandinn hefur viðvörunina virka og hefur valið að heimila afslátt af síðbúinni greiðslu (Bóka sem vikmörk) á öllum reikningum.  
- **B** Í þessu tilviki hefur notandinn viðvörunina virka og hefur valið að heimila ekki afslátt af síðbúinni greiðslu á neinum reikningum.  
- **C** - Í þessu tilviki hefur notandinn viðvörunina virka og hefur valið að heimila afslátt af síðbúinni greiðslu á fyrsta reikningi en ekki þeim næsta.  
- **D** - Í þessu tilviki hefur notandinn viðvörunina virka og hefur valið að heimila ekki afslátt af síðbúinni greiðslu á fyrsta reikningi en heimilar hann á þeim næsta.  

|—|Reikn.|Staðgr.afsl.|Hám. stgr.vikm.|Mörk staðgr.afsl.|Vikm. staðgr.afsl. Dagsetning|Greiðsludagur|Gr.|Tegund vikmarka|Allar færslur lokaðar|Vikm. staðgr.afsl. GL/CL|Gr.vikm. Fjárhagur|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1920|Stgr.vikm.|Já|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**<=15/01/03**|**1910**|**Ekkert**|**Já**|**0**<br /><br /> **0**|0 <br />0|  
|3|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1900|Stgr.vikm.|Já|0<br /><br /> 0|5 <br />5|  
|4B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1980|Stgr.vikm.|Já|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**16/01/03 17/01/03**|**1970**|**Ekkert**|**Já**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1960|Stgr.vikm.|Já|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1920|Stgr.afsl.vikm. & Stgr.vikm.|Já|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1910|Stgr.afsl.vikm.|Já|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1900|Stgr.afsl.vikm. & Stgr.vikm.|Já|60/60|5 <br />5|  
|10B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|2010|Stgr.vikm.|Já|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**18/01/03 20/01/03**|**2000**|**Ekkert**|**Já**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1990|Stgr.vikm.|Já|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1980|Stgr.afsl.vikm. & Stgr.vikm.|Já|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1970|Stgr.afsl.vikm.|Já|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1960|Stgr.afsl.vikm. & Stgr.vikm.|Já|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1950|Stgr.afsl.vikm. & Stgr.vikm.|Já|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1940|Stgr.afsl.vikm.|Já|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1930|Stgr.afsl.vikm. & Stgr.vikm.|Já|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1920|Stgr.afsl.vikm. & Stgr.vikm.|Já|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1910|Stgr.afsl.vikm.|Já|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1900|Stgr.afsl.vikm. & Stgr.vikm.|Já|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|2010|Stgr.vikm.|Já|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**21/01/03 22/01/03**|**2000**|**Ekkert**|**Já**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1990|Stgr.vikm.|Já|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1980|Stgr.afsl.vikm. & Stgr.vikm.|Já|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1970|Stgr.afsl.vikm.|Já|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1960|Stgr.afsl.vikm. & Stgr.vikm.|Já|0/0<br /><br /> 30/30|5 <br />5|  
|28|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|2010|Stgr.vikm.|Já|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**>22/01/03**|**2000**|**Ekkert**|**Já**|**0**|**0**|  
|30|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|1990|Stgr.vikm.|Já|0|5|  

### <a name="payment-range-diagrams"></a>Skýringar greiðslusviða  
Í tengslum við dæmið að ofan eru skýringar á greiðslusviðum sem hér segir:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Greiðsludagsetning <=15/01/03 (Dæmi 1-3)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol margra greiðslna 1](media/multiplePmtTolRules(Pre1503).gif "Reglur um greiðsluþol margra greiðslna 1")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Greiðsludagsetning er á milli 16.01.03 og 17.01.03 (dæmi 4-9)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol margra greiðslna 2](media/multiplePmtTolRules(GracePeriodInv1-2).gif "Reglur um greiðsluþol margra greiðslna 2")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Greiðsludagsetning er á milli 18.01.03 og 20.01.03 (dæmi 10-21)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol margra greiðslna 3](media/multiplePmtTolRules(GracePeriodInv1).gif "Reglur um greiðsluþol margra greiðslna 3")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Greiðsludagsetning er á milli 21.01.03 og 22.01.03 (dæmi 22-27)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol margra greiðslna 4](media/multiplePmtTolRules(GracePeriodInv2).gif "Reglur um greiðsluþol margra greiðslna 4")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Greiðsludagsetning er eftir 22.01.03 (Dæmi 28-30)  
Eftirstöðvar á hverja  

Venjulegar jöfnunarreglur  

![Reglur um greiðsluþol margra greiðslna 5](media/multiplePmtTolRules(Post0122).gif "Reglur um greiðsluþol margra greiðslna 5")  

(1) Ef greiðslan lendir á þessu bili er hægt að loka öllum jöfnunarfærslum með eða án vikmarka.  

(2) Ef greiðslan lendir á þessu bili er ekki hægt að loka öllum jöfnunarfærslum þó þær séu með vikmörkum.

## <a name="see-also"></a>Sjá einnig  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
