---
title: "Yfirlit bókunarlínu færslubókar | Microsoft Docs"
description: "Þetta efnisatriði fjallar um breytingar á Kóðaeining 12, **Bókunarlína fjárhags**, sem er helsti forritahluti bókana í fjárhag og er eini staðurinn þar sem færslur í fjárhag, VSK, viðskiptamenn og lánardrottna eru settar inn."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 77fa52505dc586dc11ca89e53f6eec75042d3606
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="9ffbc-103">Yfirlit bókunarlínu færslubókar</span><span class="sxs-lookup"><span data-stu-id="9ffbc-103">General Journal Post Line Overview</span></span>
<span data-ttu-id="9ffbc-104">Kóðaeining 12, **Bókunarlína fjárhags**, er helsti forritahluti bókana í fjárhag og er eini staðurinn þar sem færslur í fjárhag, VSK, viðskiptamenn og lánardrottna eru settar inn.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="9ffbc-105">Kóðaeiningin er einnig notuð fyrir allar aðgerðir Jafna, Ógilda og Reverse.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="9ffbc-106">Þrátt fyrir að kóðaeiningin hafi verið endurbætt í hverri útgáfu síðustu tíu ár var arkitektúr hennar nákvæmlega sá sami.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-106">While the codeunit has been improved in each release over the last ten years, its architecture remained essentially unchanged.</span></span> <span data-ttu-id="9ffbc-107">Kóðaeiningin varð mjög stór, með u.þ.b. 7.600 kóðalínum.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-107">The codeunit became very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="9ffbc-108">Í þessari útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] er arkitektúrnum breytt og kóðaeiningin hefur verið gerð einfaldari og auðveldara er að viðhalda henni.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-108">With this release of [!INCLUDE[d365fin](includes/d365fin_md.md)], the architecture is changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="9ffbc-109">Í þessu eru breytingar tilteknar og upplýsingar fyrir skilyrði uppfærslu gefnar.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-109">This documentation introduces the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="9ffbc-110">Eldri arkitektúr</span><span class="sxs-lookup"><span data-stu-id="9ffbc-110">Old Architecture</span></span>  
<span data-ttu-id="9ffbc-111">Eldri arkitektúr var með eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="9ffbc-111">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="9ffbc-112">Mikið var um notkun alþjóðlegra breyta, sem jók möguleikann á földum villum vegna notkun breyta með röngu umfangi.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-112">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="9ffbc-113">Það voru mörg löng ferli (með yfir 100 kóðalínum) sem voru einnig með flóknum mælingum (þ.e. mörgum CASE, REPEAT, IF földum segðum) sem gerðu það erfitt að lesa og viðhalda kóða.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-113">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="9ffbc-114">Nokkur ferli sem voru aðeins notuð staðbundið og var aðeins ætla að vera notað staðbundið voru ekki merkt sem staðbundin.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-114">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="9ffbc-115">Flest ferli höfðu engar færibreytur og notuðu altækar breytur.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-115">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="9ffbc-116">Sumir notuðu færibreytur og yfirskrifuð altækar breytur með staðbundnum.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-116">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="9ffbc-117">Kóðamynstur fyrir leit í fjárhagsreikningi og stofnun fjárhags og VSK færslna var ekki staðlað og breytilegt frá stað til staðs.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-117">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="9ffbc-118">Að auki var mikið um endurtekinn kóða og ósamhverfu milli kóða viðskiptamanna og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-118">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="9ffbc-119">Stór hluti kóðans í kóðaeiningu 12, um 30 prósent, tengdur greiðsluafslætti og útreikningi á vikmörkum, þó svo þessir eiginleikar séu ekki nauðsynlegar í mörgum löndum eða svæðum.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-119">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="9ffbc-120">Bókun, jöfnun, ógilda, Reverse, greiðsluafsláttur og vikmörk og gengisleiðréttingar voru sameinaðar í kóðaeiningu 12 með löngum lista altækra breyta.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-120">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="9ffbc-121">Nýr arkitektúr</span><span class="sxs-lookup"><span data-stu-id="9ffbc-121">New Architecture</span></span>  
<span data-ttu-id="9ffbc-122">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], hafa eftirfarandi bætur verið gerðar á kóðaeiningu 12:</span><span class="sxs-lookup"><span data-stu-id="9ffbc-122">In [!INCLUDE[d365fin](includes/d365fin_md.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="9ffbc-123">Kóðaeining 12 hefur verið endurbætt í smærri ferli (allir innan við 100 kóðalínur).</span><span class="sxs-lookup"><span data-stu-id="9ffbc-123">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="9ffbc-124">Staðlað mynstur fyrir leit fjárhagsreiknings sem hefur verið sett inn með hjálparaðgerð úr bókunarflokkstöflum.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-124">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="9ffbc-125">Bókunarvélarrammi hefur verið settur inn til að stjórna upphafi og lokum færslna og einangra stofnun í fjárhag og VSK-færslur, söfnun VSK-leiðréttingum og útreikningi viðbótarupphæðum gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-125">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="9ffbc-126">Kóðatvíverknaður hefur verið útilokaður.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-126">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="9ffbc-127">Margir hjálparvalkostir hafa verið fluttir í viðkomandi töflur viðskiptamanna- og lánardrottnafærsla.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-127">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="9ffbc-128">Notkun alþjóðlegra breyta hefur verið lágmörkuð þannig að hvert ferli noti breytur og eigin rökbreytum.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-128">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ffbc-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9ffbc-129">See Also</span></span>  
<span data-ttu-id="9ffbc-130">[Hönnunarupplýsingar: Uppbygging bókunarviðmóts](design-details-posting-interface-structure.md) </span><span class="sxs-lookup"><span data-stu-id="9ffbc-130">[Design Details: Posting Interface Structure](design-details-posting-interface-structure.md) </span></span>  
[<span data-ttu-id="9ffbc-131">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="9ffbc-131">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

