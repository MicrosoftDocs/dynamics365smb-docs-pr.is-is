---
title: Setja upp upplýsingar um markaðssetningu og tengiliðastjórnun| Microsoft Docs
description: Hægt er að setja upp markaðssetningu og tengiliðastjórnun í Business Central til að hámarka ávinning sambanda við viðskiptamenn og viðföng, og bæta herferðir og kynningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8ed7c53d4352dcebc1475f4cafdd6a13db5385bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783435"
---
# <a name="setting-up-relationship-management"></a>Uppsetning tengslastjórnar

Áður en þú byrjar að vinna með tengiliði og markaðssetningarhagsmuni, eru nokkrar ákvarðanir og skref sem þú ættir að taka til að setja upp hvernig markaðssviðið stjórnar ákveðna þætti hjá tengiliðunum þínum. Til dæmis er hægt að ákveða hvort eigi að samstilla tengiliðarspjald við viðskiptamannaspjald, lánardrottnaspjald, og bankareikningsspjald, hvernig númeraraðir eru skilgreindar eða hvaða stöðluðu kveðju á að nota þegar skrifuð eru skeyti til tengiliðanna.

Með stjórnun tengiliða og gerð áætlunar til að finna, laða að og halda viðskiptamönnum má fínstilla rekstur fyrirtækisins og auka ánægju viðskiptamanna. Notkun góðs tengiliðastjórnunarkerfis hjálpar einnig til við stofnun og viðhald sambanda við viðskiptamenn. Samskipti eru lykillinn í slíkum samböndum. Nauðsynlegt er að geta sérsniðið samskipti við mögulega og núverandi viðskiptamenn, lánadrottna og viðskiptafélaga eftir þörfum þeirra, svo fyrirtæki dafni. Stofnun áætlunar og skilgreining á hvernig fyrirtækið notar tengiliðaupplýsingar er frumskref. Margir ólíkir hópar innan fyrirtækisins munu skoða þessar upplýsingar, og gott kerfi hjálpar öllum að auka framleiðni sína.

Þú setur upp stjórnun markaðssetningar og tengiliðar á síðunni **Uppsetning markaðssetningar**. Til að opna síðuna **Uppsetning markaðssetningar** skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slá inn **Uppsetning markaðssetningar** og velja síðan tengda tengilinn.

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Afritar ákveðnar upplýsingar sjálfkrafa úr tengiliðafyrirtækjum yfir til tengiliða.
Vissar upplýsingar um tengiliðafyrirtæki eru þær sömu og um einstaklingstengiliði sem vinna hjá fyrirtækjunum, til dæmis upplýsingar um aðsetur. Í hlutanum **Erfðir** á síðunni **Uppsetning markaðssetningar** geturðu stillt forritið til að afritað tiltekna reiti sjálfkrafa af fyrirtækistengiliðaspjaldinu á tengiliðaspjaldið í hvert sinn sem stofnaður er tengiliður fyrir tengiliðarfyrirtæki. Til dæmis er hægt að velja að afrita sölumannskóða, upplýsingar um aðsetur, upplýsinga um aðsetur (aðsetur, aðsetur 2, bæ, póstnúmer og sýslu) og samskiptaupplýsingar (faxnúmer, svarkóða á telex og símanúmer) og meira.

Þegar einhverjum þessara reita er breytt á fyrirtækistengiliðaspjaldi breytir forritið þeim sjálfkrafa á einstaklingstengiliðaspjaldinu (nema efni reitsins á einstaklingstengiliðaspjaldinu hafi verið breytt handvirkt).

Frekari upplýsingar eru í [Stofna tengiliði](marketing-create-contact-companies.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Nota forskilgreind sjálfgildi á nýja tengiliði
Hægt er að láta forritið tilgreina sjálfkrafa ákveðinn tungumálskóða, umsjónarsvæðiskóða, sölumannskóða og lands-/svæðiskóða sem sjálfgildi þegar nýir einstaklingstengiliðir eru stofnaðir. Einnig er hægt að færa inn sjálfgefinn söluferliskóta sem forritið úthlutar sjálfkrafa á hvert nýtt tækifæri sem stofnað er.

Reitaerfðir skrifast yfir sjálfgildi sem sett hafa verið upp. Ef enska hefur til dæmis verið sett upp sem sjálfgefið tungumál en tungumál tengiliðafyrirtækisins er þýska, úthlutar forritið þýsku sjálfkrafa sem tungumálakóta einstaklingstengiliðanna sem skráðir eru fyrir það fyrirtæki.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Samskipti skráð sjálfkrafa
[!INCLUDE[prod_short](includes/prod_short.md)] getur sjálfkrafa skráð sölu- og innkaupaskjöl sem samskipti (til dæmis pantanir, reikninga, móttökur og þess háttar), ásamt forsíðum, tölvupóstsendingum og símtölum.

Fyrir frekar upplýsingar, sjá [Skrá samskipti við tengiliði sjálfkrafa](marketing-auto-record-interactions.md)

## <a name="synchronizing-contacts-with-customers-and-more"></a>Tengiliðir samstilltir við viðskiptamenn og meira
Eigi að samstilla tengiliðaspjaldið við viðskiptamannaspjald, lánardrottnaspjald og bankareikningsspjald þarf að velja viðskiptatengslakóta fyrir viðskiptamenn, lánardrottna og bankareikninga. Þannig er til dæmis aðeins hægt að tengja tengilið við viðskiptamann sem til er fyrir hafi viðskiptatengslakóti fyrir viðskiptamenn verið valinn á síðunni **uppsetning markaðssetningar**.

Fyrir frekar upplýsingar, sjá [Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts)  

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Úthluta Númeraraðir á tengiliði og tækifæri
Hægt er að setja upp númeraraðir fyrir tengiliði og tækifæri. Hafi númeraröð verið sett upp fyrir tengiliði færir kerfið sjálfkrafa inn númer. reitur á tengiliðaspjaldinu setur forritið sjálfkrafa inn næsta lausa tengiliðanúmer.

Frekari upplýsingar um númeraraðir er að finna á [stofna númeraraðir](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Leita að tvíteknum tengiliðum þegar tengiliðir eru stofnaðir
Hægt er að láta forritið leita sjálfkrafa leita að tvítekningum í hvert sinn þegar stofnað er tengiliðafyrirtæki eða leita handvirkt eftir að tengiliðirnir hafa verið stofnaðir. Einnig er hægt að láta forritið uppfæra leitarstrengi sjálfkrafa í hvert sinn sem tengiliðaupplýsingum er breytt eða tengiliður stofnaður. Notandinn ákveður sjálfur hver endurtekningarprósentan er, það er hlutfall strengja sem verða að vera eins hjá tveimur tengiliðum til þess að forritið líti á þá sem tvítekningar.

## <a name="see-also"></a>Sjá einnig
[Vinna með tengiliði](marketing-contacts.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]