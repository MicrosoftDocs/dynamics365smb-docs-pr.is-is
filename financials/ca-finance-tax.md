---
title: "Söluskattur í Kanada| Microsoft Docs"
description: "Kynntu þér staðbundinn söluskatt og vöru- og þjónustuskatt í Kanada"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="f8107-103">Skráning söluskatts og vöru- og þjónustuskatts í Kanada</span><span class="sxs-lookup"><span data-stu-id="f8107-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="f8107-104">Í Kanada gilda þær reglur að þegar lánardrottinn hefur ekki viðskiptalögsögu í því fylki sem viðskiptin eru gerð í mun lánardrottinn aðeins innheimta vöru- og þjónustuskatt (GST) eða samræmdan söluskatt (HST).</span><span class="sxs-lookup"><span data-stu-id="f8107-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="f8107-105">Hins vegar, ef fylkið notar fylkissöluskatt (PST) mun kaupandinn þurfa að reikna út PST, og borga hann beint til fylkisins.</span><span class="sxs-lookup"><span data-stu-id="f8107-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="f8107-106">Þegar svæðisskattasvæðisnúmer er valið, notar [!INCLUDE[d365fin](includes/d365fin_md.md)] það til að reikna PST og senda það þannig að skattskyldur sé í bæði aðalbókinni og skattaskráningaskrárunum.</span><span class="sxs-lookup"><span data-stu-id="f8107-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="f8107-107">Þar af leiðandi ætti skattsvæðiskóði fylkis einungis að fela í sér PST, ekki GST.</span><span class="sxs-lookup"><span data-stu-id="f8107-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="f8107-108">Frekari upplýsingar um söluskatt má sjá í [Söluskattur og skattflokkar í Bandaríkjunum og Kanada](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="f8107-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="f8107-109">Að senda GST/HST skrá</span><span class="sxs-lookup"><span data-stu-id="f8107-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="f8107-110">Upplýsingar um skatta í innkaupaskjölum eru notaðar til að búa til GST/HST millifærsluskrá á netinu sem verður að berast til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="f8107-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="f8107-111">Þessi skrá inniheldur vöru- og þjónustuskatt (GST) og samræmdan söluskatt (HST).</span><span class="sxs-lookup"><span data-stu-id="f8107-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="f8107-112">Skráin er búin til í skráarsniði fyrir skatt, sem hægt er að millifæra yfir netið.</span><span class="sxs-lookup"><span data-stu-id="f8107-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8107-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f8107-113">See Also</span></span>
[<span data-ttu-id="f8107-114">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f8107-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="f8107-115">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="f8107-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="f8107-116">Söluskattur og skattflokkar í Bandaríkjunum og Kanada</span><span class="sxs-lookup"><span data-stu-id="f8107-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="f8107-117">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8107-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

