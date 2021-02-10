---
title: Flytja inn launagögn með Ceridian Payroll-viðbótinni
description: Nota skal þessa viðbót til að flytja inn launafærslur frá Ceridian HR/Payroll (BNA) og Ceridian PowerPay (Kanada) þjónustunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 717c8937ea4c057b51acb3c346d950d6b7c0a43e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757318"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="2a269-103">Ceridian Payroll viðbót</span><span class="sxs-lookup"><span data-stu-id="2a269-103">The Ceridian Payroll Extension</span></span>

<span data-ttu-id="2a269-104">Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="2a269-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="2a269-105">Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir á síðuna **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="2a269-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="2a269-106">Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="2a269-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="2a269-107">Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.</span><span class="sxs-lookup"><span data-stu-id="2a269-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="2a269-108">Frekari upplýsingar er að finna í [innflutningur launafærsla](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2a269-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="2a269-109">Eftirlitsgreiðslan um Ceridian Payroll gerir þér kleift að flytja inn launatölvur frá þjónustu Ceridian Power / Payroll (US) og Ceridian PowerPay (Kanada).</span><span class="sxs-lookup"><span data-stu-id="2a269-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a269-110">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2a269-110">See Also</span></span>

<span data-ttu-id="2a269-111">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2a269-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="2a269-112">Fjármál</span><span class="sxs-lookup"><span data-stu-id="2a269-112">Finance</span></span>](finance.md)  
<span data-ttu-id="2a269-113">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2a269-113">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
