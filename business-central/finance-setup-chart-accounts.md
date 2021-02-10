---
title: Uppsetning bókhaldslykilsins
description: Þú breytir sjálfgefnum lyklum og í bókhaldslyklum og hægt er að bæta við nýjum lyklum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b20c4680393fa13b260beca366c7e4ba04abb291
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750381"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="7a18f-103">Uppsetning eða breyting á bókhaldslykli</span><span class="sxs-lookup"><span data-stu-id="7a18f-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="7a18f-104">Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn.</span><span class="sxs-lookup"><span data-stu-id="7a18f-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="7a18f-105">inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="7a18f-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="7a18f-106">Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.</span><span class="sxs-lookup"><span data-stu-id="7a18f-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="7a18f-107">Bæta við eða breyta lyklum</span><span class="sxs-lookup"><span data-stu-id="7a18f-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="7a18f-108">Fyrir hvern bókhaldslykil er hægt að opna hvern einstakan fjárhagslykil og bæta við eða breyta stillingum.</span><span class="sxs-lookup"><span data-stu-id="7a18f-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7a18f-109">Hægt er að eyða fjárhagsreikningur.</span><span class="sxs-lookup"><span data-stu-id="7a18f-109">You can delete a general ledger account.</span></span> <span data-ttu-id="7a18f-110">Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:</span><span class="sxs-lookup"><span data-stu-id="7a18f-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="7a18f-111">Staða reikningsins verður að vera núll.</span><span class="sxs-lookup"><span data-stu-id="7a18f-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="7a18f-112">Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur á síðunni **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.</span><span class="sxs-lookup"><span data-stu-id="7a18f-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="7a18f-113">Ef reiturinn **Athuga notkun fjárhagsr.** á síðunni **Uppsetning fjárhags** er valinn má ekki nota lykilinn í neinum bókunarflokkum eða bókunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="7a18f-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="7a18f-114">kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="7a18f-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="7a18f-115">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="7a18f-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="7a18f-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7a18f-116">See Also</span></span>
[<span data-ttu-id="7a18f-117">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="7a18f-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="7a18f-118">Afstemming bankareikninga</span><span class="sxs-lookup"><span data-stu-id="7a18f-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="7a18f-119">Unnið með víddir</span><span class="sxs-lookup"><span data-stu-id="7a18f-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="7a18f-120">Flytja inn gögn úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="7a18f-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="7a18f-121">Vinna með fjárhagsskemu</span><span class="sxs-lookup"><span data-stu-id="7a18f-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="7a18f-122">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a18f-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]
