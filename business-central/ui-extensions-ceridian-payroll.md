---
title: Flytja inn launagögn með Ceridian Payroll-viðbótinni | Microsoft Docs
description: Nota skal þessa viðbót til að flytja inn launafærslur frá Ceridian HR/Payroll (BNA) og Ceridian PowerPay (Kanada) þjónustunum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: ed3ba9f10ce24c97760dce972aa96134f1bc1119
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799422"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="123e1-103">Ceridian Payroll viðbót</span><span class="sxs-lookup"><span data-stu-id="123e1-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="123e1-104">Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="123e1-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="123e1-105">Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir á síðuna **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="123e1-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="123e1-106">Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="123e1-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="123e1-107">Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.</span><span class="sxs-lookup"><span data-stu-id="123e1-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="123e1-108">Frekari upplýsingar er að finna í [innflutningur launafærsla](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="123e1-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="123e1-109">Eftirlitsgreiðslan um Ceridian Payroll gerir þér kleift að flytja inn launatölvur frá þjónustu Ceridian Power / Payroll (US) og Ceridian PowerPay (Kanada).</span><span class="sxs-lookup"><span data-stu-id="123e1-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="123e1-110">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="123e1-110">See Also</span></span>
<span data-ttu-id="123e1-111">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="123e1-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="123e1-112">[Fjármál](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="123e1-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="123e1-113">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="123e1-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
