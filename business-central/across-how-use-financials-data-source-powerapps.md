---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2023
ms.author: jswymer
---
# Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps

Notandi getur gert [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.  

> [!TIP]  
> Frekari  Power Apps  heimildaöflun og Power App sýnis okkar sem  [!INCLUDE[prod_short](includes/prod_short.md)]  fram fer á ræsiviðburði verður birt hér síðar í 2023 bylgju 1. Lesið meira at  [byrja við fleiri umskapanarsniðmátum  Power Automate  og Power Apps](/dynamics365/release-plan/2023wave1/smb/dynamics365-business-central/get-started-more-sample-power-automate-templates-power-apps).

## Frumskilyrði

Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Apps.  

## Bæta við  [!INCLUDE[prod_short](includes/prod_short.md)]  sem gagnagjafi í Power Apps

1. Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/) í vafranum og skráið ykkur svo inn.
2. Á heimasíðunni, í hlutanum **Byrja frá gögnum** skal velja **Aðrir gagnagjafar**.  

    Þetta skref opnast Power Apps Studio. Í fyrsta formerki þarf að tilgreina land/svæði.  
3. Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.

    Power Apps mun tengjast með notkun skilríkja sem þú ert skráð/ur í samband  [!INCLUDE[prod_short](includes/prod_short.md)]  við. Ef þú ert ekki kerfisstjóri  [!INCLUDE[prod_short](includes/prod_short.md)] gætir þú þurft að skrá þig inn með öðrum lykli.  

4. Power Apps mun birta lista yfir *umhverfi og fyrirtæki* sem eru tiltæk í [!INCLUDE[prod_short](includes/prod_short.md)]. Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við, svo sem *FRAMLEIÐSLA - Fyrirtækið mitt*.  

5. Næst kemur þú fram með lista yfir töflur sem verða til sem hluti af API fyrir þitt umhverfi. Velja töfluna sem á að tengjast við og síðan **Tengjast**.

Þessar svokölluðu töflur verða skráðar sem endastöðvar með [!INCLUDE[prod_short](includes/prod_short.md)] tengli fyrir Power Apps.  

> [!NOTE]
> Ef þú vilt hafa gögn frá öðrum töflum í  [!INCLUDE[prod_short](includes/prod_short.md)]  í forritinu, þá verður þú að vinna með forritara til að skilgreina SÉRSNIÐIÐ API í [!INCLUDE[prod_short](includes/prod_short.md)].  

Á þessum tímapunkti hefur þú tekist á við gögnin þín  [!INCLUDE[prod_short](includes/prod_short.md)]  og ert tilbúin/NUM að byrja að byggja upp Power App. Hægt er að bæta við fleiri skjám og tengja við fleiri gögn [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Ef þú vilt tengjast við [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.  

## Sjá tengda [Microsoft þjálfun](/training/paths/power-apps-power-automate-business-central/)

## Sjá einnig .

[Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
