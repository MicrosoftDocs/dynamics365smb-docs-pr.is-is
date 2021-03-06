---
title: Stofna verksölureikning til að reikningsfæra verk| Microsoft Docs
description: Lýsir því hvernig skal reikningsfæra viðskiptamenn fyrir verkútgjöld þegar á verkið líður.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 873135d2fa6053b7101a999981fb3117ee8689ab
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938147"
---
# <a name="invoice-jobs"></a>Reikningsfærsla verka
Meðan á verkefninu stendur getur kostnaður vegna forðanotkunar, efnis og verktengdra innkaupa safnast upp. Þessar færslur eru bókaðar í verkbókina á vinnslutíma verksins. Mikilvægt er að allur kostnaður sé skráður í verkbókina áður en viðskiptavininum er sendur reikningur.

> [!NOTE]
> Einnig er hægt að kaupa ytri tilföng sem eru ótengd verki, t.d. til að senda reikning á lánardrottin fyrir afhenta vinnu. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).

Hægt er að reikningsfæra allt verkið á síðunni **Verkhlutalínur** eða aðeins reikningsfæra ákveðnar reikningshæfar línur á síðunni **Áætlunarlínur**. Hægt er að reikningsfæra þegar verkinu er lokið eða með vissu millibili á meðan á vinnslu verksins stendur, byggt á reikningsáætlun.

> [!NOTE]  
> Ef valið er **Reikningshæft** í reitnum **Verklínutegund** í söluskjölum fyrir verktengd innkaup verða stofnaðar verkáætlunarlínur sem eru tilbúnar til að vera reikningsfærðar á viðskiptamann. Frekari upplýsingar eru í [Sjá um birgðir verkefna](projects-how-manage-project-supplies.md).

## <a name="to-create-multiple-job-sales-invoices"></a>Að búa til marga sölureikninga verks
Hægt er að stofna reikning fyrir verk eða einn eða fleiri verkhluta fyrir viðskiptavin þegar verkinu sem á að reikningsfæra er lokið eða komið er að dagsetningu reikningafærslunnar, sem byggist á reikningsfærsluáætlun.

Eftirfarandi ferli sýnir hvernig á að nota keyrslu til að reikningsfæra fleiri verk.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stofna sölureikning verks** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Ef takmarka á verk sem keyrslan á að vinna skal tilgreina afmarkanir.
4. Velja hnappinn **Í lagi** til að stofna reikningana.  

Hægt er að yfirfara og bóka stofnaða reikninga í glugganum **Sölureikningar**.

> [!NOTE]
> Einnig er hægt að reikningsfæra til viðskiptamanns með því að velja verkið og velja svo aðgerðina **Stofna sölureikning verks**. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Að búa til og bóka sölureikninga verks úr verkáætlunarlínum
Hægt er að stofna reikning úr verkáætlunarlínum, og gefa upp á þeim tíma magnið af vörunni, forða eða fjárhagsreikning sem á að reikningsfæra.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.
2. Opnið viðeigandi verk.
3. Valinn er verkhluti þar sem reiturinn **Verkhlutagerð** inniheldur **Bókuð** og svo er aðgerðin **Verkhlutalínur** valin.  
4. Í verkáætlunarlínu í reitnum **Magn Til að reikningsfæra** er slegið inn magn vörunnar, forðann, fjárhagsreikningsgerð sem á að reikningsfæra.  
5. Veljið aðgerðina **Stofna sölureikning**.
6. Á síðunni **Stofna sölureikning verks** færirðu inn bókunardagsetninguna og hvort eigi að stofna nýjan reikning eða skeyta þessum reikningi við fyrirliggjandi reikning.
7. Velja hnappinn **Í lagi**.  
8. Á síðunni **Verkáætlunarlínur** skal velja aðgerðina **Sölureikningar/kreditreikningar**.

    Síðan **Sölureikningur** opnast og sýnir það magn sem hefur verið flutt á reikninginn.
9. Gerið frekari breytingar og veljið svo aðgerðina **Bóka**.

> [!NOTE]  
>   Ofangreint ferli er svipað þegar verið er að stofna, yfirfara og bóka verktengdan sölukreditreikning.


## <a name="see-also"></a>Sjá einnig
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
