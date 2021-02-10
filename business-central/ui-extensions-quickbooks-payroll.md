---
title: Notkun á QuickBooks innflutningsviðbót fyrir launaskrár | Microsoft Docs
description: Þetta efnisatriði lýsir því hvernig skal nota viðbótina til að flytja inn launafærslur úr QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757093"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="94cbf-103">QuickBooks-viðbótin fyrir innflutning á launaskrá</span><span class="sxs-lookup"><span data-stu-id="94cbf-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="94cbf-104">Notaðu QuickBooks-viðbótin fyrir innflutning á launaskrá til að flytja inn launafærslur úr QuickBooks til fjárhagslykla í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="94cbf-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="94cbf-105">Til dæmis er þetta gagnlegt þegar þú ert að skipta frá QuickBooks í [!INCLUDE[prod_short](includes/prod_short.md)] eða ef þú útvistar launaskrána þína en vilt líka halda utan um það í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="94cbf-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="94cbf-106">Skref til að flytja inn launagögn</span><span class="sxs-lookup"><span data-stu-id="94cbf-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="94cbf-107">Fyrsta skrefið er fyrir þig, eða kannski endurskoðandann þinn, til að nota útflutningseiginleikana í QuickBooks til að flytja út launagögnin í .IIF-skrá.</span><span class="sxs-lookup"><span data-stu-id="94cbf-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="94cbf-108">Annað skrefið er að opna síðuna **Færslubækur** í [!INCLUDE[prod_short](includes/prod_short.md)] og nota aðgerðina **Flytja inn launafærslur** til að flytja inn skrána.</span><span class="sxs-lookup"><span data-stu-id="94cbf-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="94cbf-109">Á meðan á innflutningsferlinu stendur varpar þú fjárhagslyklunum úr QuickBooks í samsvarandi reikninga í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="94cbf-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="94cbf-110">Lokaskrefið er að senda inn launafærslurnar í [!INCLUDE[prod_short](includes/prod_short.md)] í samræmi við reikningsvörpunina.</span><span class="sxs-lookup"><span data-stu-id="94cbf-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="94cbf-111">Frekari upplýsingar er að finna í [innflutningur launafærsla](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="94cbf-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="94cbf-112">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="94cbf-112">See Also</span></span>
<span data-ttu-id="94cbf-113">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="94cbf-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="94cbf-114">[Fjármál](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="94cbf-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="94cbf-115">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94cbf-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
