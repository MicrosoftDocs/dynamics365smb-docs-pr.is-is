---
title: Hvernig á að setja upp skjalaskiptaþjónustu | Microsoft Docs
description: Notaður er ytri þjónustuveitandi til að skiptast á rafrænum skjölum við viðskiptafélögum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0217f077c9c38603b9e3ff945fd47394c5b943bb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384375"
---
# <a name="set-up-a-document-exchange-service"></a><span data-ttu-id="1dcde-103">Setja upp skjalaskiptaþjónustu</span><span class="sxs-lookup"><span data-stu-id="1dcde-103">Set Up a Document Exchange Service</span></span>
<span data-ttu-id="1dcde-104">Notaður er ytri þjónustuveitandi til að skiptast á rafrænum skjölum við viðskiptafélögum.</span><span class="sxs-lookup"><span data-stu-id="1dcde-104">You use an external service provider to exchange electronic documents with your trading partners.</span></span> <span data-ttu-id="1dcde-105">Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="1dcde-105">For more information, see [Exchanging Data Electronically](across-data-exchange.md).</span></span>  

## <a name="to-set-up-a-document-exchange-service"></a><span data-ttu-id="1dcde-106">Setja upp skjalaskiptaþjónustu</span><span class="sxs-lookup"><span data-stu-id="1dcde-106">To set up a document exchange service</span></span>  
1. <span data-ttu-id="1dcde-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning gagnaskiptaþjónustu** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1dcde-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Doc. Exch. Service Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1dcde-108">Fylla inn í reitina eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="1dcde-108">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1dcde-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="1dcde-109">Field</span></span>|<span data-ttu-id="1dcde-110">Description</span><span class="sxs-lookup"><span data-stu-id="1dcde-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1dcde-111">**Notandagerandi**</span><span class="sxs-lookup"><span data-stu-id="1dcde-111">**User Agent**</span></span>|<span data-ttu-id="1dcde-112">Færa inn allan texta sem hægt er að nota til að auðkenna fyrirtækið í skjalaskiptaferlinu.</span><span class="sxs-lookup"><span data-stu-id="1dcde-112">Enter any text that can be used to identify your company in document exchange processes.</span></span>|  
    |<span data-ttu-id="1dcde-113">**Leigjandakenni gagnaskipti**</span><span class="sxs-lookup"><span data-stu-id="1dcde-113">**Doc. Exch. Tenant ID**</span></span>|<span data-ttu-id="1dcde-114">Færa skal inn leigjanda í skjalaþjónustan sem stendur fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="1dcde-114">Enter the tenant in the document exchange service that represents your company.</span></span> <span data-ttu-id="1dcde-115">Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="1dcde-115">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="1dcde-116">**Virk**</span><span class="sxs-lookup"><span data-stu-id="1dcde-116">**Enabled**</span></span>|<span data-ttu-id="1dcde-117">Tilgreina hvort þjónustan er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="1dcde-117">Specify if the service is enabled.</span></span> <span data-ttu-id="1dcde-118">**Athugið:** Þegar þjónustan er virkjuð eru minnst tvær verkraðarfærslur stofnaðar til að vinna með umferð rafrænna skjala inn og út úr [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1dcde-118">**Note:**  As soon as you enable the service, at least two job queue entries are created to process the traffic of electronic documents in and out of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1dcde-119">Þegar þú slekkur á þjónustu er verkraðarfærslum eytt.</span><span class="sxs-lookup"><span data-stu-id="1dcde-119">When you disable the service, the job queue entries are deleted.</span></span>|  
    |<span data-ttu-id="1dcde-120">**Skráningarvefslóð**</span><span class="sxs-lookup"><span data-stu-id="1dcde-120">**Signup URL**</span></span>|<span data-ttu-id="1dcde-121">Tilgreina vefsíðuna þar sem nýskráning fyrir skjalskiptiþjónustuna fer fram.</span><span class="sxs-lookup"><span data-stu-id="1dcde-121">Specify the web page where you sign up for the document exchange service.</span></span>|  
    |<span data-ttu-id="1dcde-122">**Vefslóð þjónustu**</span><span class="sxs-lookup"><span data-stu-id="1dcde-122">**Service URL**</span></span>|<span data-ttu-id="1dcde-123">Tilgreina veffang skjalaskiptiþjónustunna sem verður kölluð þegar rafræn skjöl eru send og tekið við þeim.</span><span class="sxs-lookup"><span data-stu-id="1dcde-123">Specify the address of the document exchange service, which will be called when you send and receive electronic documents.</span></span>|  
    |<span data-ttu-id="1dcde-124">**Innskráningarvefslóð**</span><span class="sxs-lookup"><span data-stu-id="1dcde-124">**Login URL**</span></span>|<span data-ttu-id="1dcde-125">Tilgreina innskráningarsíðu fyrir skjalaskiptiþjónustuna, sem er þar sem slegið er inn notandanafn og aðgangsorð fyrirtækis til að skrá sig inn í þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="1dcde-125">Specify the logon page for the document exchange service, which is where you enter your company’s user name and password to log on to the service.</span></span>|  
    |<span data-ttu-id="1dcde-126">**Lykill neytanda**</span><span class="sxs-lookup"><span data-stu-id="1dcde-126">**Consumer Key**</span></span>|<span data-ttu-id="1dcde-127">Færa skal inn þríliða OAuth-lykilinn fyrir neytendalykilinn.</span><span class="sxs-lookup"><span data-stu-id="1dcde-127">Enter the 3-legged OAuth key for the consumer key.</span></span> <span data-ttu-id="1dcde-128">Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="1dcde-128">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="1dcde-129">**Leyndarmál neytanda**</span><span class="sxs-lookup"><span data-stu-id="1dcde-129">**Consumer Secret**</span></span>|<span data-ttu-id="1dcde-130">Færa skal inn leyndarmálið sem verndar neytendalykilinn.</span><span class="sxs-lookup"><span data-stu-id="1dcde-130">Enter the secret that protects the consumer key.</span></span> <span data-ttu-id="1dcde-131">Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="1dcde-131">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="1dcde-132">**Tákn**</span><span class="sxs-lookup"><span data-stu-id="1dcde-132">**Token**</span></span>|<span data-ttu-id="1dcde-133">Færa skal inn þríliða OAuth-lykilinn fyrir tákn.</span><span class="sxs-lookup"><span data-stu-id="1dcde-133">Enter the 3-legged OAuth key for the token.</span></span> <span data-ttu-id="1dcde-134">Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="1dcde-134">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="1dcde-135">**Leyndarmál greiðslueiningar**</span><span class="sxs-lookup"><span data-stu-id="1dcde-135">**Token Secret**</span></span>|<span data-ttu-id="1dcde-136">Færa skal inn leyndarmálið sem verndar táknið.</span><span class="sxs-lookup"><span data-stu-id="1dcde-136">Enter the secret that protects the token.</span></span> <span data-ttu-id="1dcde-137">Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="1dcde-137">This is provided by the document exchange service provider.</span></span>|  

    > [!NOTE]  
    > <span data-ttu-id="1dcde-138">Innskráningargögnin þín eru sjálfkrafa dulrituð.</span><span class="sxs-lookup"><span data-stu-id="1dcde-138">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dcde-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1dcde-139">See Also</span></span>  
[<span data-ttu-id="1dcde-140">Setja upp gagnaskipti</span><span class="sxs-lookup"><span data-stu-id="1dcde-140">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
[<span data-ttu-id="1dcde-141">Rafræn gagnaskipti</span><span class="sxs-lookup"><span data-stu-id="1dcde-141">Exchanging Data Electronically</span></span>](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]