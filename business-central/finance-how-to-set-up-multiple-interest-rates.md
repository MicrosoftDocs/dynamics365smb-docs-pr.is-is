---
title: "Hvernig á að setja upp marga vexti"
description: "Hægt er að reikna út vaxtareikninga með mörgum vöxtum fyrir tiltekið tímabil. Vaxtaútreikningar er svipaðir fyrir öll fjárhagsgjöld, með aðeins breytingum á vöxtum fyrir tiltekið tímabil."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3d4c111af62db5858b81b76f9f51a9093c01e5e6
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="c1b2d-104">Setja upp marga vexti</span><span class="sxs-lookup"><span data-stu-id="c1b2d-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="c1b2d-105">Margir vextir eru notaðir fyrir mismunandi tímabil vegna seinkunar á greiðslum fyrir viðskiptafærslur.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="c1b2d-106">Til dæmis tilgreinir ríkisstjórn hámarksvexti sem má leggja á neytendur.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="c1b2d-107">Vöxtum er hægt að breyta tvisvar á ári, 1. janúar og 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="c1b2d-108">Vextir á milli fyrirtækja eru samþykktir af báðum aðilum og engin takmörk eru fyrir þennan viðskiptavinaflokk.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="c1b2d-109">Tilkynntir vextir eru vanalega fjórum prósentum hærri en vextir venjulegra banka.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="c1b2d-110">Þegar vaxtaskilmálar og skilmálar innheimtubréfs er búið til, fyrir sekt vegna seinkunar á greiðslu, er hægt að tilgreina marga vexti þannig að sektargreiðsla er reiknuð út frá mismunandi vöxtum á mismunandi tímabilum.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="c1b2d-111">Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="c1b2d-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="c1b2d-112">Uppsetning á mörgum vöxtum</span><span class="sxs-lookup"><span data-stu-id="c1b2d-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="c1b2d-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtaskilmálar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c1b2d-114">Í glugganum **Vaxtaskilmálar** skal velja nauðsynlega skilmála og síðan velja aðgerðina **Vextir**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-114">In the **Finance Charge Terms** window, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="c1b2d-115">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="c1b2d-116">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="c1b2d-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="c1b2d-118">Í glugganum **Skilmálar innheimtubréfa** skal velja nauðsynlega skilmála innheimtubréfs og síðan velja aðgerðina **Stig**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-118">In the **Reminder Terms** window, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="c1b2d-119">Í glugganum **Stig innheimtubréfa** skal velja reitinn **Reikna út vexti**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-119">In the **Reminder Levels** window, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="c1b2d-120">Þegar gefið er út minnisblað vaxtareiknings, sýnir það vaxtagjöldin með mörgum vöxtum fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="c1b2d-121">Minnisblaðið inniheldur einnig samskiptaupplýsingar viðskiptavinar, fyrirtækið sem gefur út minnisblaðið og viðbótar- og heildarfjárhæðina.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="c1b2d-122">Upphafsfærsla minnisblaðsins birtist í feitletruðu.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="c1b2d-123">Vaxtagjöldin eru reiknuð með mörgum vöxtum á tilteknu tímabili og eru prentuð eftir upphafsfærslu minnisblaðsins.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c1b2d-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c1b2d-124">See Also</span></span>  
[<span data-ttu-id="c1b2d-125">Innheimta útistandandi skuldir</span><span class="sxs-lookup"><span data-stu-id="c1b2d-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="c1b2d-126">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="c1b2d-126">Setting Up Finance</span></span>](finance-setup-finance.md)

