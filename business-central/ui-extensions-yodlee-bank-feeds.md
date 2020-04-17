---
title: Afstemming greiðslu með Envestnet Yodlee Bank Feeds viðbótinni | Microsoft Docs
description: Lýsir Envestnet Yodlee Bank Feeds viðbótinni, sem tengist bankareikningum svo þú getir afstemmt greiðslur á fljótlegan máta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ca384d58046bd0c798038878a3ed93f5a00eeec5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189844"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="c12d3-103">Envestnet Yodlee Bank Feeds Viðbótin</span><span class="sxs-lookup"><span data-stu-id="c12d3-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="c12d3-104">Til að stemma af á skjótan hátt greiðslur gerðar inn á bankareikninga þína, þá leyfir Envestnet Yodlee Bank Feeds þjónustan þér að tengja bankareikning kerfis þíns við netbankareikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="c12d3-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="c12d3-105">Þetta þýðir að síðustu bankayfirlitinu er sjálfkrafa eða handvirkt streymt inn í afstemmingarbók þína, og tryggir að þú ert alltaf að vinna úr síðustu greiðslunum með lágmarks hættu á villum.</span><span class="sxs-lookup"><span data-stu-id="c12d3-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="c12d3-106">Envestnet Yodlee Bank Feeds Þjónustan er aðeins studd í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="c12d3-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="c12d3-107">Envestnet Yodlee Bank Feeds þjónustan er aðeins studd í netútgáfunni af Business Central.</span><span class="sxs-lookup"><span data-stu-id="c12d3-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="c12d3-108">Til að nota þessa virkni á staðnum verður þú að verða þér út um vörumerkjareikning frá Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="c12d3-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="c12d3-109">Envestnet Yodlee Bank Feeds Þjónustan er aðeins studd í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="c12d3-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="c12d3-110">Aðeins bankar sem eru búsettir í þessum löndum eru studdir, jafnvel þó að bankar frá öðrum löndum kunni að birtast í Envestnet Yodlee Bank Feeds valglugga banka í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c12d3-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c12d3-111">Vegna nýju tilskipunar um greiðsluþjónustu í Evrópu (PSD2), eftir 14. september 2019, verður ekki hægt að flytja sjálfkrafa bankayfirlit frá bönkum í Bretlandi inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c12d3-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c12d3-112">Við bjóðum hugsanlega upp á þennan eiginleika aftur í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="c12d3-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="c12d3-113">Envestnet Yodlee Bank Feeds þjónustan veitir eftirfarandi ávinning:</span><span class="sxs-lookup"><span data-stu-id="c12d3-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="c12d3-114">Fjarlægir þörfina fyrir handvirkum innslætti.</span><span class="sxs-lookup"><span data-stu-id="c12d3-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="c12d3-115">Bætir skilvirkni og nákvæmni þegar afstemming greiðslu er gerð.</span><span class="sxs-lookup"><span data-stu-id="c12d3-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="c12d3-116">Styður fjölda banka.</span><span class="sxs-lookup"><span data-stu-id="c12d3-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="c12d3-117">Leyfir nýjustu upplýsingar um bankafærslur úr [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c12d3-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="c12d3-118">Styður handvirka ásamt sjálfvirk bankastreymi.</span><span class="sxs-lookup"><span data-stu-id="c12d3-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="c12d3-119">Gerir mögulega útvistun greiðsluafstemmingar til endurskoðanda með því að veita aðgang að bankayfirlitum.</span><span class="sxs-lookup"><span data-stu-id="c12d3-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="c12d3-120">Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="c12d3-120">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c12d3-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c12d3-121">See Also</span></span>
<span data-ttu-id="c12d3-122">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="c12d3-122">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="c12d3-123">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="c12d3-123">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="c12d3-124">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c12d3-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
