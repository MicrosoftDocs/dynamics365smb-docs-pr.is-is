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
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187509"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="2566d-103">Skoða og breyta í Excel From Business Central</span><span class="sxs-lookup"><span data-stu-id="2566d-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="2566d-104">Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu einnig skoðað færslur með Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2566d-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="2566d-105">Til að gera þetta hefur þú tvo valkosti.</span><span class="sxs-lookup"><span data-stu-id="2566d-105">To do this, you have two options.</span></span> <span data-ttu-id="2566d-106">Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="2566d-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="2566d-107">Munurinn á aðgerðunum tveimur er sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="2566d-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="2566d-108">Opna í Excel</span><span class="sxs-lookup"><span data-stu-id="2566d-108">Open in Excel</span></span>

- <span data-ttu-id="2566d-109">Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="2566d-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="2566d-110">Þetta þýðir að Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2566d-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="2566d-111">Þú getur gert breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2566d-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2566d-112">Þú getur aðeins vistað breytingarnar í Excel-skrá í tölvunni þinni.</span><span class="sxs-lookup"><span data-stu-id="2566d-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="2566d-113">Þessi aðgerð virkar bæði í Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="2566d-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="2566d-114">**Open í Excel** aðgerðin er sjálfgefið tiltæk fyrir [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss.</span><span class="sxs-lookup"><span data-stu-id="2566d-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="2566d-115">Ef þú setur hins vegar upp [!INCLUDE [prodshort](includes/prodshort.md)] innanhúss fyrir breytingar í Excel er **Opna í Excel** aðgerðinni skipt út fyrir aðgerðina **Breyta í Excel**.</span><span class="sxs-lookup"><span data-stu-id="2566d-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="2566d-116">Breyta í Excel</span><span class="sxs-lookup"><span data-stu-id="2566d-116">Edit in Excel</span></span>

- <span data-ttu-id="2566d-117">Með þessari aðgerð tekur Excel flestar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="2566d-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="2566d-118">Þetta þýðir að Excel-vinnubókin mun innihalda næstum því sömu færslur og dálka.</span><span class="sxs-lookup"><span data-stu-id="2566d-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="2566d-119">Kosturinn við aðgerðina **Breyta í Excel** er að þú getur gert breytingar á færslum í Excel og síðan birt breytingarnar aftur í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2566d-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="2566d-120">Það virkar aðeins á Windows; ekki macOS.</span><span class="sxs-lookup"><span data-stu-id="2566d-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="2566d-121">Hægt er að skipta um fyrirtæki sem unnið er með.</span><span class="sxs-lookup"><span data-stu-id="2566d-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="2566d-122">Til að gera þetta skal velja **Valkostir** táknið, ![Valkostir Excel-innbótar](media/cogwheel.png "Valkostir Excel-innbótar") í svæði Excel-innbótar og síðan velja fyrirtækið í reitnum **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="2566d-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="2566d-123">Þegar skipt er um fyrirtæki skal ganga úr skugga um að reiturinn **Umhverfi** sé ekki auður.</span><span class="sxs-lookup"><span data-stu-id="2566d-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="2566d-124">Ef svo er skal stilla hann á einn af tiltækum valkostum, annars virkar innbótin ekki sem skyldi.</span><span class="sxs-lookup"><span data-stu-id="2566d-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="2566d-125">Excel-innbótin var endurbætt árið 2019 á útgáfutímabili 2.</span><span class="sxs-lookup"><span data-stu-id="2566d-125">The Excel Add-in was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="2566d-126">Frekari upplýsingar er að finna í [Endurbætur á Excel samþættingu](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="2566d-126">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="2566d-127">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur stillt Excel-innbótina og aðeins í boði fyrir vefbiðlara.</span><span class="sxs-lookup"><span data-stu-id="2566d-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="2566d-128">Ef stjórnendur langar að fræðast betur um hvernig eigi að setja upp Excel-innbótina má finna upplýsingar um það í [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="2566d-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span> <span data-ttu-id="2566d-129">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum.</span><span class="sxs-lookup"><span data-stu-id="2566d-129">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="2566d-130">Sjá muninn á milli valkostanna</span><span class="sxs-lookup"><span data-stu-id="2566d-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="2566d-131">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="2566d-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="2566d-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2566d-132">See Also</span></span>
[<span data-ttu-id="2566d-133">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="2566d-133">Working with Business Central</span></span>](ui-work-product.md)  
