---
title: Uppsetning eigna| Microsoft Docs
description: "Kynntu þér röð verkhluta sem þú þarft að framkvæma til að setja upp eignir, eins og t.d. þá sem tengjast vélum eða byggingum."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="4a720-103">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="4a720-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="4a720-104">Áður en þú getur unnið með eignir þarftu að skilgreina nokkur atriði:</span><span class="sxs-lookup"><span data-stu-id="4a720-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="4a720-105">Hvernig þú tryggir, viðheldur og afskrifar.</span><span class="sxs-lookup"><span data-stu-id="4a720-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="4a720-106">Hvernig skráir þú kostnað og önnur gildi í aðalbókinni.</span><span class="sxs-lookup"><span data-stu-id="4a720-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="4a720-107">Taflan hér að neðan inniheldur tengla í frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="4a720-107">The table below has links to more information.</span></span> <span data-ttu-id="4a720-108">Eftir að þú hefur sett þessi atriði upp geturðu byrjað á ýmsum verkefnum.</span><span class="sxs-lookup"><span data-stu-id="4a720-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="4a720-109">Frekari upplýsingar eru í [Eignir](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="4a720-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="4a720-110">Hægt er að skrá eignafærslur í **Fjárhagsbók eigna** eða í **Færslubók eigna**, allt eftir því hvort færslurnar eru fyrir fjárhagsskýrslugerð eða fyrir innri stjórnun.</span><span class="sxs-lookup"><span data-stu-id="4a720-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="4a720-111">Hjálp fyrir Eignir lýsir einungis hvernig nota á **fjárhagsbók eigna** glugginn.</span><span class="sxs-lookup"><span data-stu-id="4a720-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="4a720-112">Þegar þú virkjar aðgerð eignar í **Fjárhagsheildun** hlutanum í á **Afskriftabókarspjald** glugganum verður glugginn **Fjárhagsbók eigna** notaður til að bóka færslur á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="4a720-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="4a720-113">Þessi virkni krefst þess að upplifunin sé stillt á **Suite**.</span><span class="sxs-lookup"><span data-stu-id="4a720-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="4a720-114">Nánari upplýsingar er að finna í [Aðlaga Financials upplifun þína](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="4a720-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="4a720-115">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="4a720-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="4a720-116">Til</span><span class="sxs-lookup"><span data-stu-id="4a720-116">To</span></span> | <span data-ttu-id="4a720-117">Sjá</span><span class="sxs-lookup"><span data-stu-id="4a720-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="4a720-118">Setja upp sjálfgefna fjárhagsreikninga, úthlutunarlykla, færslubókarsniðmát og keyrslur fyrir bókun á eign og setja upp eignaflokka og undirflokka, til dæmis Áþreifanlegar og Óáþreifanlegar.</span><span class="sxs-lookup"><span data-stu-id="4a720-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="4a720-119">Hvernig á að: Uppsetning almennra eignaupplýsinga</span><span class="sxs-lookup"><span data-stu-id="4a720-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="4a720-120">Stofnun afskriftabóka og skilgreining ýmissa afskriftaraðferðir, samþætta við fjárhag og sem gera kleift að afrita færslur í margar afskriftabækur.</span><span class="sxs-lookup"><span data-stu-id="4a720-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="4a720-121">Hvernig á að: setja upp eignir</span><span class="sxs-lookup"><span data-stu-id="4a720-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="4a720-122">Virkja vátryggingu eigna, setja upp almennar upplýsingar um vátryggingar, vátryggingarspjaldinu á hvert tryggingaskírteini, og undirbúa færslubækur til að bóka vátryggingakostnað.</span><span class="sxs-lookup"><span data-stu-id="4a720-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="4a720-123">Hvernig á að setja upp vátryggingar eigna</span><span class="sxs-lookup"><span data-stu-id="4a720-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="4a720-124">Virkja viðhald eigna, setja upp almenna viðhaldsupplýsinga, setja upp bókunarlykla viðhalds og skilgreina tegundir viðhaldsvinna.</span><span class="sxs-lookup"><span data-stu-id="4a720-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="4a720-125">Hvernig á að: Uppsetning eignarviðhalds</span><span class="sxs-lookup"><span data-stu-id="4a720-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="4a720-126">Læra um mismunandi Aðferðir við afskriftir eigna</span><span class="sxs-lookup"><span data-stu-id="4a720-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="4a720-127">Afskriftaaðferðir</span><span class="sxs-lookup"><span data-stu-id="4a720-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="4a720-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4a720-128">See Also</span></span>
[<span data-ttu-id="4a720-129">Eignir</span><span class="sxs-lookup"><span data-stu-id="4a720-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="4a720-130">Fjármál</span><span class="sxs-lookup"><span data-stu-id="4a720-130">Finance</span></span>](finance.md)  
<span data-ttu-id="4a720-131">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="4a720-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="4a720-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a720-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

