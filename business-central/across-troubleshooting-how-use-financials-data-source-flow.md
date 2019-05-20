---
title: Samþætting úrræðaleitar við Microsoft Flow| Microsoft Docs
description: Notandi getur leitað úrræða um það hvernig hann getur gert Business Central-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 8a43df89261867f80ba16782cde92b040ce180c8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240235"
---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="17f1a-103">Samþætting úrræðaleitar við Microsoft Flow - Umbeðin slóð of löng</span><span class="sxs-lookup"><span data-stu-id="17f1a-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="17f1a-104">Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="17f1a-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="17f1a-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flæði.</span><span class="sxs-lookup"><span data-stu-id="17f1a-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="17f1a-106">Ef verið er að búa til Microsoft Flow með [!INCLUDE[d365fin](includes/d365fin_md.md)] tengi kunna að birtast villuboð um að umbeðna slóðin sé of löng eftir að flæðið hefur verið búið til, á borð við: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="17f1a-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="17f1a-107">Stofnar</span><span class="sxs-lookup"><span data-stu-id="17f1a-107">Cause</span></span>
<span data-ttu-id="17f1a-108">Til að flæði fari af stað leitar það að breytingum í gögnum.</span><span class="sxs-lookup"><span data-stu-id="17f1a-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="17f1a-109">Við ákvörðun á því hvort gögn hafi breyst ber tengið saman gögn í skyndiminni við ný gögn sem beðið er um frá uppruna.</span><span class="sxs-lookup"><span data-stu-id="17f1a-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="17f1a-110">Ef gagnafyrirspurnin býr til vefslóð sem er of löng mistekst hún.</span><span class="sxs-lookup"><span data-stu-id="17f1a-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="17f1a-111">Algengar ástæður kunna að vera:</span><span class="sxs-lookup"><span data-stu-id="17f1a-111">Common causes may include:</span></span>
- <span data-ttu-id="17f1a-112">Allar upprunatöflur yfir 250 línur</span><span class="sxs-lookup"><span data-stu-id="17f1a-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="17f1a-113">Upprunatafla inniheldur þúsundir færslna</span><span class="sxs-lookup"><span data-stu-id="17f1a-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="17f1a-114">Hjáleið</span><span class="sxs-lookup"><span data-stu-id="17f1a-114">Workaround</span></span>
<span data-ttu-id="17f1a-115">Fylgið eftirfarandir skrefum til að leysa vandamálið.</span><span class="sxs-lookup"><span data-stu-id="17f1a-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="17f1a-116">Velja að breyta flæði sem mistekst.</span><span class="sxs-lookup"><span data-stu-id="17f1a-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="17f1a-117">Víkkið **Sýna ítarlega valkosti** á flæðiskveikjunni.</span><span class="sxs-lookup"><span data-stu-id="17f1a-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="17f1a-118">Í reitnum **Sleppa talningu** skal slá inn fjölda færslna sem á að sleppa.</span><span class="sxs-lookup"><span data-stu-id="17f1a-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="17f1a-119">Ef taflan sem er verið að nota er til dæmis með gagnaveitu sem inniheldur 4.000 færslur skal slá inn 4.000 sem fjöldanns em á að sleppa.</span><span class="sxs-lookup"><span data-stu-id="17f1a-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="17f1a-120">Uppfærið flæðið.</span><span class="sxs-lookup"><span data-stu-id="17f1a-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="17f1a-121">Tengið er í beta-útgáfu.</span><span class="sxs-lookup"><span data-stu-id="17f1a-121">The connector is currently in Beta.</span></span> <span data-ttu-id="17f1a-122">Uppfærist í það hvernig unnið er úr gagnabreytingum í framtíðarútgáfum.</span><span class="sxs-lookup"><span data-stu-id="17f1a-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="17f1a-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="17f1a-123">See Also</span></span>
<span data-ttu-id="17f1a-124">[Notkun [!INCLUDE[d365fin](includes/d365fin_md.md)] í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="17f1a-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="17f1a-125">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="17f1a-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="17f1a-126">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="17f1a-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="17f1a-127">[Vinna með notendur og heimildir](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="17f1a-127">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="17f1a-128">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="17f1a-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="17f1a-129">Fjármál</span><span class="sxs-lookup"><span data-stu-id="17f1a-129">Finance</span></span>](finance.md)  
