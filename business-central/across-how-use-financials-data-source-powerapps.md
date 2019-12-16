---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881001"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps.

Notandi getur gert [!INCLUDE[prodshort](includes/prodshort.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power Apps.  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a>Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power Apps

1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/) í vafranum og skráið ykkur svo inn.
2. Á heimasíðunni skal velja **Forrit**, **Búa til forrit** og **Vinnusvæði** til að búa til nýtt vinnusvæðisforrit. Þetta forrit verður hannað til notkunar í farsíma, en þú getur einnig valið að nota annað sniðmát.

    Næsta skrefið til að búa til Power App er að velja gögn. Veldu örtáknið og veldu svo valkostinn **Ný tenging** á efri hluta síðunnar, vinstra megin.
3. Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.

    Power Apps mun tengjast [!INCLUDE [prodshort](includes/prodshort.md)] með innskráningarupplýsingunum sem þú ert skráð(ur) inn með. Ef þú ert ekki stjórnandi á [!INCLUDE [prodshort](includes/prodshort.md)] þínu þarftu hugsanlega að skrá þig inn með öðrum reikningi.  

4. Power Apps mun birta lista yfir *umhverfi og fyrirtæki* sem eru tiltæk í [!INCLUDE [prodshort](includes/prodshort.md)]. Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við. Næst færðu að sjá lista yfir API. Veldu **API** sem þú vilt tengjast við.

Þessar svokölluðu töflur eru hluti af [!INCLUDE [prodshort](includes/prodshort.md)] API. Þú þarft ekki að stilla endapunkta sjálfur - [!INCLUDE [prodshort](includes/prodshort.md)] tengill fyrir Power Apps gerir það fyrir þig.  

> [!NOTE]
> Ef þú vilt hafa með gögn úr öðrum töflum í [!INCLUDE [prodshort](includes/prodshort.md)] í forritinu þínu verður þú að vinna með þróunaraðila til að skilgreina sérsniðið API í [!INCLUDE [prodshort](includes/prodshort.md)] og síðan nota þetta sérsniðna API í gegnum sérsniðinn tengil í Power Apps. Nánari upplýsingar má finna í [Stofna sérsniðin tengi frá grunni](/connectors/custom-connectors/define-blank).  

Nú hefur þér tekist að tengjast gögnum þínum í [!INCLUDE [prodshort](includes/prodshort.md)] og getur byrjað að byggja upp PowerApp. Hægt er að bæta við fleiri skjáum og tengjast við fleiri gögn úr [!INCLUDE [prodshort](includes/prodshort.md)]. Frekari upplýsingar er að finna á [Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Ef þú vilt tengjast við [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.  

## <a name="see-also"></a>Sjá einnig

[Búa til vinnusvæðaforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
