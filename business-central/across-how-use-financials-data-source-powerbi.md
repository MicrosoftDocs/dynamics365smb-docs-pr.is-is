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
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755242"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="38434-103">Notkun [!INCLUDE [prodlong](includes/prodlong.md)] sem Power BI gagnagjafa fyrir skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="38434-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="38434-104">Notandi getur gert [!INCLUDE[prodlong](includes/prodlong.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.</span><span class="sxs-lookup"><span data-stu-id="38434-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="38434-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power BI.</span><span class="sxs-lookup"><span data-stu-id="38434-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="38434-106">Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="38434-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span> <span data-ttu-id="38434-107">Frekari upplýsingar er að finna í [Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="38434-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="38434-108">Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38434-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="38434-109">Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.</span><span class="sxs-lookup"><span data-stu-id="38434-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="38434-110">Á síðunni **Ná í gögn** skal velja **Þjónusta á netinu**, velja **Microsoft Dynamics 365 Business Central** og síðan velja hnappinn **Tengjast**.</span><span class="sxs-lookup"><span data-stu-id="38434-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="38434-111">Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum tengingarferlið.</span><span class="sxs-lookup"><span data-stu-id="38434-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="38434-112">Þú verður beðin/n um að skrá þig inn í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="38434-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="38434-113">Veljið **Skrá inn** og svo reikninginn sem ætlunin er að skrá sig inn á.</span><span class="sxs-lookup"><span data-stu-id="38434-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="38434-114">Þetta ætti að vera sami reikningur og við innskráningu á [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="38434-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="38434-115">Veldu hnappinn **Tengjast** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="38434-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="38434-116">Leiðsagnarforrit Power BI sýnir lista yfir Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki og gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="38434-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="38434-117">Þessar gagnaveitur tákna allar vefþjónustur sem notandi hefur birt úr hverju fyrirtæki í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="38434-117">These data source represent all the web services that you have published from each company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. <span data-ttu-id="38434-119">Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE [prodshort](includes/prodshort.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.</span><span class="sxs-lookup"><span data-stu-id="38434-119">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="38434-120">Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.</span><span class="sxs-lookup"><span data-stu-id="38434-120">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="38434-121">Endurtaktu fyrri skref til að bæta við viðbótar [!INCLUDE [prodshort](includes/prodshort.md)] eða öðrum gögnum í Power BI gagnalíkanið þitt.</span><span class="sxs-lookup"><span data-stu-id="38434-121">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="38434-122">Þegar notandi hefur tengst [!INCLUDE [prodshort](includes/prodshort.md)] verður hann ekki beðinn aftur um skrá sig inn.</span><span class="sxs-lookup"><span data-stu-id="38434-122">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="38434-123">Þegar gögnum hefur verið hlaðið birtast þau á hægra yfirlitssvæði síðunnar.</span><span class="sxs-lookup"><span data-stu-id="38434-123">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="38434-124">Nú hefur notanda tekist að tengjast gögnum sínum í [!INCLUDE [prodshort](includes/prodshort.md)] og getur byrjað að byggja upp Power BI-skýrsluna sína.</span><span class="sxs-lookup"><span data-stu-id="38434-124">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="38434-125">Áður en þú býrð til skýrsluna mælum við með að þú flytjir inn [!INCLUDE [prodshort](includes/prodshort.md)] þemaskrána.</span><span class="sxs-lookup"><span data-stu-id="38434-125">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="38434-126">Þemaskráin mun búa til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og [!INCLUDE [prodshort](includes/prodshort.md)] forrit án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.</span><span class="sxs-lookup"><span data-stu-id="38434-126">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="38434-127">Frekari upplýsingar er að finna í [Power BI skráning](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="38434-127">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="38434-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="38434-128">See Also</span></span>

[<span data-ttu-id="38434-129">Gera viðskiptagögn þín virk fyrir Power BI</span><span class="sxs-lookup"><span data-stu-id="38434-129">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="38434-130">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="38434-130">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="38434-131">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="38434-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="38434-132">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="38434-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="38434-133">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="38434-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="38434-134">Fjármál</span><span class="sxs-lookup"><span data-stu-id="38434-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="38434-135">Stutt leiðbeining: Tengjast við gögn í Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38434-135">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
