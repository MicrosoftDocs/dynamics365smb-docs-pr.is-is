---
title: Úrræðaleita fyrirtækjamiðstöðina
description: Kynnið ykkur hvernig hægt er að leysa vandamál þegar fyrirtækjamiðstöðin er notuð í Dynamics 365 Business Central til að stjórna vinnu í mörgum fyrirtækjum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 94bd2c0270263a1382094e559b4e70753f9bb91f
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013583"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="bbdf5-103">Úrræðaleita fyrirtækjamiðstöðina</span><span class="sxs-lookup"><span data-stu-id="bbdf5-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="bbdf5-104">Það er auðvelt að bæta fyrirtækjum við stjórnborð fyrirtækjamiðstöðvarinnar, en þessi grein fjallar um vandamál sem kunna að koma upp.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="bbdf5-105">Leita að villum</span><span class="sxs-lookup"><span data-stu-id="bbdf5-105">Check errors</span></span>

<span data-ttu-id="bbdf5-106">Notið aðgerðina **Villuleit** til að skoða lista yfir nýlegar villur.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="bbdf5-107">Hægt er að sjá frekari upplýsingar fyrir hverja villu og hægt er að hreinsa kladdann með því að eyða eldri færslum.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="bbdf5-108">Tenging mistókst</span><span class="sxs-lookup"><span data-stu-id="bbdf5-108">Connection failed</span></span>

<span data-ttu-id="bbdf5-109">Það geta verið nokkrar ástæður fyrir því af hverju ekki er hægt að tengjast fyrirtæki, þ.m.t. eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="bbdf5-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="bbdf5-110">Vefslóðin í reitnum **Tengill umhverfis** er ekki gild</span><span class="sxs-lookup"><span data-stu-id="bbdf5-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="bbdf5-111">Farðu á síðuna **Umhverfistenglar**, opnið umhverfið sem ekki er hægt að tengjast við og veljið siðan aðgerðina **Prófa tenginguna**.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="bbdf5-112">Fyrirtæki viðskiptamannsins er nú ótengt, til dæmis ef verið er að uppfæra það</span><span class="sxs-lookup"><span data-stu-id="bbdf5-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="bbdf5-113">Á yfirlitinu skaltu velja **Verkfæri** valmyndaratriði og svo **Villuleit**.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="bbdf5-114">Þetta opnar lista með tæknilegum upplýsingum, svo þú kannt að vilja hafa samband við kerfisstjóra ef þú sérð villur.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="bbdf5-115">Til dæmis benda villuskilaboðin „*Netþjónninn hefur hafnað upplýsingum viðskiptamanns*“ til þess að þú hafir ekki aðgang.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="bbdf5-116">Þú hefur ekki aðgang að öllum fyrirtækjum í umhverfinu sem reynt er að tengjast við</span><span class="sxs-lookup"><span data-stu-id="bbdf5-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="bbdf5-117">Í [!INCLUDE [prod_short](includes/prod_short.md)] getur samsteypa verið með margar fyrirtækiseiningar sem kallast fyrirtæki og hugsanlega ertu ekki með aðgang að öllum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-117">In [!INCLUDE [prod_short](includes/prod_short.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="bbdf5-118">Hafðu samband við stjórnandann eða viðskiptavininn til að ganga úr skugga um að þú sért með aðgang að fyrirtækjunum sem þú þarft að vinna í.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="bbdf5-119">Gögn uppfærast ekki</span><span class="sxs-lookup"><span data-stu-id="bbdf5-119">Data does not refresh</span></span>

<span data-ttu-id="bbdf5-120">Þegar þú bætir við fyrirtæki eða biður um uppfærslu gagna sækir [!INCLUDE [prod_short](includes/prod_short.md)] gögnin.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-120">When you add a company or request a refresh of the data, [!INCLUDE [prod_short](includes/prod_short.md)] fetches the data.</span></span> <span data-ttu-id="bbdf5-121">Þú verður að uppfæra síðuna sjálfur, svo sem að velja aðgerðina **Endurbirta öll fyrirtæki**, uppfæra vafrasíðuna, fara af yfirlitinu og svo aftur í það eða annað svipað.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="bbdf5-122">Ef þú hefur bætt við fyrirtæki en það birtist ekki á listanum er einnig hægt að nota aðgerðina **Endurhlaða öllum fyrirtækjum** til að uppfæra listann.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbdf5-123">Sjá einnig .</span><span class="sxs-lookup"><span data-stu-id="bbdf5-123">See also</span></span>

[<span data-ttu-id="bbdf5-124">Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni</span><span class="sxs-lookup"><span data-stu-id="bbdf5-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="bbdf5-125">Bæta fyrirtækjum við fyrirtækjamiðstöðina</span><span class="sxs-lookup"><span data-stu-id="bbdf5-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="bbdf5-126">Upplifun endurskoðanda í Business Central</span><span class="sxs-lookup"><span data-stu-id="bbdf5-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  