---
title: 'Ábendingar: RapidStart Services | Microsoft Docs'
description: Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e301d788fdedacf0fc2ac3ce29946df965bed711
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777067"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="d461e-103">Ábendingar og góð ráð: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="d461e-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="d461e-104">Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="d461e-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="d461e-105">Nota stillingasniðmát</span><span class="sxs-lookup"><span data-stu-id="d461e-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="d461e-106">Grunnstillingarsniðmát geta auðveldað innleiðingarferlið.</span><span class="sxs-lookup"><span data-stu-id="d461e-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="d461e-107">Með því að nota þau, er hægt að taka með svipaða viðskiptamenn í hlutum og þróa síðan innleiðingarreglu sem meðhöndlar alla viðskiptamenn í hluta á svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="d461e-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="d461e-108">Með því móti er hægt að nota forskilgreiningu að einhverju leyti fyrir hvern hluta og halda áfram með skjóta innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="d461e-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="d461e-109">Spurningalisti grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="d461e-109">Configuration questionnaires</span></span>

<span data-ttu-id="d461e-110">Til að hjálpa til við útfyllingu skilgreiningarspurningalista skal íhuga að skilgreina sjálfgefin svör til að gefa bestu venjur til kynna.</span><span class="sxs-lookup"><span data-stu-id="d461e-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="d461e-111">Keyrslugerð af færslulínum</span><span class="sxs-lookup"><span data-stu-id="d461e-111">Batch creation of journal lines</span></span>

<span data-ttu-id="d461e-112">Mælt er með að nota gagnaflutningsverkfærin sem boðið er upp á til að færa bókarfærslur.</span><span class="sxs-lookup"><span data-stu-id="d461e-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="d461e-113">Ef keyrsla er notuð til að stofna færslubókarlínur hefur hún takmarkað gildissvið og myndar sjálfgefna reiti í færslubók.</span><span class="sxs-lookup"><span data-stu-id="d461e-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="d461e-114">Afganginum af færslubókinni þarf svo að ljúka handvirkt.</span><span class="sxs-lookup"><span data-stu-id="d461e-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="d461e-115">Flutningur á færslum</span><span class="sxs-lookup"><span data-stu-id="d461e-115">Migrating transactions</span></span>

<span data-ttu-id="d461e-116">Mælt er með því að opnunarstöður séu fluttar í skrefum í eftirfarandi röð.</span><span class="sxs-lookup"><span data-stu-id="d461e-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="d461e-117">Flytja opnunarstöður fjárhags án þess að nota undirhöfuðbók fjárhagslykilsins.</span><span class="sxs-lookup"><span data-stu-id="d461e-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="d461e-118">Nota tiltekna mótfærslureikninga fyrir upphafsjöfnuð, einn uppsettan fyrir hverja undirhöfuðbók.</span><span class="sxs-lookup"><span data-stu-id="d461e-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="d461e-119">Setja upp mótfærslureikningana til að virkja beinar bókanir.</span><span class="sxs-lookup"><span data-stu-id="d461e-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="d461e-120">Flytja opnar færslur í viðskiptamannabók.</span><span class="sxs-lookup"><span data-stu-id="d461e-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="d461e-121">Flytja opnar birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="d461e-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="d461e-122">Flytja opnar eignafærslur.</span><span class="sxs-lookup"><span data-stu-id="d461e-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="d461e-123">Gera hvern pakka viðráðanlegri</span><span class="sxs-lookup"><span data-stu-id="d461e-123">Make each package manageable</span></span>

<span data-ttu-id="d461e-124">Þegar skilgreiningarpakkar eru notaðir til að flytja gögn, skal aðskilja gögnin í aðskilda pakka til að auðveldara sé að meðhöndla þá.</span><span class="sxs-lookup"><span data-stu-id="d461e-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="d461e-125">Ef ætlunin er til dæmis að flytja fjárhagsfærslur 20 ára gæti innflutningurinn tekið margar klukkustundir og daga.</span><span class="sxs-lookup"><span data-stu-id="d461e-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="d461e-126">Þess í stað skaltu skipta gögnunum upp þannig að hver pakki verði viðráðanlegri.</span><span class="sxs-lookup"><span data-stu-id="d461e-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="d461e-127">Sem stendur eru engar fastreglur til um gerð pakka, en ef þú sérð vandamál við að flytja pakka inn eða út skaltu prófa að minnka hann og sjá hvort það hjálpar.</span><span class="sxs-lookup"><span data-stu-id="d461e-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d461e-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d461e-128">See Also</span></span>

[<span data-ttu-id="d461e-129">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="d461e-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="d461e-130">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="d461e-130">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]