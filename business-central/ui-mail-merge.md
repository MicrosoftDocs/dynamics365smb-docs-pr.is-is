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
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110955"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="d7551-103">Word-sniðmát notuð fyrir mörg samskipti í einu</span><span class="sxs-lookup"><span data-stu-id="d7551-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="d7551-104">Microsoft Word-sniðmát geta auðveldað mörg samskipti í einu með einingum á borð við viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="d7551-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="d7551-105">Til dæmis er hægt að búa til bæklinga til að tilkynna viðskiptavinum um söluherferð, bréf til að tilkynna lánardrottnum um nýja innkaupastefnu eða boð til að fá tengiliði til að mæta á væntanlegan viðburð.</span><span class="sxs-lookup"><span data-stu-id="d7551-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

> [!NOTE]
> <span data-ttu-id="d7551-106">Þú getur eingöngu notað Word-sniðmát á tækjum með Microsoft Word 2019 og Windows-stýrikerfinu uppsettu.</span><span class="sxs-lookup"><span data-stu-id="d7551-106">You can use Word templates only on devices with Microsoft Word 2019 and the Windows operating system installed.</span></span>

<span data-ttu-id="d7551-107">Hægt er að nota einingar í [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa sniðmátsins og bæta við innfellingarsvæðum til að sérsníða skjöl fyrir hverja einingu.</span><span class="sxs-lookup"><span data-stu-id="d7551-107">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="d7551-108">Innfellingarsvæðin koma úr einingunni í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7551-108">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d7551-109">Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið.</span><span class="sxs-lookup"><span data-stu-id="d7551-109">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="d7551-110">Á síðunni **Word-sniðmát** er hægt að nota uppsetningarleiðbeiningu með hjálp til að sækja Zip-skrá sem inniheldur DataSource.txt og Word-sniðmátsskrá fyrir einingu.</span><span class="sxs-lookup"><span data-stu-id="d7551-110">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="d7551-111">Þegar búið er að setja upp sniðmátið og bæta við innfellingarsvæðum er sama leiðbeiningin notuð til að hlaða upp sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="d7551-111">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="d7551-112">Aðeins er hægt að nota Word-sniðmátið og skrár gagnagjafans sem sótt er af [!INCLUDE[prod_short](includes/prod_short.md)] og vista verður skrárnar í sömu staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="d7551-112">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="d7551-113">Þegar eining er valin þar sem á að stofna sniðmát, sýnir listinn allar einingar í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7551-113">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d7551-114">Hins vegar er ekki hægt að stofna sniðmát fyrir allar einingar.</span><span class="sxs-lookup"><span data-stu-id="d7551-114">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="d7551-115">Ef heiti einingar inniheldur sérstafi á borð við **/**, **.**, **_** eða **-** er ekki hægt að stofna sniðmát fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="d7551-115">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="d7551-116">Heiti einingarinnar er sýnt í dálknum **Yfirskrift hlutar**.</span><span class="sxs-lookup"><span data-stu-id="d7551-116">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="d7551-117">Þegar sniðmátið er sett upp í Word er hægt í flipanum **Sendingar** að bæta við innfellingarsvæðum með því að velja **Setja inn innfellingarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="d7551-117">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="d7551-118">Ekki er hægt að nota innfellingarsvæði ef heiti reitsins inniheldur 40 stafi eða fleiri.</span><span class="sxs-lookup"><span data-stu-id="d7551-118">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="d7551-119">Til dæmis er ekki hægt að nota reitinn Company__Information_Customs_Permit_Date vegna þess að hann er með 40 stafi.</span><span class="sxs-lookup"><span data-stu-id="d7551-119">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="d7551-120">Þegar Word-sniðmátið er tilbúið er hægt á síðunni **Word-sniðmát** að velja **Nota** til að búa til skjölin.</span><span class="sxs-lookup"><span data-stu-id="d7551-120">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="d7551-121">Annaðhvort er hægt að búa til eitt skjal sem inniheldur hluta fyrir hverja einingu eða skipta aðgerðinni til að búa til nýtt skjal fyrir hverja einingu.</span><span class="sxs-lookup"><span data-stu-id="d7551-121">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="d7551-122">Til að búta til Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="d7551-122">To create a Word template</span></span>
1. <span data-ttu-id="d7551-123">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Word sniðmát** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d7551-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="d7551-124">Fylgja skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="d7551-124">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="d7551-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d7551-125">See Also</span></span>
[<span data-ttu-id="d7551-126">Stjórna útliti skýrslna og skjala</span><span class="sxs-lookup"><span data-stu-id="d7551-126">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
