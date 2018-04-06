---
title: "Leita að skjölum án viðhengja| Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c355657821f5f4d18c707d296d9607cf5ec60442
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="23307-102">Finna bókuð fylgiskjöl án færslu skjals á innleið</span><span class="sxs-lookup"><span data-stu-id="23307-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="23307-103">Úr gluggunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa- og söluskjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám.</span><span class="sxs-lookup"><span data-stu-id="23307-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="23307-104">Hvernig á að finna bókuð fylgiskjöl án færslu skjals á innleið</span><span class="sxs-lookup"><span data-stu-id="23307-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="23307-105">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="23307-105">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="23307-106">Veljið línu fyrir þann fjárhagsreikning þar sem skoða á fjárhagsfærslur og bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið og veljið síðan **bókuð skjöl án skjal á innleið**</span><span class="sxs-lookup"><span data-stu-id="23307-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="23307-107">Einnig, Valið er **fjárhagsfærslur** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="23307-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="23307-108">Í glugganum **fjárhagsfærslur**, veljið aðgerðina **bókuð skjöl án skjala á innleið**.</span><span class="sxs-lookup"><span data-stu-id="23307-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="23307-109">Glugginn **Bókuð fylgiskjöl án skjals á innleið** opnast og hann sýnir bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið sem tengjast fjárhagsfærslum á fjárhagsreikningi sem gluggninn var opnaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="23307-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="23307-110">Glugginn getur birt mest 1000 línur í einu.</span><span class="sxs-lookup"><span data-stu-id="23307-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="23307-111">Sjálfgefið inniheldur reiturinn **dagsetningarafmörkun** því síu sem takmarkar línurnar við færslur með bókunardagsetningum frá upphafi bókhaldstímabils til vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="23307-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="23307-112">Til að tengja fundin skjöl við fyrirliggjandi færslur skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="23307-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="23307-113">Í glugganum **Bókuð fylgiskjöl án skjals á innleið** skal velja línu fyrir bókað skjal sem á að tengja við fyrirliggjandi færslu skjals á innleið, og veljið svo aðgerðina velja **skjal á innleið**.</span><span class="sxs-lookup"><span data-stu-id="23307-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="23307-114">Í **skjal á innleið** glugganum skal velja færslu fyrir skjal á innleið sem tengja á við bókað skjal sem fannst og velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="23307-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="23307-115">Í glugganum **Bókuð fylgiskjöl án skjals á innleið** er valin færsla skjals á innleið nú tengt við bókaða skjalið, eins og sjá má í upplýsingakassanum **skrár fyrir skjal á innleið**.</span><span class="sxs-lookup"><span data-stu-id="23307-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="23307-116">Ef viðkomandi færsla skjals á innleið er ekki til í glugganum **skjal á innleið** er hægt að stofna hana.</span><span class="sxs-lookup"><span data-stu-id="23307-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="23307-117">Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="23307-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="23307-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="23307-118">See Also</span></span>
[<span data-ttu-id="23307-119">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="23307-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="23307-120">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="23307-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="23307-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="23307-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="23307-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="23307-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

