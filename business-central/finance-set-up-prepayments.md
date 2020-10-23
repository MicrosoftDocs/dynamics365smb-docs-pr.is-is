---
title: Fyrirframgreiðslur | Microsoft Docs
description: Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram. Þú gætir krafist innborgunar áður en þú framleiðir vörur upp í pöntun eða krafist greiðslu áður en þú afhendir viðskiptamanni vörur. Með fyrirframgreiðslum getur þú reikningsfært og innheimt innborganir frá viðskiptamönnum eða sent lánardrottnum innborganir. Þannig má tryggja að allar greiðslur séu bókaðar á móti reikningi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: prepayment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7f8d0109b42eb75f022bac580c2bef006f311157
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914240"
---
# <a name="set-up-prepayments"></a>Uppsetning fyrirframgreiðslu
Ef viðskiptavinir þurfa inna greiðslu af hendi áður en þeir fá pöntun afhenta eða ef lánardrottinn fer fram á greiðslu áður en hann afhendir pöntun er hægt að nota aðgerðina Fyrirframgreiðsla. Með þessari verkun getur þú reikningsfært og innheimt innborganir frá viðskiptamönnum eða sent lánardrottnum innborganir, og verið viss að allar hlutagreiðslur séu bókaðar til móts við reikning. Nánari upplýsingar eru í [Búa til fyrirframgreiðslureikninga](finance-how-to-create-prepayment-invoices.md).

Áður en þú getur bókað fyrirframgreiðslureikning verður þú að setja upp bókunarreikningana í fjárhag og númeraraðir fyrir fyrirframgreiðsluskjöl. Þú verður að tilgreina reikning fyrir fyrirframgreiðslur sem tengjast sölu og reikningi fyrir fyrirframgreiðslur sem tengjast innkaupum. Þú getur tilgreint sömu bókunarreikninga til notkunar fyrir allar fyrirframgreiðslur sem tengjast öllum almennum viðskiptabókunarflokkum eða almennum vörubókunarflokkum, eða þú getur tilgreint tiltekna reikninga fyrir tilteknar bókunarflokka fyrir sölu og innkaup. Þetta fer eftir kröfum fyrirtækisins þíns varðandi rakningu fyrirframgreiðslna.  

Þú getur tilgreint prósentu línuupphæðarinnar sem verður reikningsfærð, fyrir viðskiptamann eða lánardrottin fyrir allar vörur eða valdar vörur. Þegar uppsetningu er lokið er hægt að búa til fyrirframgreiðslureikninga úr sölu- og innkaupapöntunum. Þú getur notað skilgreindu prósenturnar fyrir hverja sölu- eða innkaupalínu eða breytt upphæðunum á reikningnum eins og þarf. Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

> [!NOTE]
> Mælt er með því að ekki sé notuð 100% prósenta fyrirframgreiðslu í eftirfarandi tilvikum:
> * Ef þú ert í Norður-Ameríku. Vegna þess hvernig skattar eru reiknaðir er prósenta fyrirframgreiðslu 100% sem getur leitt til vandamál með fyrirframgreiðslureikninga.
> * Á öllum svæðum, ef greiðsluafsláttur er handvirkt dreginn frá reikningi. Fyrirframgreiðsluprósenta 100% mun ekki sjálfkrafa skilja eftir upphæð sem draga þarf afsláttinn frá. 

Þar sem fyrirframgreidd upphæð tilheyrir kaupanda þar til hann hefur móttekið vörur eða þjónustu þarf að setja upp fjárhagsreikninga til að geyma fyrirframgreiðsluupphæðir þar til lokareikningurinn er bókaður. Sölufyrirframgreiðslur þarf að skrá í skuldareikning þar til vörurnar eru afhentar. Fyrirframgreiðslur innkaupa þarf að skrá í eignareikning þar til vörurnar eru mótteknar. Auk þess þarf að setja upp sérstakan fjárhagsreikning fyrir hvert VSK-kenni.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Bæta fyrirframgreiðslureikningum við almennan bókunargrunn  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Almennur bókunargrunnur** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning almennar bókunar** er fyllt út í eftirfarandi reiti:  

    - **Fyrirframgreiðslureikn. sölu**  
    - **Fyrirframgr.reikn. innkaupa**  

> [!TIP]
> Ef þú getur ekki séð reitina á síðunni **Uppsetning bókunargrunns** notaðu þá lárétta flettistiku neðst á síðunni til að fletta til hægri.  

Ef almennir fjárhagsreikningar hafa ekki enn verið settir upp fyrir fyrirframgreiðslur er hægt að fara á síðuna **Fjárhagsreikningalisti** frá viðeigandi reit reiknings.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Uppsetning númeraraðar fyrir fylgiskjöl fyrirframgreiðslu  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugrunnur** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning Sala & útistandandi** er fyllt út í eftirfarandi reiti:  

   - **Bókuð fyrirframgr.reikn.nr.**
   - **Bókuð kr.reikn.nr. fyrirframgr.**

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning innkaupagrunns** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning innkaupa & Viðskiptaskuldir** er fyllt út í eftirfarandi reiti:

    - **Bókaður fyrirframgr.reikn.nr.**
    - **Bókaður kr.reikn.nr. fyrirframgr.**

> [!NOTE]  
> Hægt er að nota sömu númeraröð fyrir fyrirframgreiðslureikninga og venjulega reikninga, auk þess sem hægt er að nota mismunandi númeraraðir. Ef mismunandi raðir eru notaðar mega þær ekki skarast, númer má ekki vera í meira en einni röð.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Að setja upp fyrirframgreiðsluprósentu fyrir vörur, viðskiptamenn og lánardrottna  
Fyrir vöru er hægt að setja upp sjálfgefna fyrirframgreiðsluprósentu fyrir alla viðskiptamenn, tiltekinn viðskiptamann eða verðflokk viðskiptamanns.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Veljið Atriði og veljið svo aðgerðina **Fyrirframgreiðsluprósenta**.  
3. Á síðunni **Sala fyrirframgreiðsluprósenta** skal fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Fyrir viðskiptamann eða lánardrottin er hægt að setja upp eina sjálfgefna prósentu fyrirframgreiðslu fyrir allar vörur og allar tegundir sölulína. Þú færir þetta inn á viðskiptamanna eða lánardrottna kortið.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna spjaldið fyrir viðskiptamann.
3. **Fyrirframgreiðsla %** er fært inn í reitinn .
4. Skrefin eru endurtekin fyrir aðra viðskiptamenn og lánardrottna.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Til að ákvarða hvaða fyrirframgreiðsluprósenta hefur forgang  

Pöntun getur haft prósentu fyrirframgreiðslu í söluhausnum og aðra prósentu fyrir vörurnar í línunni. Til að ákvarða hvaða fyrirframgreiðsluprósentu á að nota við hverja sölulínu leitar kerfið að fyrirframgreiðsluprósentu í eftirfarandi röð, og notar svo fyrsta sjálfgildið sem það finnur:  

1. Fyrirframgreiðsluprósentu fyrir vöruna í línunni og viðskiptamanninn sem pöntunin er fyrir.  
2. Fyrirframgreiðsluprósentu fyrir vöruna í línunni og verðflokk viðskiptamanna sem viðskiptamaðurinn tilheyrir.  
3. Fyrirframgreiðsluprósentu fyrir vörunar í línunni fyrir alla viðskiptamenn.  
4. Fyrirframgreiðsluprósentan í sölu- eða innkaupahausnum.  

Með öðrum orðum, fyrirframgreiðsluprósentan í viðskiptamannsspjaldinu á eingöngu við ef engin prósenta er sett upp fyrir vöruna. Ef innihaldi reitsins **Fyrirframgreiðsla %** er hinsvegar breytt á sölu- eða innkaupahausnum eftir að búið er að stofna línurnar er fyrirframgreiðsluprósenta allra lína uppfærð. Á þennan hátt er auðveldara að stofna pöntun með fasta fyrirframgreiðsluprósentu, sama hvaða prósenta er uppsett í vörum.

## <a name="see-also"></a>Sjá einnig  

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Reikna vöru- og þjónustuskatt á fyrirframgreiðslum í Ástralíu](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Reikna vöru- og þjónustuskatt á fyrirframgreiðslum á Nýja-Sjálandi](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Skilja fjárhag og bókhaldslykil](finance-general-ledger.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
