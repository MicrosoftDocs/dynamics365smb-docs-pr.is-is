---
title: Breyta því hvernig skýrsla lítur út með því að velja annað útlit | Microsoft Docs
description: Þú getur notað mismunandi útlit fyrir skýrslu, og skipt á milli útlits til að breyta því hvernig skýrsla lítur út.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07de4be7bc516cf9f4b802a48dc59293b1992f5f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315253"
---
# <a name="change-the-current-report-layout"></a><span data-ttu-id="1b6e9-103">Breyta núverandi skýrsluútliti</span><span class="sxs-lookup"><span data-stu-id="1b6e9-103">Change the Current Report Layout</span></span>
<span data-ttu-id="1b6e9-104">Skýrsla getur verið sett upp með fleiri en eitt skýrsluútliti, sem þú getur svo skipt milli eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="1b6e9-105">Með hliðsjón af útlitinu sem er í boði fyrir skýrslu er hægt að velja að nota innbyggt RDLC-skýrsluútlit, innbyggt Word-skýrsluútlit eða sérsniðið útlit.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="1b6e9-106">Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="1b6e9-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

> [!TIP]  
> <span data-ttu-id="1b6e9-107">Skýrslur skjala (ekki lista) sem nota Word-skýrsluútlit eru venjulega hraðari en þær sem nota RDLC-skýrsluútlit.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-107">Document reports (not lists) that use a Word report layout are typically faster than those that use an RDLC report layout.</span></span> <span data-ttu-id="1b6e9-108">Ef þú hefur þess vegna kost á því að velja milli Word- eða RDLC-skýrsluútlits fyrir skýrslu skjals, skaltu nota Word-skýrsluútlit fyrir bestu afköstin.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-108">So if you have the option to choose between a Word or RDLC report layout for a document report, use the Word report layout for the best performance.</span></span>  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="1b6e9-109">Til að breyta útlitinu sem er notað í skýrslu</span><span class="sxs-lookup"><span data-stu-id="1b6e9-109">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="1b6e9-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Val á útliti skýrslu** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="1b6e9-111">Síðan **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum Fyrirtæki efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-111">The **Report Layout Selection** page lists all the reports that are available for the company that is specified in the Company field at the top of the page.</span></span> <span data-ttu-id="1b6e9-112"> Reiturinn valið útlit tilgreinir útlitið sem er verið að nota á skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-112">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="1b6e9-113">Stilltu reitinn **Fyrirtæki** efst á síðunni á fyrirtækið með skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-113">Set the **Company** field at the top of the page to the company that includes the report.</span></span>
3. <span data-ttu-id="1b6e9-114">Til að breyta útliti sem er notað í skýrslu skal velja röðina fyrir skýrsluna í listanum og stilla svo **valið útlit** reitinn á einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="1b6e9-114">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="1b6e9-115">RDLC (innbyggt Notar) innbyggt RDLC skýrsluútlit í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-115">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="1b6e9-116">Word (innbyggt) Notar innbyggt Word skýrsluútlit í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-116">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="1b6e9-117">Sérsniðið, Notar sérsniðið útlit í skýrslu.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-117">Custom, uses a custom layout on the report.</span></span>  

<span data-ttu-id="1b6e9-118">Hægt er að sjá hvaða sérsniðin útlit eru í boði fyrir skýrsluna í upplýsingareitnum **Skýrsluútlitshluti**.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-118">You can see which custom layouts are available for the report in the **Report Layouts Part** FactBox.</span></span> <span data-ttu-id="1b6e9-119">Ef engin sérsniðin útlit eru til fyrir skýrsluna þarf að búa það til.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-119">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="1b6e9-120">Ef þú velur þennan valkost skaltu fara í næsta ferli til að tilgreina sérsniðið útlit´ sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-120">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

> [!NOTE]
> <span data-ttu-id="1b6e9-121">Ef þú velur **RDLC (innbyggt)** eða **Word (innbyggt)** og færð villuboð um að skýrslan vilji ekki útlit af sérstakri gerð, verðurðu að velja annað útlit eða búa til sérsniðin skýrsla af þeirri gerð sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-121">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="1b6e9-122">Ef þú velur innbyggt RDLC skýrsluútlit, þá þarf ekkert að gera og útlitið er notað næst þegar skýrslan er keyrð.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-122">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="1b6e9-123">Til að tilgreina sérsniðið útlit skýrslu</span><span class="sxs-lookup"><span data-stu-id="1b6e9-123">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="1b6e9-124">Þú tilgreinir hvaða sérsniðið útlit á að nota á skýrsluna af síðunni **sérsniðið skýrsluútlit**.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-124">You specify which custom layout to use on the report from the **Custom Report Layouts** page.</span></span> <span data-ttu-id="1b6e9-125">Ef síðan **sérsniðið skýrsluútlit** er ekki opin skaltu velja leitarhnappinn í **Lýsing á útliti skýrslu**.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-125">If the **Custom Report Layouts** page is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="1b6e9-126">Á síðunni **Sérsniðið skýrsluútlit** skal velja línuna yfir sérsniðna útlitið sem á að nota og lokið svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-126">On the **Custom Report Layouts** page, select the row for custom layout that you want to use, and then close the page.</span></span>

<span data-ttu-id="1b6e9-127">Þú ferð til baka á síðuna **sérsniðið skýrsluútlit val**.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-127">You return to the **Report Layout Selection** page.</span></span> <span data-ttu-id="1b6e9-128">Heiti valins sérsniðins útlits er birt í reitnum **sérsniðið skýrsluútlit**.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-128">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="1b6e9-129">Sérsniðið útlit verður notað í næsta skipti sem skýrslan er keyrð.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-129">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b6e9-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1b6e9-130">See Also</span></span>
[<span data-ttu-id="1b6e9-131">Stjórnun skýrsluútlita</span><span class="sxs-lookup"><span data-stu-id="1b6e9-131">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="1b6e9-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b6e9-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
