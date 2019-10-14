---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305025"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota PowerApps
Notandi getur gert [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín aðgengileg sem gagnaveitu í PowerApps.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá PowerApps.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)] við sem gagnaveitu í PowerApps
1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Á heimasíðunni skal velja **Forrit**, **Búa til forrit** og **Vinnusvæði** til að búa til nýtt vinnusvæðisforrit. Þetta forrit verður hannað til notkunar í farsíma, en þú getur einnig valið að nota annað sniðmát.

    Næsta skrefið til að búa til PowerApp er að velja gögn. Veldu örtáknið og veldu svo valkostinn **Ný tenging** á efri hluta síðunnar, vinstra megin.
3. Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.

    PowerApps mun tengjast [!INCLUDE [prodshort](includes/prodshort.md)] með því að nota skilríkin sem notandi er skráður inn í með. Ef þú ert ekki stjórnandi á [!INCLUDE [prodshort](includes/prodshort.md)] þínu þarftu hugsanlega að skrá þig inn með öðrum reikningi.  

4.  PowerApps mun birta lista yfir *umhverfi og fyrirtæki* sem eru tiltæk í [!INCLUDE [prodshort](includes/prodshort.md)]. Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við. Næst færðu að sjá lista yfir API. Veldu **API** sem þú vilt tengjast við.

Þessar svokölluðu töflur eru hluti af [!INCLUDE [prodshort](includes/prodshort.md)] API. Þú þarft ekki að grunnstilla endapunktana sjálf(ur) - [!INCLUDE [prodshort](includes/prodshort.md)] tengillinn fyrir PowerApps gerir það fyrir þig.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

Nú hefur þér tekist að tengjast gögnum þínum í [!INCLUDE [prodshort](includes/prodshort.md)] og getur byrjað að byggja upp PowerApp. Hægt er að bæta við fleiri skjáum og tengjast við fleiri gögn úr [!INCLUDE [prodshort](includes/prodshort.md)]. Frekari upplýsingar er að finna á [Búa til vinnusvæðisforrit úr sniðmáti í PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Ef þú vilt tengjast við [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.  

## <a name="see-also"></a>Sjá einnig

[Búa til vinnusvæðisforrit úr sniðmáti í PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
