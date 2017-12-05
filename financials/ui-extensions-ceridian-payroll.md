---
title: "Flytja inn launagögn með Ceridian Payroll-viðbótinni | Microsoft Docs"
description: "Nota skal þessa viðbót til að flytja inn launafærslur frá Ceridian HR/Payroll (BNA) og Ceridian PowerPay (Kanada) þjónustunum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 3c67d6bd4d24d5b58462fa05168f2ac764b2c695
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="the-ceridian-payroll-extension-to-dynamics-365-business-edition"></a><span data-ttu-id="bf9ae-103">Ceridian Payroll-viðbótin fyrir Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="bf9ae-103">The Ceridian Payroll Extension to Dynamics 365 Business edition</span></span> 
<span data-ttu-id="bf9ae-104">Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="bf9ae-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="bf9ae-105">Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir í gluggann **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="bf9ae-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="bf9ae-106">Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="bf9ae-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="bf9ae-107">Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.</span><span class="sxs-lookup"><span data-stu-id="bf9ae-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="bf9ae-108">Nánari upplýsingar eru í [Hvernig á að flytja inn launafærslur](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="bf9ae-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="bf9ae-109">Eftirlitsgreiðslan um Ceridian Payroll gerir þér kleift að flytja inn launatölvur frá þjónustu Ceridian Power / Payroll (US) og Ceridian PowerPay (Kanada).</span><span class="sxs-lookup"><span data-stu-id="bf9ae-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf9ae-110">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bf9ae-110">See Also</span></span>
<span data-ttu-id="bf9ae-111">[Sérstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="bf9ae-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="bf9ae-112">[Fjármál](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="bf9ae-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="bf9ae-113">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf9ae-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

