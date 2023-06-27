---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps" />Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps

Notandi getur gert [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.  

> [!TIP]  
> Viðskiptamiðl býður nú upp á þróun og rekstur stuðningur fyrir  Power Platform  í Al-Go og sýnishorn til að fá þú byrjaðir að búa til þitt eigið apps með Power Apps. Þessir eiginleikar eru nú í forskoðun. Til að fræðast meira er farið í  [miðborg og  Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview)  í Forritunarmálið og það Pro Help.

## <a name="prerequisites" />Frumskilyrði

Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Apps.  

## <a name="add--as-a-data-source-in-power-apps" />Bæta við  [!INCLUDE[prod_short](includes/prod_short.md)]  sem gagnagjafi í Power Apps

Þessi skref bæta við aðaltöflu viðskipta, eins og Viðskiptavinir eða vörur, sem gagnagjafi  Power Apps  forrits.

1. Í vafranum ferðu  [í powerapps.microsoft.com](https://powerapps.microsoft.com/) og skráir þig inn.
2. Í skoðunarrúðunni vinstra megin skal velja  **+ Create** og velja  **svo gagnagjöfum**  á  **síðunni Create App** .
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3.  **Tengingarnar**  Sýna hvaða gagnatengingar eru til staðar.

   -  **Ef Viðskiptatengmiðatengingar**  eru nú þegar til, veljið það og veljið  **Create**.

   - Ef þú sérð ekki Aðaltengingu viðskipta skaltu velja  **+ nýja tengingu**, leita að og velja  **Business Central**, og velja  **Create**.

   > [!NOTE]
   > Ef þú vilt tengjast  [!INCLUDE[prod_short](includes/prod_short.md)]  innanhúss þá þarf að velja  **Business Central (innanhúss)**  tengibúnað.  
  
4. Power Apps  [!INCLUDE[prod_short](includes/prod_short.md)] tengist. Skráðu þig inn með nafni og lykilorði Viðskiptaseðla. Ef þú ert ekki kerfisstjóri  [!INCLUDE[prod_short](includes/prod_short.md)] gætir þú þurft að skrá þig inn með öðrum lykli.  
5. Þegar þú hefur skráð þig inn  Power Apps  birtist listi  *yfir umhverfi og fyrirtæki*  sem eru tiltæk [!INCLUDE[prod_short](includes/prod_short.md)]. Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við, svo sem *FRAMLEIÐSLA - Fyrirtækið mitt*.  
6. Næst kemur þú fram með lista yfir töflur sem verða til sem hluti af API fyrir þitt umhverfi. Velja töfluna sem á að tengjast við og síðan **Tengjast**.

Þessar svokölluðu töflur verða skráðar sem endastöðvar með [!INCLUDE[prod_short](includes/prod_short.md)] tengli fyrir Power Apps.  

> [!NOTE]
> Ef þú vilt hafa gögn frá öðrum töflum í  [!INCLUDE[prod_short](includes/prod_short.md)]  í forritinu, þá verður þú að vinna með forritara til að skilgreina SÉRSNIÐIÐ API í [!INCLUDE[prod_short](includes/prod_short.md)].  

Á þessum tímapunkti hefur þú tekist á við gögnin þín  [!INCLUDE[prod_short](includes/prod_short.md)]  og ert tilbúin/NUM að byrja að byggja upp Power App. Alltaf er hægt að bæta við fleiri skjám og tengja við fleiri gögn. Læra meira at  [skapa strika App frá umskipan í Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum. Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## <a name="sample-apps-to-get-started" />Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## <a name="develop-and-maintain-apps-application-lifecycle-management" />Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/paths/power-apps-power-automate-business-central/)

## <a name="see-also" />Sjá einnig .

[Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
