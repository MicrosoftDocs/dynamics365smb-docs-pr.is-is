---
title: Word-sniðmát notuð fyrir mörg samskipti í einu | Microsoft Docs
description: Word-sniðmát geta auðveldað að búa til mörg skjöl í einu sem eru sérsniðin fyrir tilteknar einingar.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788556"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="57694-103">Word-sniðmát notuð fyrir mörg samskipti í einu</span><span class="sxs-lookup"><span data-stu-id="57694-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="57694-104">Microsoft Word-sniðmát geta auðveldað mörg samskipti í einu með einingum á borð við viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="57694-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="57694-105">Til dæmis er hægt að búa til bæklinga til að tilkynna viðskiptavinum um söluherferð, bréf til að tilkynna lánardrottnum um nýja innkaupastefnu eða boð til að fá tengiliði til að mæta á væntanlegan viðburð.</span><span class="sxs-lookup"><span data-stu-id="57694-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

<span data-ttu-id="57694-106">Hægt er að nota einingar í [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa sniðmátsins og bæta við innfellingarsvæðum til að sérsníða skjöl fyrir hverja einingu.</span><span class="sxs-lookup"><span data-stu-id="57694-106">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="57694-107">Innfellingarsvæðin koma úr einingunni í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="57694-107">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="57694-108">Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið.</span><span class="sxs-lookup"><span data-stu-id="57694-108">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="57694-109">Á síðunni **Word-sniðmát** er hægt að nota uppsetningarleiðbeiningu með hjálp til að sækja Zip-skrá sem inniheldur DataSource.txt og Word-sniðmátsskrá fyrir einingu.</span><span class="sxs-lookup"><span data-stu-id="57694-109">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="57694-110">Þegar búið er að setja upp sniðmátið og bæta við innfellingarsvæðum er sama leiðbeiningin notuð til að hlaða upp sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="57694-110">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="57694-111">Aðeins er hægt að nota Word-sniðmátið og skrár gagnagjafans sem sótt er af [!INCLUDE[prod_short](includes/prod_short.md)] og vista verður skrárnar í sömu staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="57694-111">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="57694-112">Þegar eining er valin þar sem á að stofna sniðmát, sýnir listinn allar einingar í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="57694-112">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="57694-113">Hins vegar er ekki hægt að stofna sniðmát fyrir allar einingar.</span><span class="sxs-lookup"><span data-stu-id="57694-113">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="57694-114">Ef heiti einingar inniheldur sérstafi á borð við **/**, **.**, **_** eða **-** er ekki hægt að stofna sniðmát fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="57694-114">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="57694-115">Heiti einingarinnar er sýnt í dálknum **Yfirskrift hlutar**.</span><span class="sxs-lookup"><span data-stu-id="57694-115">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="57694-116">Þegar sniðmátið er sett upp í Word er hægt í flipanum **Sendingar** að bæta við innfellingarsvæðum með því að velja **Setja inn innfellingarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="57694-116">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="57694-117">Ekki er hægt að nota innfellingarsvæði ef heiti reitsins inniheldur 40 stafi eða fleiri.</span><span class="sxs-lookup"><span data-stu-id="57694-117">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="57694-118">Til dæmis er ekki hægt að nota reitinn Company__Information_Customs_Permit_Date vegna þess að hann er með 40 stafi.</span><span class="sxs-lookup"><span data-stu-id="57694-118">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="57694-119">Þegar Word-sniðmátið er tilbúið er hægt á síðunni **Word-sniðmát** að velja **Nota** til að búa til skjölin.</span><span class="sxs-lookup"><span data-stu-id="57694-119">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="57694-120">Annaðhvort er hægt að búa til eitt skjal sem inniheldur hluta fyrir hverja einingu eða skipta aðgerðinni til að búa til nýtt skjal fyrir hverja einingu.</span><span class="sxs-lookup"><span data-stu-id="57694-120">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="57694-121">Til að búta til Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="57694-121">To create a Word template</span></span>
1. <span data-ttu-id="57694-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Word sniðmát** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="57694-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="57694-123">Fylgja skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="57694-123">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="57694-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="57694-124">See Also</span></span>
[<span data-ttu-id="57694-125">Stjórna útliti skýrslna og skjala</span><span class="sxs-lookup"><span data-stu-id="57694-125">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
