---
title: "Leita að skjölum án viðhengja| Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 34bbc67c0f2bcc5afe408e75a7d3ceb582160d87
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="a89d6-102">Finna bókuð fylgiskjöl án færslu skjals á innleið</span><span class="sxs-lookup"><span data-stu-id="a89d6-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="a89d6-103">Á síðunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa- og söluskjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám.</span><span class="sxs-lookup"><span data-stu-id="a89d6-103">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="a89d6-104">Hvernig á að finna bókuð fylgiskjöl án færslu skjals á innleið</span><span class="sxs-lookup"><span data-stu-id="a89d6-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="a89d6-105">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókhaldslykill** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a89d6-105">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="a89d6-106">Veljið línu fyrir þann fjárhagsreikning þar sem skoða á fjárhagsfærslur og bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið og veljið síðan **bókuð skjöl án skjal á innleið**</span><span class="sxs-lookup"><span data-stu-id="a89d6-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="a89d6-107">Einnig, Valið er **fjárhagsfærslur** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="a89d6-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="a89d6-108">Á síðunni **fjárhagsfærslur**, veljið aðgerðina **bókuð skjöl án skjala á innleið**.</span><span class="sxs-lookup"><span data-stu-id="a89d6-108">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="a89d6-109">Síðan **Bókuð fylgiskjöl án skjals á innleið** opnast og hún sýnir bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið sem tengjast fjárhagsfærslum á fjárhagsreikningi sem síðan var opnuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="a89d6-109">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="a89d6-110">Síðan getur birt mest 1000 línur í einu.</span><span class="sxs-lookup"><span data-stu-id="a89d6-110">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="a89d6-111">Sjálfgefið inniheldur reiturinn **dagsetningarafmörkun** því síu sem takmarkar línurnar við færslur með bókunardagsetningum frá upphafi bókhaldstímabils til vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="a89d6-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="a89d6-112">Til að tengja fundin skjöl við fyrirliggjandi færslur skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="a89d6-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="a89d6-113">Á síðunni **Bókuð fylgiskjöl án skjals á innleið** skal velja línu fyrir bókað skjal sem á að tengja við fyrirliggjandi færslu skjals á innleið, og veljið svo aðgerðina velja **skjal á innleið**.</span><span class="sxs-lookup"><span data-stu-id="a89d6-113">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="a89d6-114">Á síðunni **Skjöl á innleið** skal velja færslu fyrir skjal á innleið sem tengja á við bókað skjal sem fannst og velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a89d6-114">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="a89d6-115">Á síðunni **Bókuð fylgiskjöl án skjals á innleið** er valin færsla skjals á innleið nú tengt við bókaða skjalið, eins og sjá má í upplýsingakassanum **skrár fyrir skjal á innleið**.</span><span class="sxs-lookup"><span data-stu-id="a89d6-115">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="a89d6-116">Ef viðkomandi færsla skjals á innleið er ekki til á síðunni **skjal á innleið** er hægt að stofna hana.</span><span class="sxs-lookup"><span data-stu-id="a89d6-116">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="a89d6-117">Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="a89d6-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a89d6-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a89d6-118">See Also</span></span>
[<span data-ttu-id="a89d6-119">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="a89d6-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="a89d6-120">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="a89d6-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="a89d6-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="a89d6-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a89d6-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a89d6-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

