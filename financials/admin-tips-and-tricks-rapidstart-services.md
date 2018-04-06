---
title: "Ábendingar: RapidStart Services | Microsoft Docs"
description: "Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e43859a6095f0087c12d0f9c071c0504d3781ad2
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="32443-103">Ábendingar: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="32443-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="32443-104">Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="32443-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="32443-105">Nota stillingasniðmát</span><span class="sxs-lookup"><span data-stu-id="32443-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="32443-106">Grunnstillingarsniðmát geta auðveldað innleiðingarferlið.</span><span class="sxs-lookup"><span data-stu-id="32443-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="32443-107">Með því að nota þau, er hægt að taka með svipaða viðskiptamenn í hlutum og þróa síðan innleiðingarreglu sem meðhöndlar alla viðskiptamenn í hluta á svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="32443-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="32443-108">Með því móti er hægt að nota forskilgreiningu að einhverju leyti fyrir hvern hluta og halda áfram með skjóta innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="32443-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="32443-109">Spurningalisti grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="32443-109">Configuration questionnaires</span></span>  
<span data-ttu-id="32443-110">Til að hjálpa til við útfyllingu skilgreiningarspurningalista skal íhuga að skilgreina sjálfgefin svör til að gefa bestu venjur til kynna.</span><span class="sxs-lookup"><span data-stu-id="32443-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="32443-111">Keyrslugerð af færslulínum</span><span class="sxs-lookup"><span data-stu-id="32443-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="32443-112">Mælt er með að nota gagnaflutningsverkfærin sem boðið er upp á til að færa bókarfærslur.</span><span class="sxs-lookup"><span data-stu-id="32443-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="32443-113">Ef keyrsla er notuð til að stofna færslubókarlínur hefur hún takmarkað gildissvið og myndar sjálfgefna reiti í færslubók.</span><span class="sxs-lookup"><span data-stu-id="32443-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="32443-114">Afganginum af færslubókinni þarf svo að ljúka handvirkt.</span><span class="sxs-lookup"><span data-stu-id="32443-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="32443-115">Flutningur á færslum</span><span class="sxs-lookup"><span data-stu-id="32443-115">Migrating transactions</span></span>  
<span data-ttu-id="32443-116">Mælt er með því að opnunarstöður séu fluttar í skrefum í eftirfarandi röð.</span><span class="sxs-lookup"><span data-stu-id="32443-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="32443-117">Flytja opnunarstöður fjárhags án þess að nota undirhöfuðbók fjárhagslykilsins.</span><span class="sxs-lookup"><span data-stu-id="32443-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="32443-118">Nota tiltekna mótfærslureikninga fyrir upphafsjöfnuð, einn uppsettan fyrir hverja undirhöfuðbók.</span><span class="sxs-lookup"><span data-stu-id="32443-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="32443-119">Setja upp mótfærslureikningana til að virkja beinar bókanir.</span><span class="sxs-lookup"><span data-stu-id="32443-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="32443-120">Flytja opnar færslur í viðskiptamannabók.</span><span class="sxs-lookup"><span data-stu-id="32443-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="32443-121">Flytja opnar birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="32443-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="32443-122">Flytja opnar eignafærslur.</span><span class="sxs-lookup"><span data-stu-id="32443-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="32443-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="32443-123">See Also</span></span>  
[<span data-ttu-id="32443-124">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="32443-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="32443-125">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="32443-125">Administration</span></span>](admin-setup-and-administration.md)

