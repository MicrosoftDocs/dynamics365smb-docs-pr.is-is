---
title: Skrá útgjöld og tekjur beint í fjárhag| Microsoft Docs
description: Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í , eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu á síðunni Fjárhagur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e0beff15352fb8e57f57c9d0ffdcd76bc28afbb9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782380"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a>Bóka færslu beint í Fjárhag

Nota færslubækur til bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga.  

Hefðbundin notkun færslubókarinnar er að bóka starfsmannaútgjöld, þar sem þeir nota eigin peninga í viðskiptaerindum, fyrir seinni tíma endurgreiðslu. Nánari upplýsingar eru í [Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).

Færslubækur bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum. Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki. Hægt er að sérsníða þína útgáfu af færslubók með því að setja upp bókakeyrslu eða sniðmát. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).

Ólíkt því sem gerist þegar færslur eru bókaðar með fylgiskjölum, sem krefst kreditreikningsferlis, getur þú réttilega bakfært færslur sem eru bókaðar með fjárhagnum. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Að bóka færslu beint í fjárhagsreikning

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.
2. Viðeigandi færslubók keyrsla er opnaður. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).
3. Fyllið í reitina eftir þörfum í nýrri færslubókarlínu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Endurtakið skref 3 fyrir allar aðskildar færslur sem þú vilt bóka.

    > [!TIP]  
    > Ef þú vilt færa inn fleiri færslulínur fyrir ofan eina mótreikningslínu, til dæmis fyrir einn bankareikning, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu á síðunni **færslubókakeyrslur**. Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna skjalið.
5. Veljið **Bóka** aðgerðina til að skrá færslurnar á tilteknu fjárhagsreikningana.

## <a name="see-also"></a>Sjá einnig

[Vinna í færslubókum](ui-work-general-journals.md)  
[Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]