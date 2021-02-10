---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dcfc54d36b212b296747d28945324ac46c38cada
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753618"
---
<span data-ttu-id="16c1b-101">Stundum styðja notendur við fleiri en eitt fyrirtæki og þurfa að skiptast á að vinna fyrir mismunandi fyrirtæki á auðveldan hátt [!INCLUDE [prod_short](prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="16c1b-101">People sometimes support more than one company and need to easily switch from working in one company to another in [!INCLUDE [prod_short](prod_short.md)].</span></span> <span data-ttu-id="16c1b-102">Til dæmis gæti fyrirtæki verið með söluskrifstofur í borgum og mörgum löndum og því er búið að stofna aðskildar fyrirtækjaeiningar fyrir hverja skrifstofu.</span><span class="sxs-lookup"><span data-stu-id="16c1b-102">For example, a business might have sales offices in cities and multiple countries, so it has created a separate business unit for each office.</span></span> <span data-ttu-id="16c1b-103">Skrifstofurnar sem eru í sama landi eru settar upp sem aðskilin fyrirtæki í sameiginlegu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="16c1b-103">The offices that are in the same country are set up as separate companies in a shared environment.</span></span> <span data-ttu-id="16c1b-104">Aðrar skrifstofur eru stofnaðar sem fyrirtæki í aðgreindu umhverfi þar sem þær eru landfræðilega staðsettar í öðrum löndum.</span><span class="sxs-lookup"><span data-stu-id="16c1b-104">Other offices are created as companies in separate environments because they are geographically based in other countries.</span></span><br><br>  

<span data-ttu-id="16c1b-105">Hvað er umhverfi?</span><span class="sxs-lookup"><span data-stu-id="16c1b-105">What's an environment?</span></span> <span data-ttu-id="16c1b-106">Fyrirtæki í [!INCLUDE[prod_short](prod_short.md)] eru til í því sem kallað er *umhverfi*.</span><span class="sxs-lookup"><span data-stu-id="16c1b-106">Companies in [!INCLUDE[prod_short](prod_short.md)] exist in what are referred to as *environments*.</span></span> <span data-ttu-id="16c1b-107">Tvær gerðir af umhverfi eru í boði **Framleiðsla** og **Sandkassi**.</span><span class="sxs-lookup"><span data-stu-id="16c1b-107">There are two types of environments, **Production** and **Sandbox**.</span></span> <span data-ttu-id="16c1b-108">Í stuttu máli inniheldur framleiðsluumhverfi virk viðskiptagögn og sandkassaumhverfi eru notuð sem er öruggur staður til að prófa hluti á borð við ný viðskiptaferli eða -eiginleika.</span><span class="sxs-lookup"><span data-stu-id="16c1b-108">In short, production environments contain live business data, and sandbox environments are used as a safe place to test things like new business processes or features.</span></span> <span data-ttu-id="16c1b-109">Frekari upplýsingar er að finna á [Gerðir umhverfis](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="16c1b-109">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span> <span data-ttu-id="16c1b-110">Ef þú hefur aðgang að fyrirtæki hefurðu aðgang að umhverfinu sem það er í.</span><span class="sxs-lookup"><span data-stu-id="16c1b-110">If you have access to a company, you have access to the environment it's in.</span></span> <span data-ttu-id="16c1b-111">Ef þú hefur aðgang að fleiri en einu fyrirtæki, og þau fyrirtæki eru í mismunandi umhverfi, þegar þú skráir þig inn á [!INCLUDE[prod_short](prod_short.md)] verður að tilgreina umhverfið sem þú vilt vinna í.</span><span class="sxs-lookup"><span data-stu-id="16c1b-111">If you have access to more than one company, and those companies are in different environments, when you sign in to [!INCLUDE[prod_short](prod_short.md)] you must specify the environment that you want to work in.</span></span> <span data-ttu-id="16c1b-112">Umhverfi eru breytileg eftir löndum þannig að ef fyrirtækið þitt starfar í mörgum löndum þarftu aðskilin umhverfi fyrir hvert land fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="16c1b-112">Environments are particular to a given country, so if your organization works in multiple countries, you need separate environments for each country.</span></span><br><br>  

<span data-ttu-id="16c1b-113">Hvað er fyrirtæki?</span><span class="sxs-lookup"><span data-stu-id="16c1b-113">What's a company?</span></span> <span data-ttu-id="16c1b-114">Hugsaðu um *fyrirtæki* sem geymi sem inniheldur upplýsingar um lögaðila.</span><span class="sxs-lookup"><span data-stu-id="16c1b-114">Think of a *company* as a container that holds information about a legal entity.</span></span> <span data-ttu-id="16c1b-115">Með vísan í dæmið hér að ofan rekur fyrirtækið eina söluskrifstofu í Seattle og aðra í New York svo það stofnar fyrirtæki í [!INCLUDE[prod_short](prod_short.md)] fyrir hverja skrifstofu þannig að það geti stjórnað aðgerðum hverrar skrifstofu fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="16c1b-115">Using the example above, the business has a sales office in Seattle and another in New York, so it creates a company in [!INCLUDE[prod_short](prod_short.md)] for each office so that it can manage operations for each office separately.</span></span>  