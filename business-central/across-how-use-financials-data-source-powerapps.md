---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps

Notandi getur gert [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.  

> [!TIP]  
> Business Central býður nú upp á þróun og aðgerðastuðning fyrir Power Platform í AL-Go og sýnishornum til að byrja að búa til eigin forrit með Power Apps. Þessir eiginleikar eru í forskoðun eins og er. Til að læra [meira skaltu fara í Business Central og Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) í þróunaraðilanum og it pro hjálpinni.

## Frumskilyrði

Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Apps.  

## Bæta við [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa í Power Apps

Þessi skref bæta við Business Central-töflu, t.d. viðskiptamönnum eða vörum, sem gagnagjafa forrits Power Apps .

1. Farið er í [powerapps.microsoft.com](https://powerapps.microsoft.com/) í vafrann og síðan er skráð inn.
2. Á yfirlitssvæðinu vinstra megin skal velja **+ Stofna** og velja **síðan Fleiri gagnagjafa** á síðunni **Stofna smáforrit** .
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. Tengingarnar **á** listanum sýna þær gagnatengingar sem til eru.

   - Ef það er **Business Central** tenging þegar, veljið hana og veljið **Svo Stofna**.

   - Ef þú sérð ekki Business Central tengingu skaltu velja **+ Nýja tengingu**, leita að og velja **Business Central** og velja **svo Create**.

   > [!NOTE]
   > Ef þú vilt tengjast við [!INCLUDE[prod_short](includes/prod_short.md)] tengingu innanhúss verður þú að velja **Business Central (innanhúss)** tengið.  
  
4. Power Apps tengingar við notandann [!INCLUDE[prod_short](includes/prod_short.md)]. Skrá sig inn með því að nota Nafn og aðgangsorð Business Central. Ef þú ert ekki stjórnandi gætirðu [!INCLUDE[prod_short](includes/prod_short.md)] þurft að skrá þig inn með öðrum reikningi.  
5. Þegar notandi hefur skráð sig inn Power Apps  birtir lista yfir *umhverfi og fyrirtæki* sem tiltæk eru frá [!INCLUDE[prod_short](includes/prod_short.md)]. Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við, svo sem *FRAMLEIÐSLA - Fyrirtækið mitt*.  
6. Næst birtist listi yfir töflur sem eru útsettar sem hluti af API fyrir umhverfið. Velja töfluna sem á að tengjast við og síðan **Tengjast**.

Þessar svokölluðu töflur verða skráðar sem endastöðvar með [!INCLUDE[prod_short](includes/prod_short.md)] tengli fyrir Power Apps.  

> [!NOTE]
> Ef þú vilt hafa gögn úr öðrum töflum með í [!INCLUDE[prod_short](includes/prod_short.md)] forritinu þínu verður þú að vinna með forritara til að skilgreina sérsniðið API í [!INCLUDE[prod_short](includes/prod_short.md)].  

Nú hefur þú tengst gögnunum þínum [!INCLUDE[prod_short](includes/prod_short.md)] og ert tilbúinn til að byrja að byggja upp Power Appið þitt. Þú getur alltaf bætt við fleiri skjáum og tengst fleiri gögnum. Læra meira á [Búa til strigaforrit úr sýni í Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## Sjá einnig .

[Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
