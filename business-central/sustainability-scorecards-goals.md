---
title: Sjálfbærni og markmið
description: Læra að setja upp og nota árangursmat og markmið sjálfbærni.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, scorecard, goal, forecast, budget'
ms.search.form: null
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Yfirlit yfir árangursmat sjálfbærni og markmiða

Þessi grein býður upp á leiðbeiningar um hvernig á að búa til árangursmat og markmið, og hvernig á að uppfæra stöðu markmiða. Árangursmat og markmið gera fyrirtækjum kleift að lækna sjálfbærnimælingar og rekja þá gegn lykilmarkmiðum viðskipta. Hægt er að búa til markmið á grundvelli gildandi og markgilda svo að notendur geti fylgst með framvindu núverandi útstreymis í samanburði við fyrri tímabil.  

## Stofna árangursmat  

Til að stofna nýtt *árangursmat* sjálfbærni skal fylgja skrefunum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **árangursmat** sjálfbærni og velja síðan viðeigandi tengja. 
2. Á síðunni **Sjálfbærni árangursmat skal velja** Nýtt **til að stofna nýtt árangursmat** .  
3. Tilgreina skal reitinn **Nr.** Og reitunum **Heiti** á flýtiflipanum **Almennt** og síðan er eiganda **bætt** við. 

> Takið eftir, 100.000 Í reitnum **Eigandi** er aðeins hægt að velja notendur sem hafa valið reitinn **Sjálfbærnistjóri** í töflunni **Notandaupplýsingar** . 

## Stofna markmið  

Til að stofna nýtt *markmið um sjálfbærni* skal fylgja skrefunum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **árangursmat** sjálfbærni og velja síðan viðeigandi tengja.
2. Veljið aðgerðina **Markmið** til að stofna nýtt **sjálfbærnimarkmið** fyrir valið árangursmat.  
3. Valið er **Nýr** til að byrja að stofna nýtt markmið.
4. Reiturinn **Nr. árangursmats** Gildinu úr tengda **árangursmatinu** er sjálfkrafa bætt við og notandinn getur ekki breytt þessum reit. Kerfið setur einnig upp reitinn **Mælieining** samkvæmt **mælieiningarkóta** losunar á síðunni **Sjálfbærniuppsetning** .  
5. Fylla verður út reitinn **Nr.** og **heiti** nýs **sjálfbærnimarkmiðs**. Reiturinn **Eigandi** er sjálfkrafa fylltur út frá gildinu úr tengdu **árangursmati** sjálfbærni.   
6. Notendur geta ákveðið að stofna *sjálfbærnimarkmið* fyrir allt fyrirtækið, tiltekið land/svæði eða aðstöðu. Ef notendur vilja stofna sérstakt markmið verður hann að velja landið eða svæðið í reitnum **Lands-/svæðiskóti** eða aðgerðin í reitnum **Ábyrgðarstöð** .  
7. Velja skal reitina **Upphafsdagsetning** og **Lokadagsetning** til að setja upp sértækt tímabil fyrir rakningu gildandi gilda. Þessi grunnstilling ákvarðar gildin í eftirfarandi reitum: **Current Value Value fyrir CO2**, **Current Value Value fyrir CH4** og **Current Value for N2O**. 
8. Velja skal reitina **Upphafsdagsetning** grunnlínu og **Lokadagsetning** til að setja upp sértækt grunntímabil til að bera saman gildandi gildi. Þessi grunnstilling ákvarðar gildin í eftirfarandi reitum: **Grunnlína fyrir CO2,Grunnlína** **fyrir CH4** og **Grunnlína fyrir N2O**.
9. Einnig geta notendur bætt við markgildum í reitnum Mælieining sem var valinn **fyrir yfirstandandi tímabil með því að nota eftirfarandi reiti:** Target Value fyrir CO2 **,** Target Value fyrir CH4 **og** Target Value fyrir N2O **.**   
10. Hægt er að velja eitt af þessum markmiðum sem **aðalmarkmið**. Gildi úr aðalmarkmiðinu eru notuð í hlutverkamiðstöð **sjálfbærnistjóra** .  

Ef þú hefur mörg markmið á síðunni getur þú notað **Sýna markmið** aðgerð til að sýna þér aðeins markmiðin þín og ef þú vilt sýna öll verður þú að keyra aðgerðina **Sýna öll markmið** .  

> [!NOTE]
> *Sjálfbærnimarkmið* er aðeins hægt að stofna fyrir tiltekið *árangursmat* sjálfbærni og ekki er hægt að stofna mörk sem ekki tengjast árangursmatinu, en þú getur búið til fleiri mörk fyrir eitt árangursmat. Aðeins er hægt að hafa eitt **sjálfbærnimarkmið** merkt sem **aðalmarkmið**.

> [!NOTE]
> Notendur geta sett upp mismunandi samsetningar markmiða fyrir allt fyrirtækið, tiltekin lönd eða svæði og ábyrgðarstöð fyrir eitt *sjálfbært árangursmat*. Notendur geta einnig notað mismunandi tímabil fyrir sama líkan af rakningu. 

## Sjá einnig .

[Sjálfbærniuppsetning](finance-sustainability-setup.md)    
[Bókhaldslykill sjálfbærnireikninga og fjárhagur](finance-sustainability-accounts-ledger.md)    
[Hvernig á að skrá sjálfbærnifærslur](finance-sustainability-journal.md)    
[Tilfallukkagreining á sjálfbærnigögnum](ad-hoc-analysis-sustainability.md)    
[Sjálfbærniskýrslur og greiningar í Business Central](sustainability-reports.md)   
[API sjálfbærni](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Fjármál](finance.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
