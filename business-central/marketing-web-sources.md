---
title: "Setja upp veftengingar fyrir tengiliðafyrirtæki| Microsoft Docs"
description: "Hægt er að skilgreina internet eða veftengingar og úthluta þeim til tengiliðafyrirtækja til að auðvelda þér að ákveða hvernig þú vilt leita að upplýsingum um tengiliði þína."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b8c59f24eae07efe8f2c4ca1e4e22d05fd4f1b1c
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="98348-103">Setja upp veftengingar fyrir tengiliðafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="98348-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="98348-104">Hægt er að nota veftengingar með tengiliðafyrirtækjum til að þekkja t.d. leitarvélar og vefsvæði á netinu sem óskað er eftir að nota til að leita að upplýsingum um tengiliðina.</span><span class="sxs-lookup"><span data-stu-id="98348-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="98348-105">Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="98348-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="98348-106">Notkun veftenginga á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="98348-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="98348-107">Fyrst að skilgreina veftengingakóðann.</span><span class="sxs-lookup"><span data-stu-id="98348-107">First, you define the web source code.</span></span> <span data-ttu-id="98348-108">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hverja veftengingu.</span><span class="sxs-lookup"><span data-stu-id="98348-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="98348-109">Þegar kominn er veftengingakóði er hægt að byrja að úthluta kóðanum til tengiliða.</span><span class="sxs-lookup"><span data-stu-id="98348-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="98348-110">Skilgreina veftengingarkóða</span><span class="sxs-lookup"><span data-stu-id="98348-110">To define a web source code</span></span>
1. <span data-ttu-id="98348-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **veftengingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="98348-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="98348-112">Veljið aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="98348-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="98348-113">Fyllt er í reitina **Kóti**, **Lýsing** og **URL**.</span><span class="sxs-lookup"><span data-stu-id="98348-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="98348-114">Sláið inn %1 í reitinn **URL** til að setja inn staðgengil fyrir leitarorð í slóðinni.</span><span class="sxs-lookup"><span data-stu-id="98348-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="98348-115">Þegar veftengingin er ræst frá tengilið er %1 skipt út fyrir leitarorð, t.d. heiti fyrirtækisins sem fært var inn í gluggann **Veftenging tengiliðar**.</span><span class="sxs-lookup"><span data-stu-id="98348-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="98348-116">Skrefin eru endurtekin til að setja upp eins margar veftengingar og óskað er.</span><span class="sxs-lookup"><span data-stu-id="98348-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="98348-117">Úthluta veftengingum á tengiliðarfyrirtæki</span><span class="sxs-lookup"><span data-stu-id="98348-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="98348-118">Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="98348-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="98348-119">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="98348-119">Open the contact.</span></span>
2. <span data-ttu-id="98348-120">Veljið aðgerðina **Fyrirtæki** og veljið síðan aðgerðina **Veftenging**.</span><span class="sxs-lookup"><span data-stu-id="98348-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="98348-121">Glugginn **Veftenglar tengiliða** birtist.</span><span class="sxs-lookup"><span data-stu-id="98348-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="98348-122">Í reitnum **Veftengingarkóði** skal velja veftenginguna sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="98348-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="98348-123">Í reitinn **Leitarorð** er fært inn leitarorðið sem á að nota til að finna upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="98348-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="98348-124">Skrefin eru endurtekin til að úthluta eins mörgum veftengingum og óskað er.</span><span class="sxs-lookup"><span data-stu-id="98348-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="98348-125">Einnig má nota sömu aðferð til að úthluta veftengingum í glugganum **Tengiliðalisti**.</span><span class="sxs-lookup"><span data-stu-id="98348-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="98348-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="98348-126">See Also</span></span>
[<span data-ttu-id="98348-127">Fyrirtækjatengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="98348-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="98348-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98348-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

