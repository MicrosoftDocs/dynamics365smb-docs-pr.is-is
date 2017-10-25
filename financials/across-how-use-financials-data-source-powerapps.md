---
title: "Nota gögn til að stofna forrit| Microsoft Docs"
description: "Notandi getur gert Financials gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota PowerApps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e41a704d3a94abfb58d9547648f0eee46a8ed9b4
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="connecting-to-your-financials-data-to-build-a-business-app-using-powerapps"></a>Tengjast við Financials gögnin til að búa til viðskiptaforrit með því að nota PowerApps.
Notandi getur gert [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín aðgengileg sem gagnaveitu í PowerApps.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)] við sem gagnaveitu í PowerApps
1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Á vinstra yfirlitssvæðinu skal velja **Nýtt forrit**.
3. Veldur ritilinn þinn, PowerApps Studio fyrir Windows eða PowerApps Studio fyrir vefinn.

   PowerApps Studio fyrir Windows er skjáborðsforrit sem notað er til að stofna og birta PowerApps. PowerApps Studio fyrir vef er skjáborðsforrit sem notað er til að stofna og birta PowerApps.
4. Næsta skrefið til að búa til PowerApp er að velja gögn. Veldu örtáknið og veldu svo valkostinn **Ný tenging** á efri hluta síðunnar, vinstra megin.
5. Úr lista yfir tiltækar tengingar skal velja **Dynamics 365 for Financials**.
6. PowerApps birtir tengisíðu sem sendir áminningu um upplýsingarnar sem gefa þarf upp til að tengja notanda við [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín. Til að tengjast verður að tilgreina OData-vefslóð, notandanafn, aðgangsorð og heiti fyrirtækis.

   Til að finna *OData vefslóð* getur notandi afritað OData V4 vefslóð fyrir hverja þeirra vefþjónusta sem taldar eru upp á síðunni **Vefþjónustur** í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Fyrir *Fyrirtækisheiti* skal nota heitið sem birtist í reitnum **Heiti** í glugganum **Stofngögn** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] notanda inniheldur mörg fyrirtæki skal velja viðeigandi heiti fyrirtækis af listanum í glugganum **Fyrirtæki**. Í báðum tilvikum skal gæta þess að heitið sem notandi tilgreinir í leiðsagnarforritinu fyrir PowerApps samsvari nákvæmlega textanum sem birtist í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `My Company`.

   Fyrir notandanafn og aðgangsorð skal nota nafnið og aðgangslykil vefþjónustu sem tilgreind eru í reikningnum í glugganum **Notendur** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis, notandanafnið þitt er *ADMIN*, og aðgangslykill vefþjónustu sem virkar sem aðgangsorð er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Veldu hnappinn **Tenging** til að halda áfram. PowerApps birtir sjálfgefið gagnamengi fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Veljið gagnamengið **Sjálfgefið**.

   PowerApps birtir lista yfir töflur sem eru tiltækar úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessar töflur eða endapunktar tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.
8. Veldu töfluna sem á að nota fyrir þitt PowerApp og veldu svo hnappinn **Tengja**.
9. Endurtaktu fyrri skref til að bæta fleiri [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnum við Power Bi-gagnalíkanið þitt.

   > [!NOTE]  
>    Þegar notanda hefur tekist að tengjast [!INCLUDE[d365fin](includes/d365fin_md.md)] verður hann ekki beðinn aftur um OData-vefslóð, notandanafn eða aðgangsorð.

Nú hefur notanda tekist að tengjast gögnum sínum í Dynamics 365 og getur byrjað að byggja upp PowerApp. Frekari upplýsingar eru í [PowerApps skjölum](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Sjá einnig
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

