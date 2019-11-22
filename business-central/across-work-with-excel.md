---
title: Skoða og breyta í Excel From Business Central | Microsoft Docs
description: Lærðu hvernig hægt er að opna síðurnar í Microsoft Excel frá Business Central til að fá betri gagnagreiningar.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 71b4e5b7124f929255f1374b38cfbe28c9f12d2b
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692801"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="c52f1-103">Skoða og breyta í Excel From Business Central</span><span class="sxs-lookup"><span data-stu-id="c52f1-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="c52f1-104">Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu einnig skoðað færslur með Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c52f1-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="c52f1-105">Til að gera þetta hefur þú tvo valkosti.</span><span class="sxs-lookup"><span data-stu-id="c52f1-105">To do this, you have two options.</span></span> <span data-ttu-id="c52f1-106">Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="c52f1-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="c52f1-107">Munurinn á aðgerðunum tveimur er sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="c52f1-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="c52f1-108">Opna í Excel</span><span class="sxs-lookup"><span data-stu-id="c52f1-108">Open in Excel</span></span>

- <span data-ttu-id="c52f1-109">Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="c52f1-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="c52f1-110">Þetta þýðir að Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="c52f1-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="c52f1-111">Þú getur gert breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="c52f1-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="c52f1-112">Þú getur aðeins vistað breytingarnar í Excel-skrá í tölvunni þinni.</span><span class="sxs-lookup"><span data-stu-id="c52f1-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="c52f1-113">Þessi aðgerð virkar bæði í Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="c52f1-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="c52f1-114">**Open í Excel** aðgerðin er sjálfgefið tiltæk fyrir [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss.</span><span class="sxs-lookup"><span data-stu-id="c52f1-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="c52f1-115">Ef þú setur hins vegar upp [!INCLUDE [prodshort](includes/prodshort.md)] innanhúss fyrir breytingar í Excel er **Opna í Excel** aðgerðinni skipt út fyrir aðgerðina **Breyta í Excel**.</span><span class="sxs-lookup"><span data-stu-id="c52f1-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="c52f1-116">Breyta í Excel</span><span class="sxs-lookup"><span data-stu-id="c52f1-116">Edit in Excel</span></span>

- <span data-ttu-id="c52f1-117">Með þessari aðgerð tekur Excel flestar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="c52f1-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="c52f1-118">Þetta þýðir að Excel-vinnubókin mun innihalda næstum því sömu færslur og dálka.</span><span class="sxs-lookup"><span data-stu-id="c52f1-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="c52f1-119">Kosturinn við aðgerðina **Breyta í Excel** er að þú getur gert breytingar á færslum í Excel og síðan birt breytingarnar aftur í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="c52f1-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="c52f1-120">Það virkar aðeins á Windows; ekki macOS.</span><span class="sxs-lookup"><span data-stu-id="c52f1-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="c52f1-121">Þetta var endurbætt í 2019 útgáfutímabili 2.</span><span class="sxs-lookup"><span data-stu-id="c52f1-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="c52f1-122">Frekari upplýsingar er að finna í [Endurbætur á Excel samþættingu](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="c52f1-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="c52f1-123">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur stillt Excel-innbótina.</span><span class="sxs-lookup"><span data-stu-id="c52f1-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="c52f1-124">Ef stjórnendur langar að fræðast betur um hvernig eigi að setja upp Excel-innbótina má finna upplýsingar um það í [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="c52f1-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="c52f1-125">Þessi eiginleiki er aðeins í boði fyrir vefbiðlarann fyrir [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss.</span><span class="sxs-lookup"><span data-stu-id="c52f1-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="c52f1-126">Sjá muninn á milli valkostanna</span><span class="sxs-lookup"><span data-stu-id="c52f1-126">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="c52f1-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c52f1-127">See Also</span></span>
[<span data-ttu-id="c52f1-128">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="c52f1-128">Working with Business Central</span></span>](ui-work-product.md)  
