---
title: Breyta árlegri upphæð þjónustusamnings eða samningstilboðs
description: Hægt er að breyta upphæðinni sem verður reiknuð árlega á þjónustusamningum eða þjónustusamningstilboðum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes" />Breyta árlegri upphæð þjónustusamnings eða samningstilboðs
Hægt er að breyta árlegri upphæð þjónustusamnings eða samningstilboðs til að leiðrétta upphæðina sem verður reikningsfærð árlega.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote" />Árlegri upphæð þjónustusamnings eða samningstilboðs breytt:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustusamningur** eða **Þjónustsamningstilboð** og velja síðan viðkomandi tengil.  
2. Veldu samninginn eða samningstilboðið.  
3. Veldu aðgerðina **Opna samning** til að opna samninginn eða samningstilboðið þannig að hægt sé að gera breytingar.  
4. Veldu **Heimila ójafnaðar upphæðir** ef breyta á árlegri upphæð og skipta mismun árlegrar upphæðar handvirkt í samningslínunum. Annars skal hreinsa gátreitinn  til að dreifa árlegum mismun sjálfkrafa á samningslínur eftir að ársupphæð hefur verið breytt.  
5. Efninu í reitnum **Árleg upphæð** er breytt. Ekki er hægt að undirrita. þ.e. breyta í þjónustusamning ef unnið er í samningstilboði, né læsa þjónustusamningnum ef árleg upphæð er neikvæð. Ef árlega upphæðin er sett á núll verður efnið í reitnum **Reikningstímabil** að vera **Ekkert** við undirritun eða þegar þjónustusamningi er læst.  
6. Eftir því hvort gátreiturinn **Heimila ójafnaðar upphæðir** er valinn er keyrð annaðhvort handvirk eða sjálfvirk skipting á mismun árlegrar upphæðar. Samningslínurnar verða uppfærðar á þann hátt að gildið í reitnum **Reiknuð árleg upphæð** verði jafnt nýju árlegu upphæðinni.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts" />Dreifing mismunar milli nýrrar og reiknaðrar árlegrar upphæðar
Ef valið er að breyta árlegri upphæð þjónustusamnings eða samningstilboðs gæti verið gott að skipta mismuninum milli nýrra og reiknaðra árlegra upphæða í samningslínunum. Það eru þrjár leiðir til að dreifa upphæðum:

* Jöfn dreifing  
* Dreifa eftir línuupphæðum  
* Dreifa eftir framlegð

### <a name="even-distribution" />Jöfn dreifing
Ef valið er að breyta árlegri upphæð þjónustusamnings eða samningstilboðs gæti verið gott að skipta mismuninum milli nýrra og reiknaðra árlegra upphæða í samningslínunum. Jöfn skipting er ein af sjálfvirku skiptingaraðferðunum sem geta hjálpað til við að skipta mismuni nýju og reiknuðu ársupphæðanna jafnt milli línuupphæða í samningslínunum. Eftirfarandi listi yfir skref í skiptingarferlinu lýsir grunnhugmyndinni að baki þessari aðferð:  

1. Mismuninum milli gildanna í reitunum ný **Árleg upphæð** og **Reiknuð árleg upphæð** er deilt í fjölda samningslína í þjónustusamningnum eða samningstilboðinu.  
2. Gildið í reitnum **Línuupphæð** er uppfært með því að bæta við niðurstöðu fyrri aðgerðar.  
3. Efnið í reitunum **Afsl.upphæð línu**, **Línuafsl. %** og **Framlegð** er uppfært með tilliti til við nýja virðið í reitnum **Línuupphæð** á eftirfarandi hátt:   
    * Afsl.upphæð línu = Línuvirði - Línuupphæð.  
    * Línuafsl. % = Afsl.upphæð línu / Línuvirði * 100.  
    * Framlegð = Línuupphæð - Línukostnaður.  

 Skrefin eru endurtekin fyrir hverja samningslínu.  

#### <a name="example" />Dæmi
Gátreiturinn **Heimila ójafnaðar upphæðir** er ekki valinn í þjónustusamningnum sem inniheldur þrjár samningslínur með þessum upplýsingum.  

|Vara|Línukostnaður|Línuvirði|Línuafsl. %|Afsl.upphæð línu|Línuupphæð|Framlegð|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vara 1|30,00|40,00|0,00|0,00|40,00|10,00|  
|Vara 2|40,00|50,00|10,00|5,00|45,00|5,00|  
|Vara 3|50,00|70,00|10,00|7,00|63,00|13,00|  

Virðið í reitnum **Árleg upphæð** er það sama og í reitnum **Reiknuð árleg upphæð** sem er alltaf stillt á samtölu línuupphæðanna. Í þessu tilviki er það jafnt og eftirfarandi: 40 +45 +63 = 148.  

Ef **Árlegri upphæð** er breytt í 139 reiknar kerfið upphæðina sem þarf að bæta við hverja **Línuupphæð**. Þessi upphæð er reiknuð með því að draga **Reiknuð árleg upphæð** frá nýja gildinu í reitnum **Árleg upphæð** og deila útkomunni með fjölda samningslína í þjónustusamningnum. Í þessu tilviki verður það jafnt og eftirfarandi: (139 - 148) / 3 = -3. Þá er síðustu reiknuðu tölunni bætt við hvert virði í reitnum **Línuupphæð** og virðin í reitunum **Línuafsl.%**, **Afsl.upphæð línu** og **Framlegð** eru uppfærð í samræmi við reiknireglurnar í ferlinu sem lýst er hér að framan.  

Að lokum verða þessi gögn í samningslínunum.  

|Vara|Línukostnaður|Línuvirði|Línuafsl. %|Afsl.upphæð línu|Línuupphæð|Framlegð|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vara 1|30,00|40,00|7,50|3,00|37,00|7,00|  
|Vara 2|40,00|50,00|16.00|8.00|42.00|2.00|  
|Vara 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount" />Drefing byggð á línuupphæð
Ef valið er að breyta árlegri upphæð þjónustusamnings eða samningstilboðs gæti verið gott að skipta mismuninum milli nýrra og reiknaðra árlegra upphæða í samningslínunum. Skipting eftir línuupphæð er sjálfvirk aðferð sem getur hjálpað til við að skipta mismuni nýju og reiknuðu ársupphæðanna milli línuupphæða í samningslínunum. Skiptingin verður hlutfallsleg eftir línuupphæðarhlut þeirra í reiknuðu ársupphæðinni. Eftirfarandi listi yfir skref í skiptingarferlinu fyrir hverja samningslínu lýsir grunnhugmyndinni að baki þessari aðferð:  

1. Línuupphæðarprósentan er reiknuð á eftirfarandi hátt: efninu í reitnum **Línuupphæð** er deilt í samtölu gilda í reitnum **Reiknuð árleg upphæð** í öllum samningslínum.  
2. Gildið í reitnum **Línuupphæð** er uppfært með því að bæta því við mismuninn milli nýju og reiknuðu ársupphæðarinnar, sem er margfaldaður með línuupphæðarprósentunni.  
3. Efnið í reitunum **Afsl.upphæð línu**, **Línuafsl. %** og **Framlegð** er uppfært með tilliti til við nýja virðið í reitnum **Línuafsláttarupphæð** á eftirfarandi hátt:  

    * Afsl.upphæð línu = Línuvirði - Línuupphæð  
    * Línuafsl. % = Afsl.upphæð línu / Línuvirði * 100  
    * Framlegð = Línuupphæð - Línukostnaður  

Skrefin eru endurtekin fyrir hverja samningslínu.  

#### <a name="example-1" />Dæmi
Gátreiturinn **Heimila ójafnaðar upphæðir** er ekki valinn í þjónustusamningnum sem inniheldur þrjár samningslínur með þessum upplýsingum.  

|Vara|Línukostnaður|Línuvirði|Línuafsl. %|Afsl.upphæð línu|Línuupphæð|Framlegð|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vara 1|15,00|17,00|3,00|0,51|25,00|1,49|  
|Vara 2|20,00|23,00|Ekkert|0,00|55,10|3,00|  
|Vara 3|24,00|27,00|3,00|0,81|112,70|2,19|  

Virðið í reitnum **Árleg upphæð** er það sama og í reitnum **Reiknuð árleg upphæð** sem er alltaf stillt á samtölu línuupphæðanna. Í þessu tilviki er það jafnt og eftirfarandi: 16,49 +23,00 +26,19 = 65,68.  

Er **Árleg upphæð** er breytt í 60 reiknast framlegðarprósenta hverrar samningslínu:  

* Vara 1 – 5 / (5 + 5.1 +12.7) = 0.2193 %  
* Vara 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Vara 3 – 12.7 / (5 + 5.1 + 12.7) = 0.557  

Þá er gildið í reitnum **Línuupphæð** uppfærð í hverri samningslínu með reiknireglunni: Línuupphæð = Línuupphæð + mismunur milli nýju og reiknuðu ársupphæðanna * Prósenta Að því loknu eru gildin í reitunum Afsl.upphæð línu, Línuafsl. Að því loknu eru gildin í reitunum **Afsl.upphæð línu**, **Línuafsl. %** og **Framlegð** uppfærð með reiknireglunum sem lýst er að framan.  

Að lokum verða þessi gögn í samningslínunum.  

|Vara|Línukostnaður|Línuvirði|Línuafsl. %|Afsl.upphæð línu|Línuupphæð|Framlegð|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vara 1|15,00|17,00|11,41|1,94|15,06|0,06|  
|Vara 2|20,00|23,00|8.65|1.99|21.01|1.01|  
|Vara 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit" />Dreifing byggð á framlegð
Ef valið er að breyta árlegri upphæð þjónustusamnings eða samningstilboðs gæti verið gott að skipta mismuninum milli nýrra og reiknaðra árlegra upphæða í samningslínunum. Skipting eftir framlegð er ein af sjálfvirku aðferðunum sem geta hjálpað til við að skipta mismuni nýju og reiknuðu ársupphæðanna milli línuupphæða í samningslínunum. Þessi skipting verður hlutfallsleg eftir framlegðarhlut þeirra í heildarframlegð samningsins eða samningstilboðsins. Eftirfarandi listi yfir skref í skiptingarferlinu fyrir hverja samningslínu lýsir grunnhugmyndinni að baki þessari aðferð:  

1. Framlegðarprósentan er reiknuð á eftirfarandi hátt: efninu í reitnum **Framlegð** er deilt í samtölu gilda í reitnum **Framlegð** í öllum samningslínum.  
2. Gildið í reitnum **Línuupphæð** er uppfært með því að bæta því við mismuninn milli nýju og reiknuðu ársupphæðarinnar, sem er margfaldaður með framlegðarprósentunni.  
3. Efnið í reitunum Afsl.upphæð línu, Línuafsl. % og Framlegð er uppfært með tilliti til við nýja virðið í reitnum **Línuupphæð** á eftirfarandi hátt:  

    * Afsl.upphæð línu = Línuvirði - Línuupphæð  
    * Línuafsl. % = Afsl.upphæð línu / Línuvirði * 100  
    * Framlegð = Línuupphæð - Línukostnaður  

#### <a name="example-2" />Dæmi
Gátreiturinn **Heimila ójafnaðar upphæðir** er ekki valinn í þjónustusamningnum sem inniheldur þrjár samningslínur með þessum upplýsingum.  

|Vara|Línukostnaður|Línuvirði|Línuafsl. %|Afsl.upphæð línu|Línuupphæð|Framlegð|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vara 1|20,00|25,00|0,00|0,00|25,00|5,00|  
|Vara 2|50,00|58,00|5,00|2,90|55,10|5,10|  
|Vara 3|100,00|115,00|2,00|2,30|112,70|12,70|  

Virðið í reitnum **Árleg upphæð** er það sama og í reitnum **Reiknuð árleg upphæð** sem er alltaf stillt á samtölu línuupphæðanna. Í þessu tilviki er það jafnt og eftirfarandi: 25,00 +55,10 +112,70 = 192,80.  

 Er **Árleg upphæð** er breytt í 180 reiknast framlegðarprósenta hverrar samningslínu:  

* Vara 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Vara 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Vara 3 – 12.7 / (5 + 5.1 + 12.7) = 0.557  

Þá er gildið í reitnum **Línuupphæð** uppfærð í hverri samningslínu með reiknireglunni: Línuupphæð = Línuupphæð + mismunur milli nýju og reiknuðu ársupphæðanna * Prósenta Að því loknu eru gildin í reitunum Afsl.upphæð línu, Línuafsl. Að því loknu eru gildin í reitunum **Afsl.upphæð línu**, **Línuafsl. %** og **Framlegð** uppfærð með reiknireglunum úr skrefi 3 í ferlinu sem lýst er að framan.  

Að lokum verða þessi gögn í samningslínunum.  

|Vara|Línukostnaður|Línuvirði|Línuafsl. %|Afsl.upphæð línu|Línuupphæð|Framlegð|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vara 1|20,00|25,00|11,24|2,81|22,19|2,19|  
|Vara 2|50,00|58,00|9.93|5.76|52.24|2.24|  
|Vara 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also" />Sjá einnig
[Búa til þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Þjónustustýring sett upp](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
