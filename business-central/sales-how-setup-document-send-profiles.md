---
title: Setja upp útvaldar aðferðir við að senda söluskjöl | Microsoft Docs
description: Lýsir því hvernig setja skal upp aðferðir við senda söluskjöl samkvæmt óskum viðskiptamanna, t.d. tölvupóstur, PDF, rafræn skjöl osfrv.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: f72c4eba9ad199c559f24d29b712b6636bec47e0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800067"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="a0fe6-103">Setja upp sendisnið skjala</span><span class="sxs-lookup"><span data-stu-id="a0fe6-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="a0fe6-104">Hægt er að setja upp hvern viðskiptavin með valinni aðferð við að senda söluskjöl til að þurfa ekki að velja sendingarvalkost í hvert skipti sem aðgerðin **Bóka og senda** er valin.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="a0fe6-105">Á síðunni **Sendisnið skjala** er hægt að setja upp ólík sendisnið, sem hægt er að velja úr í reitnum **Sendisnið skjala** á viðskiptamannaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="a0fe6-106">Hægt er að velja gátreitinn **Sjálfgefið** til að tilgreina að sendingarsniðið sé sjálfgefið snið fyrir alla viðskiptamenn, nema fyrir viðskiptamenn þar sem reiturinn **Sendisnið skjala** er fylltur út með öðru sendingarsniði.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="a0fe6-107">Þegar aðgerðin **Bóka og senda** er valin á söluskjali mun svarglugginn **Bóka og senda staðfestingu** sýna sendingarsnið sem er í notkun, annað hvort það sem er sett upp fyrir viðskiptamann eða það sem er sjálfgefið fyrir alla viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="a0fe6-108">Í svarglugga er hægt að breyta sendingarsniði fyrir þetta söluskjalið.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="a0fe6-109">Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="a0fe6-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="a0fe6-110">Að setja upp sendingarsnið skjala</span><span class="sxs-lookup"><span data-stu-id="a0fe6-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="a0fe6-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **forstilling skjalasendingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0fe6-112">Á síðunni **Sendisnið skjala** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="a0fe6-113">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="a0fe6-114">Til að tilgreina sendingarsnið á viðskiptamannaspjaldi</span><span class="sxs-lookup"><span data-stu-id="a0fe6-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="a0fe6-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0fe6-116">Opnið spjald viðskiptamanns þar sem á að setja upp sendingarsnið.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="a0fe6-117">Í reitnum **Forstilling sendingar skjals** snið skaltu velja snið sem þú hefur sett upp eins og lýst er í fyrri málsmeðferð.</span><span class="sxs-lookup"><span data-stu-id="a0fe6-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0fe6-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0fe6-118">See Also</span></span>
[<span data-ttu-id="a0fe6-119">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="a0fe6-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="a0fe6-120">Sala</span><span class="sxs-lookup"><span data-stu-id="a0fe6-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a0fe6-121">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0fe6-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
