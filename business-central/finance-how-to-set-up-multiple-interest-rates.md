---
title: Hvernig á að setja upp marga vexti
description: Hægt er að reikna út vaxtareikninga með mörgum vöxtum fyrir tiltekið tímabil. Vaxtaútreikningar er svipaðir fyrir öll fjárhagsgjöld, með aðeins breytingum á vöxtum fyrir tiltekið tímabil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a38e286dab02dcb23acaba39a0d61b0b939bb20
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775426"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="0f4bf-104">Setja upp marga vexti</span><span class="sxs-lookup"><span data-stu-id="0f4bf-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="0f4bf-105">Margir vextir eru notaðir fyrir mismunandi tímabil vegna seinkunar á greiðslum fyrir viðskiptafærslur.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="0f4bf-106">Til dæmis tilgreinir ríkisstjórn hámarksvexti sem má leggja á neytendur.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="0f4bf-107">Vöxtum er hægt að breyta tvisvar á ári, 1. janúar og 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="0f4bf-108">Vextir á milli fyrirtækja eru samþykktir af báðum aðilum og engin takmörk eru fyrir þennan viðskiptavinaflokk.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="0f4bf-109">Tilkynntir vextir eru vanalega fjórum prósentum hærri en vextir venjulegra banka.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="0f4bf-110">Þegar vaxtaskilmálar og skilmálar innheimtubréfs er búið til, fyrir sekt vegna seinkunar á greiðslu, er hægt að tilgreina marga vexti þannig að sektargreiðsla er reiknuð út frá mismunandi vöxtum á mismunandi tímabilum.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="0f4bf-111">Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="0f4bf-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="0f4bf-112">Uppsetning á mörgum vöxtum</span><span class="sxs-lookup"><span data-stu-id="0f4bf-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="0f4bf-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtaskilmálar** eða Lánardrottinn og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0f4bf-114">Á síðunni **Vaxtaskilmálar** skal velja nauðsynlega skilmála og síðan velja aðgerðina **Vextir**.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="0f4bf-115">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="0f4bf-116">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="0f4bf-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="0f4bf-118">Á síðunni **Skilmálar innheimtubréfa** skal velja nauðsynlega skilmála innheimtubréfs og síðan velja aðgerðina **Stig**.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="0f4bf-119">Á síðunni **Stig innheimtubréfa** skal velja reitinn **Reikna út vexti**.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="0f4bf-120">Þegar gefið er út minnisblað vaxtareiknings, sýnir það vaxtagjöldin með mörgum vöxtum fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="0f4bf-121">Minnisblaðið inniheldur einnig samskiptaupplýsingar viðskiptavinar, fyrirtækið sem gefur út minnisblaðið og viðbótar- og heildarfjárhæðina.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="0f4bf-122">Upphafsfærsla minnisblaðsins birtist í feitletruðu.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="0f4bf-123">Vaxtagjöldin eru reiknuð með mörgum vöxtum á tilteknu tímabili og eru prentuð eftir upphafsfærslu minnisblaðsins.</span><span class="sxs-lookup"><span data-stu-id="0f4bf-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0f4bf-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0f4bf-124">See Also</span></span>  
[<span data-ttu-id="0f4bf-125">Innheimta útistandandi skuldir</span><span class="sxs-lookup"><span data-stu-id="0f4bf-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="0f4bf-126">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="0f4bf-126">Setting Up Finance</span></span>](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]