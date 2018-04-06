---
title: "Uppsetning bókhaldslykla | Microsoft Docs"
description: "Þú breytir sjálfgefnum lyklum og í bókhaldslyklum og hægt er að bæta við nýjum lyklum."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1d0130dde256706460e58e5efc445bc5f4d5c595
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="67988-103">Uppsetning eða breyting á bókhaldslykli</span><span class="sxs-lookup"><span data-stu-id="67988-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="67988-104">Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn.</span><span class="sxs-lookup"><span data-stu-id="67988-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="67988-105"> inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="67988-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="67988-106">Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.</span><span class="sxs-lookup"><span data-stu-id="67988-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="67988-107">Bæta við eða breyta lyklum</span><span class="sxs-lookup"><span data-stu-id="67988-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="67988-108">Fyrir hvern bókhaldslykil er hægt að opna hvern einstakan fjárhagslykil og bæta við eða breyta stillingum.</span><span class="sxs-lookup"><span data-stu-id="67988-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="67988-109">Hægt er að eyða fjárhagsreikningur.</span><span class="sxs-lookup"><span data-stu-id="67988-109">You can delete a general ledger account.</span></span> <span data-ttu-id="67988-110">Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:</span><span class="sxs-lookup"><span data-stu-id="67988-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="67988-111">Staða reikningsins verður að vera núll.</span><span class="sxs-lookup"><span data-stu-id="67988-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="67988-112">Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur í glugganum **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.</span><span class="sxs-lookup"><span data-stu-id="67988-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="67988-113">Ef reiturinn **Athuga notkun fjárhagsr.** í glugganum **Uppsetning fjárhags** er valinn má ekki nota lykilinn í neinum bókunarflokkum eða bókunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="67988-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="67988-114"> kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="67988-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67988-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="67988-115">See Also</span></span>
[<span data-ttu-id="67988-116">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="67988-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="67988-117">Stjórna bankareikningum</span><span class="sxs-lookup"><span data-stu-id="67988-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="67988-118">Unnið með víddir</span><span class="sxs-lookup"><span data-stu-id="67988-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="67988-119">Flytja inn úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="67988-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="67988-120">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="67988-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

