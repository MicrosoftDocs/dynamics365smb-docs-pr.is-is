---
title: Yfirlit bókunarlínu færslubókar | Microsoft Docs
description: Þetta efnisatriði fjallar um breytingar á Kóðaeining 12, **Bókunarlína fjárhags**, sem er helsti forritahluti bókana í fjárhag og er eini staðurinn þar sem færslur í fjárhag, VSK, viðskiptamenn og lánardrottna eru settar inn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215254"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="96031-103">Yfirlit bókunarlínu færslubókar</span><span class="sxs-lookup"><span data-stu-id="96031-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="96031-104">Kóðaeining 12, **Bókunarlína fjárhags**, er helsti forritahluti bókana í fjárhag og er eini staðurinn þar sem færslur í fjárhag, VSK, viðskiptamenn og lánardrottna eru settar inn.</span><span class="sxs-lookup"><span data-stu-id="96031-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="96031-105">Kóðaeiningin er einnig notuð fyrir allar aðgerðir Jafna, Ógilda og Reverse.</span><span class="sxs-lookup"><span data-stu-id="96031-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="96031-106">Í Microsoft Dynamics NAV 2013 R2 var kóðaeiningin endurhönnuð þar sem hún var orðin mjög stór, með u.þ.b. 7.600 kóðalínum.</span><span class="sxs-lookup"><span data-stu-id="96031-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="96031-107">Í þessari útgáfu hefur arkitektúrnum verið breytt og kóðaeiningin hefur verið gerð einfaldari og auðveldara er að viðhalda henni.</span><span class="sxs-lookup"><span data-stu-id="96031-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="96031-108">Í þessu eru breytingum lýst og upplýsingar fyrir skilyrði uppfærslu gefnar.</span><span class="sxs-lookup"><span data-stu-id="96031-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="96031-109">Eldri arkitektúr</span><span class="sxs-lookup"><span data-stu-id="96031-109">Old Architecture</span></span>  
<span data-ttu-id="96031-110">Eldri arkitektúr var með eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="96031-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="96031-111">Mikið var um notkun alþjóðlegra breyta, sem jók möguleikann á földum villum vegna notkun breyta með röngu umfangi.</span><span class="sxs-lookup"><span data-stu-id="96031-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="96031-112">Það voru mörg löng ferli (með yfir 100 kóðalínum) sem voru einnig með flóknum mælingum (þ.e. mörgum CASE, REPEAT, IF földum segðum) sem gerðu það erfitt að lesa og viðhalda kóða.</span><span class="sxs-lookup"><span data-stu-id="96031-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="96031-113">Nokkur ferli sem voru aðeins notuð staðbundið og var aðeins ætla að vera notað staðbundið voru ekki merkt sem staðbundin.</span><span class="sxs-lookup"><span data-stu-id="96031-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="96031-114">Flest ferli höfðu engar færibreytur og notuðu altækar breytur.</span><span class="sxs-lookup"><span data-stu-id="96031-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="96031-115">Sumir notuðu færibreytur og yfirskrifuð altækar breytur með staðbundnum.</span><span class="sxs-lookup"><span data-stu-id="96031-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="96031-116">Kóðamynstur fyrir leit í fjárhagsreikningi og stofnun fjárhags og VSK færslna var ekki staðlað og breytilegt frá stað til staðs.</span><span class="sxs-lookup"><span data-stu-id="96031-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="96031-117">Að auki var mikið um endurtekinn kóða og ósamhverfu milli kóða viðskiptamanna og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="96031-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="96031-118">Stór hluti kóðans í kóðaeiningu 12, um 30 prósent, tengdur greiðsluafslætti og útreikningi á vikmörkum, þó svo þessir eiginleikar séu ekki nauðsynlegar í mörgum löndum eða svæðum.</span><span class="sxs-lookup"><span data-stu-id="96031-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="96031-119">Bókun, jöfnun, ógilda, Reverse, greiðsluafsláttur og vikmörk og gengisleiðréttingar voru sameinaðar í kóðaeiningu 12 með löngum lista altækra breyta.</span><span class="sxs-lookup"><span data-stu-id="96031-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="96031-120">Nýr arkitektúr</span><span class="sxs-lookup"><span data-stu-id="96031-120">New Architecture</span></span>  
<span data-ttu-id="96031-121">Í [!INCLUDE[prod_short](includes/prod_short.md)], hafa eftirfarandi bætur verið gerðar á kóðaeiningu 12:</span><span class="sxs-lookup"><span data-stu-id="96031-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="96031-122">Kóðaeining 12 hefur verið endurbætt í smærri ferli (allir innan við 100 kóðalínur).</span><span class="sxs-lookup"><span data-stu-id="96031-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="96031-123">Staðlað mynstur fyrir leit fjárhagsreiknings sem hefur verið sett inn með hjálparaðgerð úr bókunarflokkstöflum.</span><span class="sxs-lookup"><span data-stu-id="96031-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="96031-124">Bókunarvélarrammi hefur verið settur inn til að stjórna upphafi og lokum færslna og einangra stofnun í fjárhag og VSK-færslur, söfnun VSK-leiðréttingum og útreikningi viðbótarupphæðum gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="96031-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="96031-125">Kóðatvíverknaður hefur verið útilokaður.</span><span class="sxs-lookup"><span data-stu-id="96031-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="96031-126">Margir hjálparvalkostir hafa verið fluttir í viðkomandi töflur viðskiptamanna- og lánardrottnafærsla.</span><span class="sxs-lookup"><span data-stu-id="96031-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="96031-127">Notkun alþjóðlegra breyta hefur verið lágmörkuð þannig að hvert ferli noti breytur og eigin rökbreytum.</span><span class="sxs-lookup"><span data-stu-id="96031-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96031-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="96031-128">See Also</span></span>

[<span data-ttu-id="96031-129">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="96031-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="96031-130">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="96031-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="96031-131">Hönnunarupplýsingar: Bókunarlína færslubókar (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="96031-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]