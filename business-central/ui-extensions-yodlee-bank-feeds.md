---
title: Afstemming greiðslu með Envestnet Yodlee Bank Feeds viðbótinni
description: Lýsir Envestnet Yodlee Bank Feeds viðbótinni, sem tengist bankareikningum svo þú getir afstemmt greiðslur á fljótlegan máta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9bdbcc208429bba15e30bc56cc8a4477312c1cdd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771236"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="59e88-103">Envestnet Yodlee Bank Feeds Viðbótin</span><span class="sxs-lookup"><span data-stu-id="59e88-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="59e88-104">Til að stemma af á skjótan hátt greiðslur gerðar inn á bankareikninga þína, þá leyfir Envestnet Yodlee Bank Feeds þjónustan þér að tengja bankareikning kerfis þíns við netbankareikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="59e88-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="59e88-105">Þetta þýðir að síðustu bankayfirlitinu er sjálfkrafa eða handvirkt streymt inn í afstemmingarbók þína, og tryggir að þú ert alltaf að vinna úr síðustu greiðslunum með lágmarks hættu á villum.</span><span class="sxs-lookup"><span data-stu-id="59e88-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="59e88-106">Envestnet Yodlee Bank Feeds Þjónustan er aðeins studd í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="59e88-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="59e88-107">Envestnet Yodlee Bank Feeds þjónustan er aðeins studd í netútgáfunni af Business Central.</span><span class="sxs-lookup"><span data-stu-id="59e88-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="59e88-108">Til að nota þessa virkni á staðnum verður þú að verða þér út um vörumerkjareikning frá Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="59e88-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="59e88-109">Envestnet Yodlee Bank Feeds Þjónustan er aðeins studd í Bandaríkjunum og Kanada.</span><span class="sxs-lookup"><span data-stu-id="59e88-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="59e88-110">Aðeins bankar sem eru búsettir í þessum löndum eru studdir, jafnvel þó að bankar frá öðrum löndum kunni að birtast í Envestnet Yodlee Bank Feeds valglugga banka í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="59e88-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59e88-111">Vegna nýju tilskipunar um greiðsluþjónustu í Evrópu (PSD2), eftir 14. september 2019, verður ekki hægt að flytja sjálfkrafa bankayfirlit frá bönkum í Bretlandi inn í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="59e88-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="59e88-112">Við bjóðum hugsanlega upp á þennan eiginleika aftur í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="59e88-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="59e88-113">Envestnet Yodlee Bank Feeds þjónustan veitir eftirfarandi ávinning:</span><span class="sxs-lookup"><span data-stu-id="59e88-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="59e88-114">Fjarlægir þörfina fyrir handvirkum innslætti.</span><span class="sxs-lookup"><span data-stu-id="59e88-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="59e88-115">Bætir skilvirkni og nákvæmni þegar afstemming greiðslu er gerð.</span><span class="sxs-lookup"><span data-stu-id="59e88-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="59e88-116">Styður fjölda banka.</span><span class="sxs-lookup"><span data-stu-id="59e88-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="59e88-117">Leyfir nýjustu upplýsingar um bankafærslur úr [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="59e88-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="59e88-118">Styður handvirka ásamt sjálfvirk bankastreymi.</span><span class="sxs-lookup"><span data-stu-id="59e88-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="59e88-119">Gerir mögulega útvistun greiðsluafstemmingar til endurskoðanda með því að veita aðgang að bankayfirlitum.</span><span class="sxs-lookup"><span data-stu-id="59e88-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="59e88-120">Bankastreymi í boði</span><span class="sxs-lookup"><span data-stu-id="59e88-120">Available Bank Feeds</span></span>
<span data-ttu-id="59e88-121">Hægt er að skoða hvort banki sé studdur með því að setja upp og tengjast við Envestnet Yodlee Bank Feeds-þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="59e88-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="59e88-122">Bankinn mun birtast á listanum ef hann er studdur af Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="59e88-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="59e88-123">Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="59e88-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="59e88-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="59e88-124">See Also</span></span>
<span data-ttu-id="59e88-125">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="59e88-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="59e88-126">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="59e88-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="59e88-127">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59e88-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]