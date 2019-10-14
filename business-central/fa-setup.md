---
title: Uppsetning eigna| Microsoft Docs
description: Kynntu þér röð verkhluta sem þú þarft að framkvæma til að setja upp eignir, eins og t.d. þá sem tengjast vélum eða byggingum.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9bc15c216edf295ecf6c04da2f30db8097ddfe31
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306509"
---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="9e47a-103">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="9e47a-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="9e47a-104">Áður en þú getur unnið með eignir þarftu að skilgreina nokkur atriði:</span><span class="sxs-lookup"><span data-stu-id="9e47a-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="9e47a-105">Hvernig þú tryggir, viðheldur og afskrifar.</span><span class="sxs-lookup"><span data-stu-id="9e47a-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="9e47a-106">Hvernig skráir þú kostnað og önnur gildi í aðalbókinni.</span><span class="sxs-lookup"><span data-stu-id="9e47a-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="9e47a-107">Taflan hér að neðan inniheldur tengla í frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9e47a-107">The table below has links to more information.</span></span> <span data-ttu-id="9e47a-108">Eftir að þú hefur sett þessi atriði upp geturðu byrjað á ýmsum verkefnum.</span><span class="sxs-lookup"><span data-stu-id="9e47a-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="9e47a-109">Frekari upplýsingar eru í [Eignir](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="9e47a-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9e47a-110">Hægt er að skrá eignafærslur á síðunum **Fjárhagsbók eigna** eða í **Færslubók eigna**, allt eftir því hvort færslurnar eru fyrir fjárhagsskýrslugerð eða fyrir innri stjórnun.</span><span class="sxs-lookup"><span data-stu-id="9e47a-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** pages, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="9e47a-111">Hjálp fyrir Eignir lýsir einungis hvernig nota á síðuna **Fjárhagsbók eigna**.</span><span class="sxs-lookup"><span data-stu-id="9e47a-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** page.</span></span>  

<span data-ttu-id="9e47a-112">Þegar þú virkjar aðgerð eignar í **Fjárhagsheildun** hlutanum á síðunni **Afskriftabókarspjald** verður síðan **Fjárhagsbók eigna** notuð til að bóka færslur á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="9e47a-112">When you enable a fixed asset activity in the **G/L Integration** section on the **Depreciation Book Card** page, the **Fixed Asset G/L Journal** page is used to post transactions for the activity.</span></span>

<span data-ttu-id="9e47a-113">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="9e47a-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="9e47a-114">Til</span><span class="sxs-lookup"><span data-stu-id="9e47a-114">To</span></span> | <span data-ttu-id="9e47a-115">Sjá</span><span class="sxs-lookup"><span data-stu-id="9e47a-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="9e47a-116">Setja upp sjálfgefna fjárhagsreikninga, úthlutunarlykla, færslubókarsniðmát og keyrslur fyrir bókun á eign og setja upp eignaflokka og undirflokka, til dæmis Áþreifanlegar og Óáþreifanlegar.</span><span class="sxs-lookup"><span data-stu-id="9e47a-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="9e47a-117">Uppsetning almennra eignaupplýsinga</span><span class="sxs-lookup"><span data-stu-id="9e47a-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="9e47a-118">Stofnun afskriftabóka og skilgreining ýmissa afskriftaraðferðir, samþætta við fjárhag og sem gera kleift að afrita færslur í margar afskriftabækur.</span><span class="sxs-lookup"><span data-stu-id="9e47a-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="9e47a-119">Setja upp eignaafskriftir</span><span class="sxs-lookup"><span data-stu-id="9e47a-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="9e47a-120">Virkja vátryggingu eigna, setja upp almennar upplýsingar um vátryggingar, vátryggingarspjaldinu á hvert tryggingaskírteini, og undirbúa færslubækur til að bóka vátryggingakostnað.</span><span class="sxs-lookup"><span data-stu-id="9e47a-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="9e47a-121">Uppsetning vátryggingar eignar.</span><span class="sxs-lookup"><span data-stu-id="9e47a-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="9e47a-122">Virkja viðhald eigna, setja upp almenna viðhaldsupplýsinga, setja upp bókunarlykla viðhalds og skilgreina tegundir viðhaldsvinna.</span><span class="sxs-lookup"><span data-stu-id="9e47a-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="9e47a-123">Uppsetning eignarviðhalds</span><span class="sxs-lookup"><span data-stu-id="9e47a-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="9e47a-124">Læra um mismunandi Aðferðir við afskriftir eigna</span><span class="sxs-lookup"><span data-stu-id="9e47a-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="9e47a-125">Afskriftaaðferðir</span><span class="sxs-lookup"><span data-stu-id="9e47a-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="9e47a-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9e47a-126">See Also</span></span>
[<span data-ttu-id="9e47a-127">Eignir</span><span class="sxs-lookup"><span data-stu-id="9e47a-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="9e47a-128">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9e47a-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="9e47a-129">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="9e47a-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="9e47a-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e47a-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
