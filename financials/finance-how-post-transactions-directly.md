---
title: "Skrá útgjöld og tekjur beint í fjárhag| Microsoft Docs"
description: "Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í, eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu í glugganum Fjárhagur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 43065620f34a7ef02e5247e78acf306500f82d90
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Hvernig skal: Bóka færslu beint í Fjárhag
Flestar fjárhagsfærslur eru bókaðar í fjárhag gegnum sérstök viðskiptaskjöl, eins og innkaupareikninga og sölupantanir. Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í [!INCLUDE[d365fin](includes/d365fin_md.md)], eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu í glugganum **Fjárhagur**.

Hefðbundin notkun færslubókarinnar er að bóka starfsmannaútgjöld, þar sem þeir nota eigin peninga í viðskiptaerindum, fyrir seinni tíma endurgreiðslu. Nánari upplýsingar eru í [Hvernig á að: Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).

Færslubækur bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum. Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki. Hægt er að sérsníða þína útgáfu af færslubók með því að setja upp bókakeyrslu eða sniðmát. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).

Ólíkt því sem gerist þegar færslur eru bókaðar með fylgiskjölum, sem krefst kreditreikningsferlis, getur þú réttilega bakfært færslur sem eru bókaðar með fjárhagnum. Frekari upplýsingar, sjá [Hvernig skal: Bakfæra bókanir](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Að bóka færslu beint í fjárhagsreikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.
2. Viðeigandi færslubók keyrsla er opnaður. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).
3. Fyllið í reitina eftir þörfum í nýrri færslubókarlínu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Endurtakið skref 3 fyrir allar aðskildar færslur sem þú vilt bóka.

    > [!TIP]  
    > Ef þú vilt færa inn fleiri færslulínur fyrir ofan eina mótreikningslínu, til dæmis fyrir einn bankareikning, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu í glugganum **færslubókakeyrslur**. Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna skjalið.
5. Veljið **Bóka** aðgerðina til að skrá færslurnar á tilteknu fjárhagsreikningana.

## <a name="see-also"></a>Sjá einnig
[Vinna í færslubókum](ui-work-general-journals.md)  
[Hvernig á að: Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).  
[Hvernig skal: Bakfæra bókanir](finance-how-reverse-journal-posting.md).  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

