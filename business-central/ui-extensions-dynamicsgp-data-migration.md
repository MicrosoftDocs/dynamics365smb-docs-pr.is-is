---
title: Flytja gögn úr Dynamics GP fyrir 15.3 | Microsoft Docs
description: Fyrir 15.3 uppfærslu geturðu notað Dynamics GP-Gagnaflutningaviðbótina til að flytja viðskiptamenn, lánardrottna, birgðavörur, fjárhagsreikninga, opnar viðskiptaskuldir og opnar viðskiptakröfur færslur frá Dynamics GP til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: 986612a04ea75e89c2ef7cc983af4ae507738871
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377299"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="9f824-103">Dynamics GP-Gagnaflutningaviðbótin</span><span class="sxs-lookup"><span data-stu-id="9f824-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="9f824-104">Viðbótin er úrelt í uppfærslu 15.3.</span><span class="sxs-lookup"><span data-stu-id="9f824-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="9f824-105">Mælt er með því að notendur sem vilja flytja úr Dynamics GP byrji að nota leiðsagnarforritið **Flutningur í ský** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="9f824-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="9f824-106">Viðbótin **Flutningur í ský** er með öflugri virkni og færir meiri gögn í Business Central úr Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="9f824-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="9f824-107">Frekari upplýsingar er að finna á [Yfirfæra í Business Central Online úr Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) í stjórnunarefninu fyrir [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9f824-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="9f824-108">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9f824-108">See Also</span></span>

[<span data-ttu-id="9f824-109">Snjallskýsviðbætur fyrir flutningi í skýi</span><span class="sxs-lookup"><span data-stu-id="9f824-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="9f824-110">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="9f824-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="9f824-111">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="9f824-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="9f824-112">Yfirfæra í Business Central Online úr Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="9f824-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  


[!INCLUDE[footer-include](includes/footer-banner.md)]