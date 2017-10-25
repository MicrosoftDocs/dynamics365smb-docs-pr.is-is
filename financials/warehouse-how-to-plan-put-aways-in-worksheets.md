---
title: "Hvernig á að áætla frágang á vinnublöðum | Microsoft Docs"
description: "Ef birgðageymslan krefst bæði frágangs- og móttökuvinnslu og áætla á frágangsleiðbeiningar fyrir margar móttökur, í stað þess að fara eftir leiðbeiningum sem stofnaðar eru fyrir einstakar bókaðar móttökur, er hægt að nota frágangsvinnublaðið."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 99c3ac10460a62ee23294cfd0d8c25709c37901b
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-put-aways-in-worksheets"></a><span data-ttu-id="a0c08-103">Hvernig á að áætla frágang á vinnublöðum</span><span class="sxs-lookup"><span data-stu-id="a0c08-103">How to: Plan Put-aways in Worksheets</span></span>
<span data-ttu-id="a0c08-104">Ef birgðageymslan krefst bæði frágangs- og móttökuvinnslu og áætla á frágangsleiðbeiningar fyrir margar móttökur, í stað þess að fara eftir leiðbeiningum sem stofnaðar eru fyrir einstakar bókaðar móttökur, er hægt að nota frágangsvinnublaðið.</span><span class="sxs-lookup"><span data-stu-id="a0c08-104">If your location requires both put-away and receive processing, and you want to plan put-away instructions for a number of receipts, rather than have employees follow the instructions that the program creates for separate posted receipts, you can use the put-away worksheet.</span></span>  

<span data-ttu-id="a0c08-105">Eigi að setja vöruhúsið þannig upp að móttökulínur séu tiltækar á frágangsvinnublaðinu um leið og þær hafa verið bókaðar þarf að setja gátmerki í reitinn **Nota vinnublað frágangs** á flýtiflipanum **Vöruhús** á birgðageymsluspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="a0c08-105">To set up your warehouse so that receipt lines are available to you in the put-away worksheet as soon as they are posted, select the **Use Put-away Worksheet** field on the **Warehouse** FastTab of the location card.</span></span> <span data-ttu-id="a0c08-106">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="a0c08-106">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

<span data-ttu-id="a0c08-107">Ef gátmerki er ekki sett í þennan reit eru frágangsleiðbeiningar stofnaðar sjálfkrafa fyrir móttökur þegar þær eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="a0c08-107">If you do not select this field, the program will automatically create put-away instructions for receipts as they are posted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a0c08-108">Óháð stöðu reitarins **Nota vinnublað frágangs** á birgðageymsluspjaldinu er alltaf hægt að sækja frágangsleiðbeiningalínur (bókaðar móttökulínur) í frágangsvinnublaðið með því að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="a0c08-108">Regardless of the status of the **Use Put-away Worksheet** field on the location card, you can always get put-away instruction lines, that is, posted receipt lines, into the put-away worksheet by doing the following:</span></span>  
>   
>  1.  <span data-ttu-id="a0c08-109">Í glugganum **Vöruhús – frágangur** er ýtt á Ctrl+D til að eyða öllum frágangsleiðbeiningunum eða línurnar sem á að vinna með á vinnublaðinu valdar og þeim eytt.</span><span class="sxs-lookup"><span data-stu-id="a0c08-109">In the **Warehouse Put-away** window, press Ctrl+D to delete the entire put-away instruction, or select the lines that you want to process in the worksheet and delete them.</span></span>  
> 2.  <span data-ttu-id="a0c08-110">Þessu er haldið áfram þar til línunum sem vinna á með á vinnublaðinu hefur verið eytt.</span><span class="sxs-lookup"><span data-stu-id="a0c08-110">Continue the process in as many put-aways as you wish, until you have deleted the lines you want to work on in the worksheet.</span></span> <span data-ttu-id="a0c08-111">Veljið nú **Vinnublöð frágangs** og haldið áfram að áætla.</span><span class="sxs-lookup"><span data-stu-id="a0c08-111">Now choose **Put-away Worksheets** and proceed with planning.</span></span>  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a><span data-ttu-id="a0c08-112">Leiðbeiningar áætlaðar á vinnublaði frágangs:</span><span class="sxs-lookup"><span data-stu-id="a0c08-112">To plan instructions in the put-away worksheet</span></span>  
1.  <span data-ttu-id="a0c08-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Frágangsvinnublað** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="a0c08-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Put-away Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a0c08-114">Valið er **Sækja vöruhúsaskjöl** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="a0c08-114">Choose the **Get Warehouse Documents** action.</span></span> <span data-ttu-id="a0c08-115">Glugginn **Frágangsval** opnast.</span><span class="sxs-lookup"><span data-stu-id="a0c08-115">The **Put-away Selection** window opens.</span></span>  

    <span data-ttu-id="a0c08-116">Hægt er að sjá allar bókaðar móttökur og skráðan innanhússfrágang sem send hafa verið í frágangsaðgerðina, þar á meðal þá sem frágangsleiðbeiningar hafa þegar verið stofnaðar fyrir.</span><span class="sxs-lookup"><span data-stu-id="a0c08-116">You see all the posted receipts and registered internal put-aways that have been forwarded to the put-away function, including those for which put-away instructions have already been created.</span></span> <span data-ttu-id="a0c08-117">Skjöl með frágangslínur sem gengið hefur verið frá að fullu og skráðar birtast ekki á þessum lista.</span><span class="sxs-lookup"><span data-stu-id="a0c08-117">Documents with put-away lines that have been completely put away and registered are not shown on this list.</span></span>  

3. <span data-ttu-id="a0c08-118">Skjölin sem vinna á með á vinnublaðinu eru valin.</span><span class="sxs-lookup"><span data-stu-id="a0c08-118">Select the documents that you want to work on in the worksheet.</span></span> <span data-ttu-id="a0c08-119">Hægt er að vinna með línur úr nokkrum skjölum í einu.</span><span class="sxs-lookup"><span data-stu-id="a0c08-119">You can work on lines from several documents at the same time.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a0c08-120">Ef reynt er að velja móttöku eða innanhússfrágang sem leiðbeiningar hafa þegar verið stofnaðar fyrir allar línur í, birtist tilkynning um það að ekkert sé til meðhöndlunar.</span><span class="sxs-lookup"><span data-stu-id="a0c08-120">If you try to select a receipt or internal put-away document for which you have already created instructions for all its lines, the program informs you that there is nothing to handle.</span></span>  

4. <span data-ttu-id="a0c08-121">Reiturinn **Röðunaraðferð** er fylltur út til að raða línunum eins og óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a0c08-121">Fill in the **Sorting Method** field to sort the lines the way you prefer.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a0c08-122">Röðun lína á vinnublaðinu flyst ekki sjálfkrafa í frágangsleiðbeiningar en sömu röðunaraðferðir eru fyrir hendi ásamt hólfaflokkun.</span><span class="sxs-lookup"><span data-stu-id="a0c08-122">The way the lines are sorted in the worksheet does not carry through automatically to the put-away instruction, but the same sorting possibilities exist, along with bin ranking.</span></span> <span data-ttu-id="a0c08-123">Þannig er auðvelt að endurgera línuröðunina á vinnublaðinu þegar frágangsleiðbeiningarnar eru stofnaðar eða með því að raða í frágangsleiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="a0c08-123">The line order you plan in the worksheet is thus easily recreated when you create the put-away instructions or by sorting in the put-away instructions.</span></span>  

5.  <span data-ttu-id="a0c08-124">Fylla inn í reitinn **Magn til afgreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="a0c08-124">Fill in the **Qty. to Handle** field.</span></span> <span data-ttu-id="a0c08-125">Velja aðgerðina **Færa sjálfkr. magn til afgr.** eða fyllið út reitina handvirkt.</span><span class="sxs-lookup"><span data-stu-id="a0c08-125">Choose the **Autofill Qty.to Handle** action, or fill in the fields manually.</span></span>  
6.  <span data-ttu-id="a0c08-126">Ef þess þarf er línunum breytt handvirkt.</span><span class="sxs-lookup"><span data-stu-id="a0c08-126">If necessary, edit the lines manually.</span></span> <span data-ttu-id="a0c08-127">Hægt er að eyða línum, til dæmis ef setja þarf sumar vörur í hólf sem er langt frá hólfunum fyrir hinar vörurnar.</span><span class="sxs-lookup"><span data-stu-id="a0c08-127">You can delete lines, for example, if some items need to be put away in a bin far away from the bins for the other items.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a0c08-128">Línum er aðeins eytt af þessu vinnublaði, ekki frágangsvallistanum.</span><span class="sxs-lookup"><span data-stu-id="a0c08-128">Lines deleted are only deleted from this worksheet, not from the put-away selection list.</span></span>  

7.  <span data-ttu-id="a0c08-129">Veldu aðgerðina **Stofna frágang**.</span><span class="sxs-lookup"><span data-stu-id="a0c08-129">Choose the **Create Put-away** action.</span></span> <span data-ttu-id="a0c08-130">Glugginn **Stofna fylgiskjal** opnast, þar sem hægt er að bæta við upplýsingum í fráganginn sem verið er að stofna, á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a0c08-130">The **Create Document** window opens, where you can add more information to the put-away you are creating, as follows:</span></span>  

    -   <span data-ttu-id="a0c08-131">Hægt er að úthluta fráganginum á tiltekinn starfsmann.</span><span class="sxs-lookup"><span data-stu-id="a0c08-131">You can assign the put-away to a specific employee.</span></span>  
    -   <span data-ttu-id="a0c08-132">Hægt er að raða frágangsleiðbeiningalínum eins og gert var á vinnublaðinu eða eftir flokkun hólfa.</span><span class="sxs-lookup"><span data-stu-id="a0c08-132">You can sort the put-away instruction lines as you did in the worksheet or by bin ranking.</span></span> <span data-ttu-id="a0c08-133">Þegar raðað er eftir flokkun hólfa birtast Taka-línurnar fyrst þar sem flestar móttökulínurnar hafa hólfaflokkunina 0 og Setja línurnar birtast síðast í hækkandi röð eftir hólfaflokkun.</span><span class="sxs-lookup"><span data-stu-id="a0c08-133">When you sort according to bin ranking, the Take lines appear first, since most receipt bins have a 0 bin ranking, and the Place lines appear last, starting with the bins with the lowest bin ranking.</span></span> <span data-ttu-id="a0c08-134">Hafi vöruhúsið verið skipulagt þannig að hólf með svipaða flokkun séu næst hvert öðru, sparar röðun með þessum hætti starfsmönnunum sporin.</span><span class="sxs-lookup"><span data-stu-id="a0c08-134">If you have structured your warehouse so bins of similar bin ranking are side by side, sorting lines in this way will ultimately save steps for your warehouse employees.</span></span>  
    -   <span data-ttu-id="a0c08-135">Hægt er að fela millilínurnar sem stofnaðar eru þegar kerfið skiptir stórri mælieiningu í smærri mælieiningar með því að velja reitinn **Setja einingaskiptaafmörkun**.</span><span class="sxs-lookup"><span data-stu-id="a0c08-135">You can choose not to see the intermediate lines created when the program breaks a larger unit of measure to smaller units of measure by selecting the **Set Breakbulk Filter** field.</span></span> <span data-ttu-id="a0c08-136">Frekari upplýsingar, sjá [Hvernig skal: Virkja sjálfvirk einingaskipti með beinum frágangi og tínslu] (vöruhús_virkja_sjálfvirk_einingaskipti_með_beinum_frágangi_og_tínslum_md).</span><span class="sxs-lookup"><span data-stu-id="a0c08-136">For more information, see [How to: Enable Automatic Breaking Bulk with Directed Put-away and Pick] (warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).</span></span>  
    -   <span data-ttu-id="a0c08-137">Hægt er að velja að ekki sé sjálfkrafa fyllt út í reitinn **Magn til afgreiðslu** í frágangsleiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="a0c08-137">You can choose not to have the **Qty. to Handle** field automatically filled in on the put-away instructions.</span></span>  
    -   <span data-ttu-id="a0c08-138">Hægt er að prenta skjalið strax.</span><span class="sxs-lookup"><span data-stu-id="a0c08-138">You can choose to print the document immediately.</span></span>  

8.  <span data-ttu-id="a0c08-139">Veldu hnappinn **Í lagi** og þá stofnar kerfið fráganginn samkvæmt óskum notandans.</span><span class="sxs-lookup"><span data-stu-id="a0c08-139">Choose the **OK** button, and the program creates the put-away according to your requests.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0c08-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0c08-140">See Also</span></span>  
[<span data-ttu-id="a0c08-141">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="a0c08-141">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="a0c08-142">Birgðir</span><span class="sxs-lookup"><span data-stu-id="a0c08-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a0c08-143">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="a0c08-143">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="a0c08-144">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="a0c08-144">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="a0c08-145">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="a0c08-145">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="a0c08-146">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0c08-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

