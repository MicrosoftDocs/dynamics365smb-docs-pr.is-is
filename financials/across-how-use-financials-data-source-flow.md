---
title: "Að nota Dynamics 365 for Financials í Microsoft Flow | Microsoft Docs"
description: "Notandi getur gert Financials-gögnin sín aðgengileg sem gagnaveitu í Power Apps."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 76d24ed80adb08083c6167040be8cc6a4bcc3167
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-in-microsoft-flow"></a>Notkun Dynamics 365 for Financials í Microsoft Flow
Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.  

**Athugið:**: Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)]við sem gagnaveitu í flæði
1. Flettið í [flow.microsoft.com](https://flow.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Veldu **Mitt flæði** af borðanum efst á síðunni.
3. Í glugganum **Mitt flæði** skal velja valkostinn **Stofna úr auðu**.
4. Farðu í lista yfir tiltækar kveikjur og veldu eina af tveimur [!INCLUDE[d365fin](includes/d365fin_md.md)] tiltækum kveikjum: *Þegar færsla er stofnuð*, eða *Þegar færslu er breytt*.
5. Flow birtir tengisíðu sem sendir áminningu um upplýsingarnar sem gefa þarf upp til að tengja notanda við [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín. Til að tengjast verður notandi að tilgreina heiti fyrir tenginguna, OData vefslóð, notandanafn, aðgangsorð og heiti fyrirtækis.

   Til að finna *OData vefslóð* getur notandi afritað OData V4 vefslóð fyrir hverja þeirra vefþjónusta sem taldar eru upp á síðunni **Vefþjónustur** í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Fyrir *Fyrirtækisheiti* skal nota heitið sem birtist í reitnum **Heiti** í glugganum **Stofngögn** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] notanda inniheldur mörg fyrirtæki skal velja viðeigandi heiti fyrirtækis af listanum í glugganum **Fyrirtæki**. Í báðum tilvikum skal gæta þess að heitið sem notandi tilgreinir í leiðsagnarforritinu fyrir PowerApps samsvari nákvæmlega textanum sem birtist í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `My Company`.

   Fyrir notandanafn og aðgangsorð skal nota nafnið og aðgangslykil vefþjónustu sem tilgreind eru í reikningnum í glugganum **Notendur** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis, notandanafnið þitt er *ADMIN*, og aðgangslykill vefþjónustu sem virkar sem aðgangsorð er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Nánari upplýsingar eru í [Hvernig á að: Vinna með notendur og heimildir](ui-how-users-permissions.md).
6. Veljið hnappinn **Stofna** neðst á síðunni til að halda áfram.

   Flow birtir þá lista yfir töflur sem eru aðgengilegar úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessar töflur eða endapunktar tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.
7. Velja gögnin sem á að nota í Flow.

Nú hefur notanda tekist að tengjast gögnum sínum í Dynamics 365 og getur byrjað að byggja upp flæðið. Frekari upplýsingar eru í [gögnum um Flow](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Sjá einnig
[Velkomin í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](upload-data.md)  
[Hvernig á að: Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

