---
title: Úrræðaleit vegna samstillingarvillna | Microsoft Docs
description: Veitir leiðbeiningar til að finna og leysa samstillingarvillur.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726791"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="6f41f-103">Úrræðaleit vegna samstillingarvillna</span><span class="sxs-lookup"><span data-stu-id="6f41f-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="6f41f-104">Margir hreyfanlegir hlutir taka þátt í samþættingu [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] og stundum fer eitthvað úrskeiðis.</span><span class="sxs-lookup"><span data-stu-id="6f41f-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="6f41f-105">Þetta efnisatriði bendir á nokkrar dæmigerðar villur sem koma upp og gefur ýmis ráð um hvernig á að laga þær.</span><span class="sxs-lookup"><span data-stu-id="6f41f-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="6f41f-106">Villur koma oft upp annaðhvort vegna þess að notandi hefur gert eitthvað við tengdar færslur eða eitthvað er að uppsetningu samþættingar.</span><span class="sxs-lookup"><span data-stu-id="6f41f-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="6f41f-107">Notendur geta leyst úr villum sem tengjast tengdum færslum.</span><span class="sxs-lookup"><span data-stu-id="6f41f-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="6f41f-108">Þessar villur stafa af aðgerðum eins og að eyðing á færslu í öðru, en ekki báðum, viðskiptaforritunum og síðan samstilla.</span><span class="sxs-lookup"><span data-stu-id="6f41f-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="6f41f-109">Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="6f41f-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="6f41f-110">Villur sem tengjast því hvernig samþættingin er sett upp þurfa venjulega á athygli stjórnanda að halda.</span><span class="sxs-lookup"><span data-stu-id="6f41f-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="6f41f-111">Hægt er að skoða þessar villur á síðunni **Villur í samstillingu samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="6f41f-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="6f41f-112">Dæmigerð vandamál eru til að mynda:</span><span class="sxs-lookup"><span data-stu-id="6f41f-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="6f41f-113">Heimildum og hlutverkum sem notanda er úthlutað eru ekki rétt.</span><span class="sxs-lookup"><span data-stu-id="6f41f-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="6f41f-114">Reikningur stjórnanda var tilgreindur sem samþættingarnotandinn.</span><span class="sxs-lookup"><span data-stu-id="6f41f-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="6f41f-115">Aðgangsorð samþættingarnotanda er stillt þannig að þurfi að breyta því þegar notandi skráir sig inn.</span><span class="sxs-lookup"><span data-stu-id="6f41f-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="6f41f-116">Gengi gjaldmiðla er ekki tilgreint í öðru hvoru forritinu.</span><span class="sxs-lookup"><span data-stu-id="6f41f-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="6f41f-117">Leysa þarf villurnar handvirkt, en til eru nokkrar leiðir sem síðan hjálpar þér með.</span><span class="sxs-lookup"><span data-stu-id="6f41f-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="6f41f-118">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="6f41f-118">For example:</span></span>  

* <span data-ttu-id="6f41f-119">Reitirnir **Uppruni** og **Endastaður** kunna að innihalda tengla á færsluna þar sem villan fannst.</span><span class="sxs-lookup"><span data-stu-id="6f41f-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="6f41f-120">Smelltu á tengilinn til að opna færsluna og skoða villuna.</span><span class="sxs-lookup"><span data-stu-id="6f41f-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="6f41f-121">Aðgerðirnar **Eyða færslum eldri en sjö daga** og **Eyða öllum færslum** hreinsa listana.</span><span class="sxs-lookup"><span data-stu-id="6f41f-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="6f41f-122">Venjulega eru þessar aðgerðir notaðar eftir að orsök villu sem hefur áhrif á margar færslur hefur verið löguð.</span><span class="sxs-lookup"><span data-stu-id="6f41f-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="6f41f-123">Sýndu samt aðgát.</span><span class="sxs-lookup"><span data-stu-id="6f41f-123">Use caution, however.</span></span> <span data-ttu-id="6f41f-124">Þessar aðgerðir gætu eytt villum sem skipta enn máli.</span><span class="sxs-lookup"><span data-stu-id="6f41f-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f41f-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6f41f-125">See Also</span></span>
<span data-ttu-id="6f41f-126">[Samþætting við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="6f41f-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="6f41f-127">[Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="6f41f-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="6f41f-128">[Uppsetning á tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="6f41f-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="6f41f-129">Tengja og samstilla færslur handvirkt</span><span class="sxs-lookup"><span data-stu-id="6f41f-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="6f41f-130">Skoða stöðu á samstillingu</span><span class="sxs-lookup"><span data-stu-id="6f41f-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  