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
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 2474f83fd9fa137b40756a3d07ac025208f3ac6c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308261"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="1a7dd-103">Skoða og breyta í Excel From Business Central</span><span class="sxs-lookup"><span data-stu-id="1a7dd-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="1a7dd-104">Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu einnig skoðað færslur með Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="1a7dd-105">Til að gera þetta hefur þú tvo valkosti.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-105">To do this, you have two options.</span></span> <span data-ttu-id="1a7dd-106">Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="1a7dd-107">Munurinn á aðgerðunum tveimur er sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="1a7dd-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="1a7dd-108">Opna í Excel</span><span class="sxs-lookup"><span data-stu-id="1a7dd-108">Open in Excel</span></span>

-    <span data-ttu-id="1a7dd-109">Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="1a7dd-110">Þetta þýðir að Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1a7dd-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="1a7dd-111">Þú getur gert breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1a7dd-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="1a7dd-112">Þú getur aðeins vistað breytingarnar í Excel-skrá í tölvunni þinni.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="1a7dd-113">Þessi aðgerð virkar bæði í Windows og macOS.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="1a7dd-114">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum er aðgerðin **Opna í Excel** ekki í boði ef aðgerðin **Breyta í Excel** er í boði.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="1a7dd-115">Breyta í Excel</span><span class="sxs-lookup"><span data-stu-id="1a7dd-115">Edit in Excel</span></span>

-    <span data-ttu-id="1a7dd-116">Með þessari aðgerð tekur Excel-vinnubókin síur á síðunni ekki til greina sem takmarka færslurnar sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="1a7dd-117">Þetta þýðir að Excel-vinnubókin mun innihalda allar tiltækar færslur og dálka, óháð því sem sýnt er á síðunni.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="1a7dd-118">Kosturinn við aðgerðina **Breyta í Excel** er að þú getur gert breytingar á færslum í Excel og síðan birt breytingarnar aftur í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1a7dd-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="1a7dd-119">Það virkar aðeins á Windows; ekki macOS.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="1a7dd-120">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur sett upp Excel-innbótina.</span><span class="sxs-lookup"><span data-stu-id="1a7dd-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="1a7dd-121">Fyrir stjórnendur, ef þig langar að fræðast betur um hvernig eigi að setja upp Excel-innbót skal sjá [Setja upp Excel-innbótina](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="1a7dd-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="1a7dd-122">Sjá muninn á milli valkostanna</span><span class="sxs-lookup"><span data-stu-id="1a7dd-122">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="1a7dd-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1a7dd-123">See Also</span></span>
[<span data-ttu-id="1a7dd-124">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="1a7dd-124">Working with Business Central</span></span>](ui-work-product.md)  
