---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota PowerApps.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: be1f5c64cefdcd4cb9a14c0c2f1c559e426ce0f8
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "938345"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota PowerApps.
Notandi getur gert [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín aðgengileg sem gagnaveitu í PowerApps.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)] við sem gagnaveitu í PowerApps
1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Á vinstra yfirlitssvæðinu skal velja **Nýtt forrit**.
3. Veldur ritilinn þinn, PowerApps Studio fyrir Windows eða PowerApps Studio fyrir vefinn.

   PowerApps Studio fyrir Windows er skjáborðsforrit sem notað er til að stofna og birta PowerApps. PowerApps Studio fyrir vef er skjáborðsforrit sem notað er til að stofna og birta PowerApps.
4. Næsta skrefið til að búa til PowerApp er að velja gögn. Veldu örtáknið og veldu svo valkostinn **Ný tenging** á efri hluta síðunnar, vinstra megin.
5. Úr lista yfir tiltækar tengingar skal velja **Dynamics 365 Business Central**.
6. PowerApps birtir tengisíðu sem sendir áminningu um upplýsingarnar sem gefa þarf upp til að tengja notanda við [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín. Til að tengjast verður að tilgreina OData-vefslóð, notandanafn, aðgangsorð og heiti fyrirtækis.

   Fyrir *OData vefslóð* getur notandi afritað OData V4 vefslóð fyrir hverja þá vefþjónustu sem talin er upp á síðunni **Vefþjónustur** í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `https://mycompany.businesscentral.dynamics.com:7048/MS/ODataV4/`.  

   Fyrir *Fyrirtækisheiti* skal nota heitið sem birtist í reitnum **Heiti** á síðunni **Stofngögn** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] notanda inniheldur mörg fyrirtæki skal velja viðeigandi heiti fyrirtækis af listanum á síðunni **Fyrirtæki**. Í báðum tilvikum skal gæta þess að heitið sem notandi tilgreinir í leiðsagnarforritinu fyrir PowerApps samsvari nákvæmlega textanum sem birtist í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `My Company`.

   Fyrir notandanafn og aðgangsorð skal nota nafnið og aðgangslykil vefþjónustu sem tilgreind eru í reikningnum á síðunni **Notendur** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis, notandanafnið þitt er *ADMIN*, og aðgangslykill vefþjónustu sem virkar sem aðgangsorð er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Veldu hnappinn **Tenging** til að halda áfram. PowerApps birtir sjálfgefið gagnamengi fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Veljið gagnamengið **Sjálfgefið**.

   PowerApps birtir lista yfir töflur sem eru tiltækar úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessar töflur eða endapunktar tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.
8. Veldu töfluna sem á að nota fyrir þitt PowerApp og veldu svo hnappinn **Tengja**.
9. Endurtaktu fyrri skref til að bæta fleiri [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnum við Power BI-gagnalíkanið þitt.

   > [!NOTE]  
   >    Þegar notanda hefur tekist að tengjast [!INCLUDE[d365fin](includes/d365fin_md.md)] verður hann ekki beðinn aftur um OData-vefslóð, notandanafn eða aðgangsorð.

Nú hefur notanda tekist að tengjast gögnum sínum í Business Central og getur byrjað að byggja upp PowerApp. Frekari upplýsingar eru í [PowerApps skjölum](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Sjá einnig
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
