---
title: Nota Business Central í Power BI-skýrslum | Microsoft Docs
description: Notandi getur gert gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528463"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="1df19-103">Notkun [!INCLUDE[prodlong](includes/prodlong.md)] sem Power BI gagnagjafa fyrir skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="1df19-103">Using [!INCLUDE[prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="1df19-104">Notandi getur gert [!INCLUDE[prodlong](includes/prodlong.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.</span><span class="sxs-lookup"><span data-stu-id="1df19-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="1df19-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power BI.</span><span class="sxs-lookup"><span data-stu-id="1df19-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="1df19-106">Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="1df19-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="1df19-107">Frekari upplýsingar er að finna í [Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="1df19-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="1df19-108">Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1df19-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="1df19-109">Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.</span><span class="sxs-lookup"><span data-stu-id="1df19-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="1df19-110">Á síðunni **Ná í gögn** skal velja **Þjónusta á netinu**, velja **Microsoft Dynamics 365 Business Central** og síðan velja hnappinn **Tengjast**.</span><span class="sxs-lookup"><span data-stu-id="1df19-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="1df19-111">Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum tengingarferlið, þ.á.m. innskráningu í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1df19-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="1df19-112">Velja skal **Innskráning** og síðan viðeigandi reikning.</span><span class="sxs-lookup"><span data-stu-id="1df19-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="1df19-113">Notaðu sama reikning og þú skráir þig inn í [!INCLUDE[prodshort](includes/prodshort.md)] með.</span><span class="sxs-lookup"><span data-stu-id="1df19-113">Use the same account that you sign into [!INCLUDE[prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="1df19-114">Veldu hnappinn **Tengjast** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="1df19-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="1df19-115">Power BI leiðsagnarforritið sýnir lista yfir Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] umhverfi, fyrirtæki og gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="1df19-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="1df19-116">Þessar gagnaveitur tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1df19-116">These data sources represent all the web services that you have published from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="1df19-117">Einnig er hægt að búa til vefslóð vefþjónustu í [!INCLUDE[prodshort](includes/prodshort.md)] í staðinn.</span><span class="sxs-lookup"><span data-stu-id="1df19-117">You can also create a new web service URL in [!INCLUDE[prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="1df19-118">Veljið eina af eftirfarandi leiðum:</span><span class="sxs-lookup"><span data-stu-id="1df19-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="1df19-119">Nota aðgerðina **Búa til gagnasafn** á síðunni **Vefþjónusta**</span><span class="sxs-lookup"><span data-stu-id="1df19-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="1df19-120">Nota uppsetningarleiðbeiningar **Setja upp skýrslugerð** með hjálp</span><span class="sxs-lookup"><span data-stu-id="1df19-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="1df19-121">Velja aðgerðina **Breyta í Excel** í hvaða lista sem er</span><span class="sxs-lookup"><span data-stu-id="1df19-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="1df19-122">Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.</span><span class="sxs-lookup"><span data-stu-id="1df19-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="1df19-123">Endurtaktu fyrri skref til að bæta við viðbótar [!INCLUDE[prodshort](includes/prodshort.md)] eða öðrum gögnum í Power BI gagnalíkanið þitt.</span><span class="sxs-lookup"><span data-stu-id="1df19-123">Repeat the previous steps to add additional [!INCLUDE[prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="1df19-124">Þegar notandi hefur tengst [!INCLUDE[prodshort](includes/prodshort.md)] verður hann ekki beðinn aftur um skrá sig inn.</span><span class="sxs-lookup"><span data-stu-id="1df19-124">Once you have successfully connected to [!INCLUDE[prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="1df19-125">Þegar gögnum hefur verið hlaðið er hægt að sjá þau á hægra yfirlitssvæði síðunnar.</span><span class="sxs-lookup"><span data-stu-id="1df19-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="1df19-126">Notanda tókst að tengjast gögnum sínum í [!INCLUDE[prodshort](includes/prodshort.md)] og getur byrjað að byggja upp Power BI-skýrsluna sína.</span><span class="sxs-lookup"><span data-stu-id="1df19-126">You have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="1df19-127">Áður en þú býrð til skýrsluna mælum við með að þú flytjir inn [!INCLUDE[prodshort](includes/prodshort.md)] þemaskrána.</span><span class="sxs-lookup"><span data-stu-id="1df19-127">Before building your report, we recommend that you import the [!INCLUDE[prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="1df19-128">Þemaskráin mun búa til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og [!INCLUDE[prodshort](includes/prodshort.md)] forrit án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.</span><span class="sxs-lookup"><span data-stu-id="1df19-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE[prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="1df19-129">Frekari upplýsingar er að finna í [Power BI skráning](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="1df19-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="1df19-130">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="1df19-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="1df19-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1df19-131">See Also</span></span>

[<span data-ttu-id="1df19-132">Gera viðskiptagögn þín virk fyrir Power BI</span><span class="sxs-lookup"><span data-stu-id="1df19-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="1df19-133">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="1df19-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="1df19-134">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="1df19-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="1df19-135">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="1df19-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="1df19-136">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="1df19-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="1df19-137">Fjármál</span><span class="sxs-lookup"><span data-stu-id="1df19-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="1df19-138">Stutt leiðbeining: Tengjast við gögn í Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1df19-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
