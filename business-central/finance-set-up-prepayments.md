---
title: Uppsetning fyrirframgreiðslu
description: Kynntu þér hvernig á að skilgreina Business Central þannig að hægt sé að nota fyrirframgreiðslur til að reikningsfæra og innheimta innborganir frá viðskiptavinum og senda lánardrottnum innborganir.
author: edupont04
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: 314, 459, 460, 664
ms.date: 10/27/2021
ms.author: edupont
ms.openlocfilehash: cf7f84b8ba0c7622f08856b677e3559cc669e7ed
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078675"
---
# <a name="set-up-prepayments"></a>Uppsetning fyrirframgreiðslu

Ef viðskiptavinir þurfa inna greiðslu af hendi áður en þeir fá pöntun afhenta eða ef lánardrottinn fer fram á greiðslu áður en hann afhendir pöntun er hægt að nota aðgerðina Fyrirframgreiðsla. Aðgerð fyrirframgreiðslu gerir þér kleift að reikningsfæra og innheimta innborganir frá viðskiptavinum eða senda lánardrottnum innborganir til að tryggja að allar hlutagreiðslur séu bókaðar til móts við reikning. Nánari upplýsingar eru í [Búa til fyrirframgreiðslureikninga](finance-how-to-create-prepayment-invoices.md).

Áður en þú getur bókað fyrirframgreiðslureikning verður þú að setja upp bókunarreikningana í fjárhag og númeraraðir fyrir fyrirframgreiðsluskjöl. Þú verður að tilgreina reikning fyrir fyrirframgreiðslur sem tengjast sölu og reikningi fyrir fyrirframgreiðslur sem tengjast innkaupum. Þú getur tilgreint sömu bókunarreikninga til notkunar fyrir allar fyrirframgreiðslur sem tengjast öllum almennum viðskiptabókunarflokkum eða almennum vörubókunarflokkum, eða þú getur tilgreint tiltekna reikninga fyrir tilteknar bókunarflokka fyrir sölu og innkaup. Þetta fer eftir kröfum fyrirtækisins þíns varðandi rakningu fyrirframgreiðslna.  

Þú getur tilgreint prósentu línuupphæðarinnar sem verður reikningsfærð, fyrir viðskiptamann eða lánardrottin fyrir allar vörur eða valdar vörur. Þegar uppsetningu er lokið er hægt að búa til fyrirframgreiðslureikninga úr sölu- og innkaupapöntunum. Þú getur notað skilgreindu prósenturnar fyrir hverja sölu- eða innkaupalínu eða breytt upphæðunum á reikningnum eins og þarf. Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

> [!NOTE]
> Mælt er með því að fyrirframgreidd prósenta af 100 sé ekki notuð í eftirfarandi tilvikum:
>
> * Ef þú ert í Norður-Ameríku. Vegna þess hvernig skattar eru reiknaðir er hægt að fá fyrirframgreiðslu upp á 100 á úthreyfingu með fyrirframgreiðslureikningum.
> * Á öllum svæðum, ef greiðsluafsláttur er handvirkt dreginn frá reikningi. Fyrirframgreidd prósenta af 100 mun ekki sjálfkrafa fara upphæð sem dregst frá afslættinum.
>
> Ef greiðsluprósenta af 100 er [!INCLUDE[prod_short](includes/prod_short.md)] notuð, gæti þurft að setja sléttunarfærslur af stað þegar verið er að nota fyrirframgreiðslu. Þegar það gerist þarf að velja fjárhagsreikning í **reitnum Reikningssléttunarlykill** á **síðunni Viðskiptamannabókaraflokkar**. Þetta gildir jafnvel þótt ekki hafi verið kveikt á **reikningssléttun** reikninga á **uppsetningarsíðu** söluins &. Ef ekki er tilgreindur lykill verður ekki hægt að bóka fyrirframgreiðslureikninga. 

Þar sem fyrirframgreidd upphæð tilheyrir kaupanda þar til hann hefur móttekið vörur eða þjónustu þarf að setja upp fjárhagsreikninga til að geyma fyrirframgreiðsluupphæðir þar til lokareikningurinn er bókaður. Sölufyrirframgreiðslur þarf að skrá í skuldareikning þar til vörurnar eru afhentar. Fyrirframgreiðslur innkaupa þarf að skrá í eignareikning þar til vörurnar eru mótteknar. Auk þess þarf að setja upp sérstakan fjárhagsreikning fyrir hvert VSK-kenni.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Bæta fyrirframgreiðslureikningum við almennan bókunargrunn  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning almennrar bókunar** og velja síðan viðkomandi tengil.
2. **Á síðunni almennar bókunaruppsetningar** fyrir viðeigandi línur er fyllt út í eftirfarandi reiti:  

    * **Fyrirframgreiðslureikn. sölu**  
    * **Fyrirframgr.reikn. innkaupa**  

> [!TIP]
> Ef þú getur ekki séð reitina á síðunni **Uppsetning bókunargrunns** notaðu þá lárétta flettistiku neðst á síðunni til að fletta til hægri.  

Ef almennir fjárhagsreikningar hafa ekki enn verið settir upp fyrir fyrirframgreiðslur er hægt að fara á síðuna **Fjárhagsreikningalisti** frá viðeigandi reit reiknings.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Uppsetning númeraraðar fyrir fylgiskjöl fyrirframgreiðslu  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. **Á uppsetningarsíðu** sölu&, á **flipanum númeraröð**, er fyllt út í eftirfarandi reiti:  

   * **Bókuð fyrirframgr.reikn.nr.**
   * **Bókuð kr.reikn.nr. fyrirframgr.**

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slá inn **Uppsetning innkaupa og viðskiptaskulda** og velja svo viðeigandi tengil.
4. **Á uppsetningarsíðu** innkaupa & lánardrottna, á **flipanum númeraröð**, er fyllt út í eftirfarandi reiti:

    * **Bókuð fyrirframgr.reikn.nr.**
    * **Bókuð kr.reikn.nr. fyrirframgr.**

> [!NOTE]  
> Hægt er að nota sömu númeraröð fyrir fyrirframgreiðslureikninga og venjulega reikninga, auk þess sem hægt er að nota mismunandi númeraraðir. Ef mismunandi raðir eru notaðar mega þær ekki skarast, númer má ekki vera í meira en einni röð.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Að setja upp fyrirframgreiðsluprósentu fyrir vörur, viðskiptamenn og lánardrottna

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
> Einnig er hægt að **nálgast síðuna prósenta fyrirframgreiðslu á söluprósentu** af spjaldi viðskiptamanns eða lánardrottins.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Til að ákvarða hvaða fyrirframgreiðsluprósenta hefur forgang  

Pöntun getur haft prósentu fyrirframgreiðslu í söluhausnum og aðra prósentu fyrir vörurnar í línunni. Til að ákvarða hvaða fyrirframgreiðsluprósentu á að nota við hverja sölulínu leitar kerfið að fyrirframgreiðsluprósentu í eftirfarandi röð, og notar svo fyrsta sjálfgildið sem það finnur:  

1. Fyrirframgreiðsluprósentu fyrir vöruna í línunni og viðskiptamanninn sem pöntunin er fyrir.  
2. Fyrirframgreiðsluprósentu fyrir vöruna í línunni og verðflokk viðskiptamanna sem viðskiptamaðurinn tilheyrir.  
3. Fyrirframgreiðsluprósentu fyrir vörunar í línunni fyrir alla viðskiptamenn.  
4. Fyrirframgreiðsluprósentan í sölu- eða innkaupahausnum.  

Með öðrum orðum, fyrirframgreiðsluprósentan í viðskiptamannsspjaldinu á eingöngu við ef engin prósenta er sett upp fyrir vöruna. Ef innihaldi reitsins **Fyrirframgreiðsla %** er hinsvegar breytt á sölu- eða innkaupahausnum eftir að búið er að stofna línurnar er fyrirframgreiðsluprósenta allra lína uppfærð. Á þennan hátt er auðveldara að stofna pöntun með fasta fyrirframgreiðsluprósentu, sama hvaða prósenta er uppsett í vörum.

## <a name="to-automatically-release-sales-orders-when-prepayments-are-applied"></a>Til að gefa út sölupantanir sjálfvirkt þegar fyrirframgreiðslur eru jafnaðar

Hægt er að spara tíma með því að setja upp verkraðarafærslu sem mun sjálfkrafa gefa út sölupantanir sem krefjast fyrirframgreiðslu eftir að greiðslum er beitt. Ef vinnslan er sjálfvirkt vistuð er skrefið að losa sölupöntunina.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. **Í fyrirframgr. Reiturinn Sjálfvirk uppfærslutíðni**, Tilgreinið hversu oft eigi að keyra verkraðarafærslu.

> [!TIP]
> Ef þú ert hér skaltu íhuga að bæta við safeguard gegn sendingu eða reikningsfærslum sem hafa ógreiddar forsöluupphæðir. Ef kveikt er á **ávísunarreglu** fyrir víxlun, [!INCLUDE[prod_short](includes/prod_short.md)] kemur ekki í veg fyrir að fólk bóki pantanir með útistandandi fyrirframgreiðsluupphæðum.

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
4. Uppsetning á **UPD. Fyrirframreikningur biðlauna Færsla í vinnslubiðröð sölu**, til dæmis, með því að nota stillingarnar á **endurtekningarflipanum** til að áætla hversu oft á að keyra hana. Frekari upplýsing er [í nota Starfaraðir til að áætla verk](admin-job-queues-schedule-tasks.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .  

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Reikna vöru- og þjónustuskatt á fyrirframgreiðslum í Ástralíu](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Reikna vöru- og þjónustuskatt á fyrirframgreiðslum á Nýja-Sjálandi](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Skilja fjárhag og bókhaldslykil](finance-general-ledger.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]