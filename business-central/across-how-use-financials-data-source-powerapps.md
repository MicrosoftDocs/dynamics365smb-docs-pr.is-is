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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5d2e6b75978d9aced7636b41623365f3d98ed3aa
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754493"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps

Notandi getur gert [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Apps.  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a>Til að bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnaveitu í Power Apps

1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/) í vafranum og skráið ykkur svo inn.
2. Á heimasíðunni, í hlutanum **Byrja frá gögnum** skal velja **Aðrir gagnagjafar**.  

    Þetta opnar Power Apps Studio. Í fyrstu innskráningu þarf að tilgreina land/svæði.  
3. Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.

    Power Apps mun tengjast [!INCLUDE[prod_short](includes/prod_short.md)] með því að nota skilríkin sem notandi er skráður inn í með. Ef þú ert ekki stjórnandi á [!INCLUDE[prod_short](includes/prod_short.md)] þínu þarftu hugsanlega að skrá þig inn með öðrum reikningi.  

4. Power Apps mun birta lista yfir *umhverfi og fyrirtæki* sem eru tiltæk í [!INCLUDE[prod_short](includes/prod_short.md)]. Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við, svo sem *FRAMLEIÐSLA - Fyrirtækið mitt*.  

5. Næst verður settur fram listi yfir töflur sem verða fyrir áhrifum sem hluti af API fyrir umhverfið þitt. Velja töfluna sem á að tengjast við og síðan **Tengjast**.

Þessar svokölluðu töflur verða skráðar sem endastöðvar með [!INCLUDE[prod_short](includes/prod_short.md)] tengli fyrir Power Apps.  

> [!NOTE]
> Ef þú vilt hafa með gögn úr öðrum töflum í [!INCLUDE[prod_short](includes/prod_short.md)] í forritinu þínu verður þú að vinna með þróunaraðila til að skilgreina sérsniðið API í [!INCLUDE[prod_short](includes/prod_short.md)] og síðan nota þetta sérsniðna API í gegnum sérsniðinn tengil í Power Apps. Nánari upplýsingar má finna í [Stofna sérsniðin tengi frá grunni](/connectors/custom-connectors/define-blank).  

Nú hefur þér tekist að tengjast gögnum þínum í [!INCLUDE[prod_short](includes/prod_short.md)] og getur byrjað að byggja upp PowerApp. Hægt er að bæta við fleiri skjáum og tengjast við fleiri gögn úr [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Ef þú vilt tengjast við [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.  

## <a name="see-also"></a>Sjá einnig

[Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]