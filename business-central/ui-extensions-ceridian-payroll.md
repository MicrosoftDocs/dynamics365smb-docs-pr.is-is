---
title: "Flytja inn launagögn með Ceridian Payroll-viðbótinni | Microsoft Docs"
description: "Nota skal þessa viðbót til að flytja inn launafærslur frá Ceridian HR/Payroll (BNA) og Ceridian PowerPay (Kanada) þjónustunum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7df17702abafd834976527978f1caadffb590ab4
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="5d202-103">Ceridian Payroll viðbót</span><span class="sxs-lookup"><span data-stu-id="5d202-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="5d202-104">Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="5d202-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="5d202-105">Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir í gluggann **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="5d202-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="5d202-106">Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="5d202-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="5d202-107">Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.</span><span class="sxs-lookup"><span data-stu-id="5d202-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="5d202-108">Frekari upplýsingar er að finna í [innflutningur launafærsla](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="5d202-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="5d202-109">Eftirlitsgreiðslan um Ceridian Payroll gerir þér kleift að flytja inn launatölvur frá þjónustu Ceridian Power / Payroll (US) og Ceridian PowerPay (Kanada).</span><span class="sxs-lookup"><span data-stu-id="5d202-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d202-110">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5d202-110">See Also</span></span>
<span data-ttu-id="5d202-111">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="5d202-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="5d202-112">[Fjármál](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="5d202-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="5d202-113">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5d202-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

