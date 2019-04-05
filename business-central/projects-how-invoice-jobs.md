---
title: Stofna verksölureikning til að reikningsfæra verk| Microsoft Docs
description: Lýsir því hvernig skal reikningsfæra viðskiptamenn fyrir verkútgjöld þegar á verkið líður.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 73894bb8c7193d96ca1f4c4f7c8b8394b1f26f5f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799577"
---
# <a name="invoice-jobs"></a>Reikningsfærsla verka
Meðan á verkefninu stendur getur kostnaður vegna forðanotkunar, efnis og verktengdra innkaupa safnast upp. Þessar færslur eru bókaðar í verkbókina á vinnslutíma verksins. Mikilvægt er að allur kostnaður sé skráður í verkbókina áður en viðskiptavininum er sendur reikningur.

Hægt er að reikningsfæra allt verkið á síðunni **Verkhlutalínur** eða aðeins reikningsfæra ákveðnar reikningshæfar línur á síðunni **Áætlunarlínur**. Hægt er að reikningsfæra þegar verkinu er lokið eða með vissu millibili á meðan á vinnslu verksins stendur, byggt á reikningsáætlun.

> [!NOTE]  
>   Ef valið er **Reikningshæft** í reitnum **Verklínutegund** í söluskjölum fyrir verktengd innkaup verða stofnaðar verkáætlunarlínur sem eru tilbúnar til að vera reikningsfærðar á viðskiptamann. Frekari upplýsingar eru í [Sjá um birgðir verkefna](projects-how-manage-project-supplies.md).

## <a name="to-create-and-post-a-job-sales-invoice"></a>Til að stofna og bóka sölureikning verks:
Hægt er að stofna reikning fyrir verk eða einn eða fleiri verkhluta fyrir viðskiptavin þegar verkinu sem á að reikningsfæra er lokið eða komið er að dagsetningu reikningafærslunnar, sem byggist á reikningsfærsluáætlun.

Á síðunni **Verk** er hægt að reikningsfæra til viðskiptamanns með því að velja verkið og velja svo aðgerðina **Stofna sölureikning verks**. Eftirfarandi ferli sýnir hvernig á að nota keyrslu til að reikningsfæra fleiri verk.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk - Stofna sölureikning** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Ef takmarka á verk sem keyrslan á að vinna skal tilgreina afmarkanir.
4. Velja hnappinn **Í lagi** til að stofna reikningana.  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a>Að búa til fleiri sölureikninga úr verkáætlunarlínum
Hægt er að stofna reikning úr verkáætlunarlínum, og gefa upp á þeim tíma magnið af vörunni, forða eða fjárhagsreikning sem á að reikningsfæra.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.
2. Opnið viðeigandi verk.
3. Valinn er verkhluti þar sem reiturinn **Verkhlutagerð** inniheldur **Bókuð** og svo er aðgerðin **Verkhlutalínur** valin.  
4. Í verkáætlunarlínu í reitnum **Magn Til að reikningsfæra** er slegið inn magn vörunnar, forðann, fjárhagsreikningsgerð sem á að reikningsfæra.  
5. Veljið aðgerðina **Stofna sölureikning**.
6. Á síðunni **Stofna sölureikning verks** færirðu inn bókunardagsetninguna og hvort eigi að stofna nýjan reikning eða skeyta þessum reikningi við fyrirliggjandi reikning.
7. Velja hnappinn **Í lagi**.  

    Í reitnum **Magn flutt á reikning** í verkáætlunarlínunni er hægt að sjá magnið.
8. Á síðunni **Verkáætlunarlínur** skal velja aðgerðina **Sölureikningar/kreditreikningar**.

    Síðan **Sölureikningur** opnast og sýnir það magn sem hefur verið flutt á reikninginn.  
9. Gerið frekari breytingar og veljið svo aðgerðina **Bóka**.

> [!NOTE]  
>   Ofangreint ferli er svipað þegar verið er að stofna, yfirfara og bóka verktengdan sölukreditreikning.

## <a name="to-calculate-and-post-job-completion-entries"></a>Að reikna út og bóka verklokafærslur
Þegar öllum aðgerðum verks hefur verið lokið, þar með talin bókun notkunar og reikningsfærsla, þarf að uppfæra verkið svo að **Staða** þess sé **Lokið**. Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið opið verk og veljið svo aðgerðina **Breyta**.
3. Í reitnum **Staða** skal velja **Lokið**.
4. Fylgið aðstoðarskrefunum til að reikna og bóka VÍV. Einnig er hægt að fylgja skrefum 5 og 6 til að gera það handvirkt.  
5. Veljið aðgerðina **Reikna VÍV**.
6. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.  

     VÍV færslurnar sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær séu lokafærslur.  
7. Velja skal aðgerðina **Verk - Bóka VÍV í fjárhag**.
8. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  

     VÍV-fjárlagsfærslur verks sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær eru lokafærslur.

## <a name="see-also"></a>Sjá einnig
[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
