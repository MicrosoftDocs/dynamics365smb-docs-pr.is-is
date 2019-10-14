---
title: Flytja inn margar myndir af vörum úr ZIP-skrá| Microsoft Docs
description: Hægt er að flytja inn margar vörumyndir í einu. Gefðu einfaldlega myndaskránum þínum heiti sem samsvarar vörunúmerunum þínum, þjappaðu þeim í zip-skrá og notaðu síðan síðuna fyrir innflutning á vörumyndum til að stýra því hvaða vörumyndir á að flytja inn.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cfb80821177c0860413526b5bc529fa1bdeedf7b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309845"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="57c12-104">Flytja inn margar vörumyndir</span><span class="sxs-lookup"><span data-stu-id="57c12-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="57c12-105">Hægt er að flytja inn margar vörumyndir í einu.</span><span class="sxs-lookup"><span data-stu-id="57c12-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="57c12-106">Gefðu einfaldlega myndaskránum þínum heiti sem samsvarar vörunúmerunum þínum, þjappaðu þeim í ZIP-skrá og notaðu síðan síðuna **Flytja inn vörumyndir** til að stýra því hvaða vörumyndir á að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="57c12-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="57c12-107">Öll helstu skráarsnið eru studd.</span><span class="sxs-lookup"><span data-stu-id="57c12-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="57c12-108">Að skíra myndaskrár eftir vöruheitum og undirbúa ZIP-skrána</span><span class="sxs-lookup"><span data-stu-id="57c12-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="57c12-109">Á staðsetningunni sem vörumyndirnar þínar eru geymdar skal nefna hverja skrá samkvæmt númeri tengdrar vöru.</span><span class="sxs-lookup"><span data-stu-id="57c12-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="57c12-110">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="57c12-110">For example:</span></span>

    |<span data-ttu-id="57c12-111">Vörunr.</span><span class="sxs-lookup"><span data-stu-id="57c12-111">Item No.</span></span>|<span data-ttu-id="57c12-112">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="57c12-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="57c12-113">1000</span><span class="sxs-lookup"><span data-stu-id="57c12-113">1000</span></span>|<span data-ttu-id="57c12-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="57c12-114">1000.bmp</span></span>|
    |<span data-ttu-id="57c12-115">1001</span><span class="sxs-lookup"><span data-stu-id="57c12-115">1001</span></span>|<span data-ttu-id="57c12-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="57c12-116">1001.bmp</span></span>|
    |<span data-ttu-id="57c12-117">1002</span><span class="sxs-lookup"><span data-stu-id="57c12-117">1002</span></span>|<span data-ttu-id="57c12-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="57c12-118">1002.bmp</span></span>|

2. <span data-ttu-id="57c12-119">Safnaðu öllum skrám í ZIP-skrá.</span><span class="sxs-lookup"><span data-stu-id="57c12-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="57c12-120">Til dæmis í Windows Explorer skal velja skrárnar og síðan velja **Senda til**, **Þjöppuð mappa (zip-þjöppuð)**.</span><span class="sxs-lookup"><span data-stu-id="57c12-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="57c12-121">Að flytja inn myndir af vörum</span><span class="sxs-lookup"><span data-stu-id="57c12-121">To import item pictures</span></span>
1. <span data-ttu-id="57c12-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning birgða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="57c12-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="57c12-123">Velja skal aðgerðina **Flytja inn myndir**.</span><span class="sxs-lookup"><span data-stu-id="57c12-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="57c12-124">Í reitnum **Velja ZIP-skrá** skal velja viðeigandi Zip-möppu og síðan velja hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="57c12-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="57c12-125">Lína fyrir hverja vöru og mynd er búin til á síðunni **Flytja inn vörumyndir**.</span><span class="sxs-lookup"><span data-stu-id="57c12-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57c12-126">Fyrir vöruspjöld sem eru þegar með mynd er gátreiturinn **Mynd er þegar til** valinn.</span><span class="sxs-lookup"><span data-stu-id="57c12-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="57c12-127">Ef þú vilt ekki að fyrirliggjandi myndum verði skipt út skal hætta við val á gátreitnum **Skipta út myndum**.</span><span class="sxs-lookup"><span data-stu-id="57c12-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="57c12-128">Ef þú vilt ekki að einstökum myndum sem eru til verði skipt út skal eyða línunum sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="57c12-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="57c12-129">Velja skal aðgerðina **Flytja inn myndir**.</span><span class="sxs-lookup"><span data-stu-id="57c12-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="57c12-130">Reiturinn **Staða innflutnings** er uppfærður til að sýna hvort innflutningur á mynd hafi verið sleppt eða kláraður.</span><span class="sxs-lookup"><span data-stu-id="57c12-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="57c12-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="57c12-131">See Also</span></span>
[<span data-ttu-id="57c12-132">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="57c12-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="57c12-133">Stofnun númeraraða</span><span class="sxs-lookup"><span data-stu-id="57c12-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="57c12-134">Birgðir</span><span class="sxs-lookup"><span data-stu-id="57c12-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="57c12-135">Innkaup</span><span class="sxs-lookup"><span data-stu-id="57c12-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="57c12-136">Sala</span><span class="sxs-lookup"><span data-stu-id="57c12-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="57c12-137">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57c12-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
