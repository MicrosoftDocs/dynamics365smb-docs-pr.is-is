---
title: Uppsetning bankareikninga| Microsoft Docs
description: "Hægt er að afstemma bankareikninga við yfirlit frá bankanum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3b52026643eee4fa2eb4625c99c881789e0373ed
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-bank-accounts"></a>Bankareikningar settir upp
Þú notar bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fylgjast með bankafærslunum þínum. Hægt er að hafa reikninga í SGM eða erlendum gjaldmiðli. Þegar bankareikningar hafa verið settir upp er einnig hægt að nota valkostinn prentskoðun.

## <a name="to-set-up-bank-accounts"></a>Bankareikningar settir upp
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bankareikningar** og veldu síðan tengda tengilinn.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Til að fylla út í reitinn **Staða** með onunarstöðu verður þú að bóka fjárhagsfærslu bankareiknings með upphæðinni. Hægt er að gera þetta með því að framkvæma afstemmingu bankareiknings. Frekari upplýsingar í [Afstemma Bankareikninga Sérstaklega](bank-how-reconcile-bank-accounts-separately.md). Einnig er hægt að tiltaka opnunarstöðu sem hluta af almennri gagnamyndun í nýjum fyrirtækjum með því að nota hjálpina fyrir **Flytja viðskiptagögn**. Nánari upplýsingar er að finna í [Hafist handa](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Til að setja upp bankareikning þinn til að flytja inn eða flytja út bankaskrár
Reitir á **Flutningur** flýtiflipanum á síðunni **Bankareikningsspjald** eru tengdir innflutningi og útflutningi á bankastraumum og skrám. Frekari upplýsingar er að finna í [Setja upp umskráningarþjónusta fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md) og [Setja upp Envestnet Yodlee Bank Feeds þjónustu](bank-how-setup-bank-statement-service.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bankareikningar** og veldu síðan tengda tengilinn.
2. Opnaðu kortið fyrir bankareikning sem þú vilt flytja út eða flytja inn bankaskrár fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Flytja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunni **Bankareikningsspjald**. Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána. Svo lestu stuttar lýsingar á reitunum vandlega eða vísaðu til viðkomandi efnisferlis. Til dæmis, við útflutning greiðsluskráar fyrir kortamillifærslu NA (EFT) þarf að fylla út reitina **Síðasta greiðslutilkynningarnúmer** og **Kenninúmer**. Frekari upplýsingar eru í [Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa
Reitir á **Flutningur** flýtiflipanum á síðunni **Bankareikningsspjald lánardrottins** eru tengdir útflutningi á bankastraumum og skrám. Nánari upplýsingar er að finna í [Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md) og [Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **lánardrottnar** og veldu síðan tengda tengilinn.
2. Opnaðu kortið fyrir lánardrottinn með bankareikning sem þú sendir út greiðslubankaskrár til.
3. Veldu aðgerðina **Bankareikningar**.
3. Á síðunni **Bankareikn.spjald lánardr** á flipanum **Flutningur** fylltu inn reitina eftir því sem þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

