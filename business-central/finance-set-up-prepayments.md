---
title: Uppsetning fyrirframgreiðslu
description: Kynntu þér hvernig á að skilgreina Business Central þannig að hægt sé að nota fyrirframgreiðslur til að reikningsfæra og innheimta innborganir frá viðskiptavinum og senda lánardrottnum innborganir.
author: brentholtorf
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: '314, 459, 460, 664'
ms.date: 10/27/2021
ms.author: bholtorf
---
# Uppsetning fyrirframgreiðslu

Ef viðskiptavinir þurfa inna greiðslu af hendi áður en þeir fá pöntun afhenta eða ef lánardrottinn fer fram á greiðslu áður en hann afhendir pöntun er hægt að nota aðgerðina Fyrirframgreiðsla. Aðgerð fyrirframgreiðslu gerir þér kleift að reikningsfæra og innheimta innborganir frá viðskiptavinum eða senda lánardrottnum innborganir til að tryggja að allar hlutagreiðslur séu bókaðar til móts við reikning. Nánari upplýsingar eru í [Búa til fyrirframgreiðslureikninga](finance-how-to-create-prepayment-invoices.md).

Áður en þú getur bókað fyrirframgreiðslureikning verður þú að setja upp bókunarreikningana í fjárhag og númeraraðir fyrir fyrirframgreiðsluskjöl. Þú verður að tilgreina reikning fyrir fyrirframgreiðslur sem tengjast sölu og reikningi fyrir fyrirframgreiðslur sem tengjast innkaupum. Þú getur tilgreint sömu bókunarreikninga til notkunar fyrir allar fyrirframgreiðslur sem tengjast öllum almennum viðskiptabókunarflokkum eða almennum vörubókunarflokkum, eða þú getur tilgreint tiltekna reikninga fyrir tilteknar bókunarflokka fyrir sölu og innkaup. Þetta fer eftir kröfum fyrirtækisins þíns varðandi rakningu fyrirframgreiðslna.  

Þú getur tilgreint prósentu línuupphæðarinnar sem verður reikningsfærð, fyrir viðskiptamann eða lánardrottin fyrir allar vörur eða valdar vörur. Þegar uppsetningu er lokið er hægt að búa til fyrirframgreiðslureikninga úr sölu- og innkaupapöntunum. Þú getur notað skilgreindu prósenturnar fyrir hverja sölu- eða innkaupalínu eða breytt upphæðunum á reikningnum eins og þarf. Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

> [!NOTE]
> Mælt er með því að ekki sé notuð 100 prósenta fyrirframgreiðslu í eftirfarandi tilvikum:
>
> * Ef þú ert í Norður-Ameríku. Vegna þess hvernig skattar eru reiknaðir er prósenta fyrirframgreiðslu 100 sem getur leitt til vandamál með fyrirframgreiðslureikninga.
> * Á öllum svæðum, ef greiðsluafsláttur er handvirkt dreginn frá reikningi. Fyrirframgreiðsluprósenta 100 mun ekki sjálfkrafa skilja eftir upphæð sem draga þarf afsláttinn frá.
>
> Þegar þú notar fyrirframgreiðsluprósentuna 100 gæti [!INCLUDE[prod_short](includes/prod_short.md)] einnig þurft að stofna sléttunarfærslur mótbókunar. Þegar það gerist þarftu að velja fjárhagsreikning í reitnum **Sléttunarlykill reiknings** á síðunni **Bókunarflokkar viðskiptamanns**. Þetta á við jafnvel þótt þú hafir ekki kveikt á **Sléttun reiknings** á síðunni **Uppsetning sölugrunns**. Ef þú tilgreinir ekki lykil geturðu ekki bókað fyrirframgreiðslureikninga. 

Þar sem fyrirframgreidd upphæð tilheyrir kaupanda þar til hann hefur móttekið vörur eða þjónustu þarf að setja upp fjárhagsreikninga til að geyma fyrirframgreiðsluupphæðir þar til lokareikningurinn er bókaður. Sölufyrirframgreiðslur þarf að skrá í skuldareikning þar til vörurnar eru afhentar. Fyrirframgreiðslur innkaupa þarf að skrá í eignareikning þar til vörurnar eru mótteknar. Auk þess þarf að setja upp sérstakan fjárhagsreikning fyrir hvert VSK-kenni.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## Bæta fyrirframgreiðslureikningum við almennan bókunargrunn  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning almennrar bókunar** og velja síðan viðkomandi tengil.
2. Á síðunni **Almennur bókunargrunnur**, fyrir viðeigandi línur, skal fylla út eftirfarandi reiti:  

    * **Fyrirframgreiðslureikn. sölu**  
    * **Fyrirframgr.reikn. innkaupa**  

> [!TIP]
> Ef þú getur ekki séð reitina á síðunni **Uppsetning bókunargrunns** notaðu þá lárétta flettistiku neðst á síðunni til að fletta til hægri.  

Ef almennir fjárhagsreikningar hafa ekki enn verið settir upp fyrir fyrirframgreiðslur er hægt að fara á síðuna **Fjárhagsreikningalisti** frá viðeigandi reit reiknings.  

## Uppsetning númeraraðar fyrir fylgiskjöl fyrirframgreiðslu  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. Á síðunni **Uppsetning sölugrunns**, í flýtiflipanum **Númeraraðir**, skal fylla út eftirfarandi reiti:  

   * **Bókuð fyrirframgr.reikn.nr.**
   * **Bókuð kr.reikn.nr. fyrirframgr.**

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slá inn **Uppsetning innkaupa og viðskiptaskulda** og velja svo viðeigandi tengil.
4. Á síðunni **Uppsetning innkaupagrunns**, í flýtiflipanum **Númeraraðir**, skal fylla út eftirfarandi reiti:

    * **Bókuð fyrirframgr.reikn.nr.**
    * **Bókuð kr.reikn.nr. fyrirframgr.**

> [!NOTE]  
> Hægt er að nota sömu númeraröð fyrir fyrirframgreiðslureikninga og venjulega reikninga, auk þess sem hægt er að nota mismunandi númeraraðir. Ef mismunandi raðir eru notaðar mega þær ekki skarast, númer má ekki vera í meira en einni röð.  

## Að setja upp fyrirframgreiðsluprósentu fyrir vörur, viðskiptamenn og lánardrottna

Fyrir vöru er hægt að setja upp sjálfgefna fyrirframgreiðsluprósentu fyrir alla viðskiptamenn, tiltekinn viðskiptamann eða verðflokk viðskiptamanns. Ef ekki á að nota sömu fyrirframgreiðsluprósentuna á alla viðskiptamenn þarf að tilgreina hvaða viðskiptamenn eða verðflokkar viðskiptamanns fyrirframgreiðsluprósentan á við um.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Veljið Atriði og veljið svo aðgerðina **Fyrirframgreiðsluprósenta**.  
3. Á síðunni **Sala fyrirframgreiðsluprósenta** skal fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Fyrir viðskiptamann eða lánardrottin er hægt að setja upp eina sjálfgefna prósentu fyrirframgreiðslu fyrir allar vörur og allar tegundir sölulína. Þú færir þetta inn á viðskiptamanna eða lánardrottna kortið. Eftirfarandi ferli sýnir hvernig á að tilgreina fyrirframgreiðsluprósentu fyrir viðskiptamann, en svipuð skref gilda um lánardrottna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opna spjaldið fyrir viðskiptamann.
3. **Fyrirframgreiðsla %** er fært inn í reitinn .
4. Skrefin eru endurtekin fyrir aðra viðskiptamenn og lánardrottna.  

> [!TIP]
> Einnig er hægt að opna síðuna **Fyrirframgreiðsluprósentur sölu** úr viðskiptamanna- eða lánardrottnaspjaldi.

### Til að ákvarða hvaða fyrirframgreiðsluprósenta hefur forgang  

Pöntun getur haft prósentu fyrirframgreiðslu í söluhausnum og aðra prósentu fyrir vörurnar í línunni. Til að ákvarða hvaða fyrirframgreiðsluprósentu á að nota við hverja sölulínu leitar kerfið að fyrirframgreiðsluprósentu í eftirfarandi röð, og notar svo fyrsta sjálfgildið sem það finnur:  

1. Fyrirframgreiðsluprósentu fyrir vöruna í línunni og viðskiptamanninn sem pöntunin er fyrir.  
2. Fyrirframgreiðsluprósentu fyrir vöruna í línunni og verðflokk viðskiptamanna sem viðskiptamaðurinn tilheyrir.  
3. Fyrirframgreiðsluprósentu fyrir vörunar í línunni fyrir alla viðskiptamenn.  
4. Fyrirframgreiðsluprósentan í sölu- eða innkaupahausnum.  

Með öðrum orðum, fyrirframgreiðsluprósentan í viðskiptamannsspjaldinu á eingöngu við ef engin prósenta er sett upp fyrir vöruna. Ef innihaldi reitsins **Fyrirframgreiðsla %** er hinsvegar breytt á sölu- eða innkaupahausnum eftir að búið er að stofna línurnar er fyrirframgreiðsluprósenta allra lína uppfærð. Á þennan hátt er auðveldara að stofna pöntun með fasta fyrirframgreiðsluprósentu, sama hvaða prósenta er uppsett í vörum.

## Að gefa út sölupantanir sjálfkrafa þegar fyrirframgreiðslur eru jafnaðar

Hægt er að spara tíma með því að setja upp verkraðarfærslu sem gefur sjálfkrafa út sölupantanir sem krefjast fyrirframgreiðslu eftir að greiðslur eru jafnaðar. Að gera ferlið sjálfvirkt sparar þér skrefið við að gefa út sölupöntunina.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. Í reitnum **Tíðni sjálfvirkrar uppfærslu fyrirfgr.** skal tilgreina hversu oft á að keyra verkraðarfærsluna.

> [!TIP]
> Á meðan þú ert hér skaltu íhuga að bæta við vörn gegn afhendingu eða reikningsfærslu sölupantana sem eru með ógreiddar upphæðir fyrirframgreiðslu. Ef þú kveikir á **Athuga fyrirfgr. við bókun** mun [!INCLUDE[prod_short](includes/prod_short.md)] koma í veg fyrir að fólk geti bókað pantanir með útistandandi fyrirframgreiðsluupphæðir.

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
4. Settu upp til dæmis verkraðarfærsluna **Uppf. fyrirfgr.sölu í bið** með því að nota stillingarnar í flýtiflipanum **Endurtekning** til að tímasetja hversu oft á að keyra hana. Frekari upplýsingar er að finna í [Nota verkraðir til að tímasetja verk](admin-job-queues-schedule-tasks.md).

## Sjá tengda [Microsoft þjálfun](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## Sjá einnig .  

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Reikna vöru- og þjónustuskatt á fyrirframgreiðslum í Ástralíu](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Reikna vöru- og þjónustuskatt á fyrirframgreiðslum á Nýja-Sjálandi](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Skilja fjárhag og bókhaldslykil](finance-general-ledger.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
