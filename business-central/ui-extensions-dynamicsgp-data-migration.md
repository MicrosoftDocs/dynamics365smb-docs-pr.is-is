---
title: Flytja gögn úr Dynamics GP fyrir 15.3 | Microsoft Docs
description: Fyrir 15.3 uppfærslu geturðu notað Dynamics GP-Gagnaflutningaviðbótina til að flytja viðskiptamenn, lánardrottna, birgðavörur, fjárhagsreikninga, opnar viðskiptaskuldir og opnar viðskiptakröfur færslur frá Dynamics GP til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 06/22/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: c42f16f588b360b0e382ab2a3a91bd6974cc8a7e
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529189"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="43fbe-103">Dynamics GP-Gagnaflutningaviðbótin</span><span class="sxs-lookup"><span data-stu-id="43fbe-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="43fbe-104">Viðbótin er úrelt í uppfærslu 15.3.</span><span class="sxs-lookup"><span data-stu-id="43fbe-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="43fbe-105">Mælt er með því að notendur sem vilja flytja úr Dynamics GP byrji að nota leiðsagnarforritið **Flutningur í ský** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="43fbe-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="43fbe-106">Viðbótin **Flutningur í ský** er með öflugri virkni og færir meiri gögn í Business Central úr Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="43fbe-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="43fbe-107">Frekari upplýsingar er að finna á [Yfirfæra í Business Central Online úr Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) í stjórnunarefninu fyrir [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="43fbe-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="43fbe-108">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="43fbe-108">See Also</span></span>

[<span data-ttu-id="43fbe-109">Snjallskýsviðbætur fyrir flutningi í skýi</span><span class="sxs-lookup"><span data-stu-id="43fbe-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="43fbe-110">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="43fbe-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="43fbe-111">[Sérstilling [!INCLUDE[prodshort](includes/prodshort.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="43fbe-111">[Customizing [!INCLUDE[prodshort](includes/prodshort.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="43fbe-112">Yfirfæra í Business Central Online úr Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="43fbe-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
