---
title: Stjórnunarverk í Business Central
description: Sumir verkhlutar í Business Central krefjast miðlægrar stjórnunar og uppsetningar. Sjáðu hverjir þeir eru og lærðu hvað skal gera.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: b7a20d6f116a383332b5daab6aa059839f608276
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521177"
---
# <a name="administration"></a>Stjórnun

Almenn stjórnunarverk eru yfirleitt framkvæmd af einu hlutverki innan fyrirtækisins. Umfang þessara verka getur byggst á stærð fyrirtækisins og starfsábyrgð stjórnandans. Þessi verk geta falið í sér umsjón með gagnagrunnssamstillingu verkraða og póstraða, uppsetningu notenda og sérstillingu viðmóts.  

Mikilvægt er að færa inn rétt uppsetningargildi frá upphafi til að ný viðskiptaforrit nái árangri. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur nokkrar uppsetningarleiðbeiningar sem aðstoða þig við að setja upp grunngögn. Nánari upplýsingar er að finna í [Uppsetning Business Central](setup.md).

> [!NOTE]
> Hægt er að setja upp nýja fyrir tækið í [!INCLUDE[prod_short](includes/prod_short.md)] með RapidStart Services, sem er tæki sem hannað er til að flýta fyrir virkjunartíma, bæta gæði innleiðingar, koma á innleiðingaraðferð sem hægt er að endurtaka, og gera bæta framleiðni með því að gera síendurtekin verk sjálfvirk og einföld. Nánari upplýsingar er að finna í [Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Hvort sem RapidStart Services er notað til að innleiða uppsetningargildi eða þau eru handfærð inn í nýja fyrirtækið má notast við almennar leiðbeiningar til að auðvelda uppsetningu fyrir tiltekna reiti sem þekktir eru fyrir að valda vandræðum ef þeir eru rangt skilgreindir.  

Yfirnotandi eða stjórnandi getur sett upp Data Exchange Framework til að gera notendum kleift að flytja út og flytja inn gögn í banka og launaskrár, t.d. fyrir ýmsa stjórnun reiðufés. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|
|Skilgreinið hver getur skráð sig inn [!INCLUDE[prod_short](includes/prod_short.md)] með því að stofna notendur á Microsoft 365 admin Center samkvæmt vöruleyfum.|[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)|
|Úthluta heimildum til notendur, breyta heimildasöfnum og hópa notendur saman til að auðvelda heimildastjórnun.|[Úthluta leyfi til notenda og hópa](ui-how-users-permissions.md)|
|Bæta við notendum, meðhöndla heimildir og aðgang að gögnum, úthluta hlutverkum.|[Vinna með forstillingar](admin-users-profiles-roles.md)|
|Stjórna notandastillingum, t.d. fyrirtæki, hlutverk, tungumál, svæði og tímabelti.|[Notandastillingar](admin-manage-user-settings-preferences.md)|
|Setja upp prentara og tilgreina hvaða skýrslur á að prenta á hvaða prentara.|[Setja upp prentara](ui-specify-printer-selection-reports.md)|
|Flokka gagnatrúnað fyrir reiti þannig að þú getir svarað beiðnum frá skráðum aðilum sem tengjast persónuupplýsingum þeirra.|[Flokkun gagnatrúnaðar](admin-classifying-data-sensitivity.md)|
|Svara beiðnum frá skráðum aðilum sem tengjast persónuupplýsingum þeirra.|[Svara beiðnum um persónuleg gögn](admin-responding-to-requests-about-personal-data.md)|
|Nýtt fyrirtækiseining sem notar sniðmát er sett upp.|[Stofna ný fyrirtæki](about-new-company.md)|
|Rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum til að finna uppruna villna og gagnabreytinga.|[Skráning breytinga](across-log-changes.md)|  
|Færa inn stakar eða endurteknar beiðnir um keyrslu skýrslna eða kótaeininga.|[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)|  
|Meðhöndla, eyða eða þjappa skjöl|[Eyðing skjala](admin-manage-documents.md)|  
|Birta síður, kóðaeiningar og beiðnir sem vefþjónustu.|[Birta vefþjónustu](across-how-publish-web-service.md)|
|Sem hluti af því að búa til Connect Apps milli [!INCLUDE[prod_short](includes/prod_short.md)] og lausna þriðja aðila í gegnum REST API skal skilgreina sniðmát sem eru notuð til að fylla í tóma eiginleika í einingu þegar þú býrð til POST-aðgerð í gegnum API.|[Grunnstilling API-sniðmáta](admin-configuring-api-template.md)|
|Hægt er að dulrita gögn á [!INCLUDE[prod_short](includes/prod_short.md)] netþjóninum með því að stofna nýjan dulritunarlykil eða flytja inn fyrirliggjandi lykil sem virkjaður er á netþjóni.|[Stjórnun gagnadulritunar](admin-manage-data-encryption.md)|
|Tengdu Dynamics 365 Sales við [!INCLUDE[prod_short](includes/prod_short.md)] til að fá hnökralausa samþættingu milli viðskiptavinatengsla og úrvinnslu pantana í heildarferlinu.|[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Breyta hvaða reiti og aðgerðir eru sýndar í notandaviðmótinu til að passa viðskiptaferlum fyrirtækisins og víkka út lausnina með forritum.|[Sérstillir [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Stjórnun í stjórnendamiðstöðinni

Innri og úthlutaðir stjórnendur hafa aðgang að stjórnendamiðstöðinni [!INCLUDE [prod_short](includes/prod_short.md)] þar sem þeir geta stillt, fylgst með og úrræðaleitað [!INCLUDE [prod_short](includes/prod_short.md)] umhverfi. Eftirfarandi tafla lýsir nokkrum lykilverkum með tenglum í greinar þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|
|Kynntu þér verkfærin sem eru tiltæk til að aðstoða þig við að leysa úr vandamálum.|[Tæknilegur stuðningur](/dynamics365/business-central/dev-itpro/technical-support)|
|Fylgjast með notkun og úrræðaleita lotur|[Umhverfismælingar í stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Stjórna notandalotum, þar á meðal að hætta við lotu ef lokað er á notandann.|[Stjórnun lota](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|
|Skilgreina leigjanda til að senda fjarmælingargögn til Azure Application Insights til að fá betri greiningu og úrræðaleit.|[Virkja sendingu fjarmælingar til Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Viðskiptavirkni](across-business-functionality.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]