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
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540270"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota PowerApps.
Notandi getur gert [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín aðgengileg sem gagnaveitu í PowerApps.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)] við sem gagnaveitu í PowerApps
1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Á heimasíðunni skal velja sniðmátið **Byrja frá gögnum** til að búa til nýtt vinnusvæðaforrit. Þetta forrit verður hannað til notkunar í farsíma, en þú getur einnig valið að nota annað sniðmát.

    Næsta skrefið til að búa til PowerApp er að velja gögn. Veldu örtáknið og veldu svo valkostinn **Ný tenging** á efri hluta síðunnar, vinstra megin.
3. Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.

    PowerApps mun tengjast [!INCLUDE [prodshort](includes/prodshort.md)] með innskráningarupplýsingunum sem þú ert skráð(ur) inn með. Ef þú ert ekki stjórnandi á [!INCLUDE [prodshort](includes/prodshort.md)] þínu þarftu hugsanlega að skrá þig inn með öðrum reikningi.  

4. Ef þú hefur fleiri en eitt fyrirtæki í [!INCLUDE [prodshort](includes/prodshort.md)] þínu þarftu að velja fyrirtækið til að tengjast við. PowerApps birtir lista yfir *töflur* sem eru í boði frá [!INCLUDE [prodshort](includes/prodshort.md)]. Þessar svokölluðu töflur eru hluti af [!INCLUDE [prodshort](includes/prodshort.md)] API. Þú þarft ekki að stilla endapunkta sjálfur - [!INCLUDE [prodshort](includes/prodshort.md)] tengið fyrir PowerApps gerir það fyrir þig.  

    Ef þú vilt hafa með gögn úr öðrum töflum í [!INCLUDE [prodshort](includes/prodshort.md)] í forritinu þínu verður þú að vinna með þróunaraðila til að skilgreina sérsniðið API í [!INCLUDE [prodshort](includes/prodshort.md)] og síðan nota þetta sérsniðna API í gegnum sérsniðinn tengil í PowerApps. Nánari upplýsingar má finna í [Stofna sérsniðin tengi frá grunni](/connectors/custom-connectors/define-blank).  

Nú hefur þér tekist að tengjast gögnum þínum í [!INCLUDE [prodshort](includes/prodshort.md)] og getur byrjað að byggja upp PowerApp. Hægt er að bæta við fleiri skjáum og tengjast við fleiri gögn úr [!INCLUDE [prodshort](includes/prodshort.md)]. Nánari upplýsingar er að finna í [Búa til vinnusvæðaforrit úr sniðmáti í PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Nánari upplýsingar er að finna í [Vista og birta vinnusvæðaforrit í PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Ef þú vilt tengjast við [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.  

## <a name="see-also"></a>Sjá einnig

[Búa til vinnusvæðaforrit úr sniðmáti í PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
