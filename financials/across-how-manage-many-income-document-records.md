---
title: "Skilgreina hvaða skjöl á innleið skal skoða| Microsoft Docs"
description: "Stilla hvaða skjöl á innleið skuli birtast sjálfgefið, eins og t.d. rafrænir reikningar, til að bæta yfirsýn yfir færslur sem búið er að vinna og færslur sem á eftir að vinna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="0af6a-103">Vinna með margar færslur skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="0af6a-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="0af6a-104">Þegar þú býrð til eða vinnur færslur fyrir skjal á innleið, fjöldi lína í glugga  **skjal á innleið** vaxa að marki þar sem þú tapar yfirsýn.</span><span class="sxs-lookup"><span data-stu-id="0af6a-104">As you create or process incoming document records, the number of lines in the **Incoming Documents** window may grow to an extent where you lose overview.</span></span> <span data-ttu-id="0af6a-105">Þess vegna getur þú stillt færslur fyrir skjal á innleið sem unnið, til að fjarlægja þá úr sjálfgefna yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="0af6a-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="0af6a-106">Þegar valið er **Sýna Allt** aðgerð, geturðu skoðað bæði unnar og óunnar færslur.</span><span class="sxs-lookup"><span data-stu-id="0af6a-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0af6a-107">Ekki er hægt að breyta upplýsingum, hengja við skrár eða framkvæma aðra vinnslu á færslum fyrir skjöl á innleið sem eru stillt á unnið.</span><span class="sxs-lookup"><span data-stu-id="0af6a-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="0af6a-108">Fyrst þarf að stilla hana á óunnið.</span><span class="sxs-lookup"><span data-stu-id="0af6a-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="0af6a-109">**Úrvinnsla** gátreiturinn er sjálfkrafa valinn fyrir færslur fyrir skjal á innleið sem hafa verið unnar, en einnig er hægt að haka við eða afhaka gátreitinn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="0af6a-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="0af6a-110">Það fer eftir viðskiptaferli þínu, hvort færsla fyrir skjal á innleið geti verið unnið þegar tengt skjal hefur verið stofnað fyrir hana eða skrá hengd við.</span><span class="sxs-lookup"><span data-stu-id="0af6a-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0af6a-111">Þegar glugginn **Skjöl á innleið** er opnaður með **Mín skjöl á innleið** aðgerð í hlutverkamiðstöð, eru aðeins óunnar færslur fyrir skjöl á innleið sýndar sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="0af6a-111">When you open the **Incoming Documents** window with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="0af6a-112">Vísað er í þetta í þesssu efnisatriði sem "sjálfgefna yfirlitið".</span><span class="sxs-lookup"><span data-stu-id="0af6a-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="0af6a-113">Fjarlægja færslu skjals á innleið úr sjálfgefna yfirlitinu</span><span class="sxs-lookup"><span data-stu-id="0af6a-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="0af6a-114">Í **skjal á innleið** glugganum skal velja færslu eina eða fleiri línur fyrir færslur fyrir skjöl á innleið sem þú vilt fjarlægja úr sjálfgefna yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="0af6a-114">In the **Incoming Documents** window, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="0af6a-115">Valið er **stilla á unnið** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="0af6a-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="0af6a-116">Færslur fyrir skjal á innleið eru fjarlægðar úr sjálfgefna yfirlitinu, og gátreiturinn **unnið** er valinn á línunum.</span><span class="sxs-lookup"><span data-stu-id="0af6a-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0af6a-117">Einnig má framkvæma þessa aðgerð fyrir einstaka færslu í glugganum **Spjald fyrir skjöl á innleið** .</span><span class="sxs-lookup"><span data-stu-id="0af6a-117">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="0af6a-118">Skoða allar færslur fyrir skjöl á innleið.</span><span class="sxs-lookup"><span data-stu-id="0af6a-118">To view all incoming document records</span></span>
1. <span data-ttu-id="0af6a-119">Í glugganum **Skjal á innleið** skal velja aðgerðina **sýna allt**</span><span class="sxs-lookup"><span data-stu-id="0af6a-119">In the **Incoming Documents** window, choose the **Show All** action.</span></span>

<span data-ttu-id="0af6a-120">Allar færslur skjala á innleið eru birtar , þar á meðal þær þar sem **unnið** gátreiturinn er ekki valinn.</span><span class="sxs-lookup"><span data-stu-id="0af6a-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="0af6a-121">Bæta við færslu skjals á innleið við sjálfgefna yfirlitinu</span><span class="sxs-lookup"><span data-stu-id="0af6a-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="0af6a-122">Í glugganum **Skjal á innleið** skal velja aðgerðina **sýna allt**</span><span class="sxs-lookup"><span data-stu-id="0af6a-122">In the **Incoming Documents** window, choose the **Show All** action.</span></span>
2. <span data-ttu-id="0af6a-123">velja færslu eina eða fleiri línur fyrir færslur fyrir skjöl á innleið sem þú vilt að birtist í sjálfgefna yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="0af6a-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="0af6a-124">Valið er **Setja upp óunnið** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="0af6a-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="0af6a-125">Einnig má framkvæma þessa aðgerð fyrir einstaka færslu í glugganum **Spjald fyrir skjöl á innleið** .</span><span class="sxs-lookup"><span data-stu-id="0af6a-125">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="0af6a-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0af6a-126">See Also</span></span>
[<span data-ttu-id="0af6a-127">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="0af6a-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="0af6a-128">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="0af6a-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="0af6a-129">Innkaup</span><span class="sxs-lookup"><span data-stu-id="0af6a-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0af6a-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0af6a-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

