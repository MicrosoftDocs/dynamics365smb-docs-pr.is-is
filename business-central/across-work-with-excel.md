---
title: Skoða og breyta í Excel From Business Central
description: Lærðu hvernig hægt er að opna síðurnar í Microsoft Excel frá Business Central til að fá betri gagnagreiningar.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/06/2020
ms.author: jswymer
ms.openlocfilehash: 5e585d4bc7d9f7ce159671c10298f734fd5a09d5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378824"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="099f9-103">Skoða og breyta í Excel From Business Central</span><span class="sxs-lookup"><span data-stu-id="099f9-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="099f9-104">Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu einnig skoðað færslur með Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="099f9-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="099f9-105">Til að gera þetta hefur þú tvo valkosti.</span><span class="sxs-lookup"><span data-stu-id="099f9-105">To do this, you have two options.</span></span> <span data-ttu-id="099f9-106">Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="099f9-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="099f9-107">Munurinn á aðgerðunum tveimur er sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="099f9-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="099f9-108">Opna í Excel</span><span class="sxs-lookup"><span data-stu-id="099f9-108">Open in Excel</span></span>

- <span data-ttu-id="099f9-109">Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="099f9-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="099f9-110">Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="099f9-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="099f9-111">Þú getur gert breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="099f9-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="099f9-112">Þú getur aðeins vistað breytingarnar í Excel-skrá í tölvunni þinni.</span><span class="sxs-lookup"><span data-stu-id="099f9-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="099f9-113">Þessi aðgerð virkar bæði í Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="099f9-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="099f9-114">**Open í Excel** aðgerðin er sjálfgefið tiltæk fyrir [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss.</span><span class="sxs-lookup"><span data-stu-id="099f9-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="099f9-115">Ef þú setur hins vegar upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss fyrir breytingar í Excel er **Opna í Excel** aðgerðinni skipt út fyrir aðgerðina **Breyta í Excel**.</span><span class="sxs-lookup"><span data-stu-id="099f9-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="099f9-116">Breyta í Excel</span><span class="sxs-lookup"><span data-stu-id="099f9-116">Edit in Excel</span></span>

- <span data-ttu-id="099f9-117">Með þessari aðgerð tekur Excel flestar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar, þannig að Excel-vinnubókin innihaldi nánast sömu færslur og dálka.</span><span class="sxs-lookup"><span data-stu-id="099f9-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="099f9-118">Kosturinn við aðgerðina **Breyta í Excel** er að þú getur gert breytingar á færslum í Excel og síðan birt breytingarnar aftur í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="099f9-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="099f9-119">Það virkar aðeins á Windows; ekki macOS.</span><span class="sxs-lookup"><span data-stu-id="099f9-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="099f9-120">Hægt er að skipta um fyrirtæki sem unnið er með.</span><span class="sxs-lookup"><span data-stu-id="099f9-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="099f9-121">Til að skipta um fyrirtæki skal velja **Valkostir** táknið, ![Valkostir Excel-innbótar](media/cogwheel.png "Valkostir Excel-innbótar") í svæði Excel-innbótar og síðan velja fyrirtækið í reitnum **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="099f9-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="099f9-122">Þegar skipt er um fyrirtæki skal ganga úr skugga um að reiturinn **Umhverfi** sé ekki auður.</span><span class="sxs-lookup"><span data-stu-id="099f9-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="099f9-123">Ef svo er skal stilla hann á einn af tiltækum valkostum, annars virkar innbótin ekki sem skyldi.</span><span class="sxs-lookup"><span data-stu-id="099f9-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="099f9-124">Ef verið er að gera breytingar á innbótinni verður að endurhlaða hana til að uppfæra tenginguna.</span><span class="sxs-lookup"><span data-stu-id="099f9-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="099f9-125">Til að endurhlaða skal nota valmyndina ![Excel-innbót](media/excel-addin-menu.png "Valkostir Excel-innbótar") efst í hægra horni innbótarinnar.</span><span class="sxs-lookup"><span data-stu-id="099f9-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="099f9-126">Ef ekki er hægt að hlaða innbótinni skal tala við kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="099f9-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="099f9-127">Ef notandi er kerfisstjóri skal skoða [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="099f9-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="099f9-128">Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur stillt Excel-innbótina og aðeins í boði fyrir vefbiðlara.</span><span class="sxs-lookup"><span data-stu-id="099f9-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="099f9-129">Ef stjórnendur langar að fræðast betur um hvernig eigi að setja upp Excel-innbótina má finna upplýsingar um það í [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="099f9-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="099f9-130">Sjá muninn á milli valkostanna</span><span class="sxs-lookup"><span data-stu-id="099f9-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="099f9-131">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="099f9-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="099f9-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="099f9-132">See Also</span></span>

[<span data-ttu-id="099f9-133">Greina fjárhagsskýrslur í Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="099f9-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="099f9-134">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="099f9-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="099f9-135">Endurbætur á Excel-samþættingu í 2019 útgáfu 2</span><span class="sxs-lookup"><span data-stu-id="099f9-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]