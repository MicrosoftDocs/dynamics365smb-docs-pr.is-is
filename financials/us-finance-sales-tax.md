---
title: "Söluskattur og skattflokkar í Bandaríkjunum og Kanada | Microsoft Docs"
description: "Fræðast um hvernig söluskattur er sett upp og hvernig skattflokka, skattsvæði, skattlögsögur og skattasundurliðanir vinna."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Söluskattur og skattflokkar í Bandaríkjunum og Kanada
Þegar fyrst er byrjað að nota [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að keyra hjálparuppsetningu til að setja fljótt og einfalt upp söluskattsupplýsingar fyrir fyrirtæki þitt , viðskiptamenn og lánardrottna. Á nokkrum mínútur, er hægt að stofna söluskjöl og innkaupaskjölum með rétt reiknaðan söluskatt. Þetta er útskýrt [í okkar bloggpóstum](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Ef þú færir yfir í tóma mitt fyrirtæki, mælum við með að þú byrjir að nota hvern og einn hjálparuppsetningarleiðbeiningar, þar á meðan einn fyrir VSK. Ef kosið er að setja upp söluskattur sjálfur, útskýrir þessi grein hvað þarf að taka tillit til.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Skattflokka, Skattsvæði og Skattlögsögur
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] táknar skattahópur hóp af birgðatölum eða fjármunum sem eru háð sömu skattskilmálum. Til dæmis er hægt að setja upp skattflokkur fyrir vörur sem eru skattskyld og aðrar óskattskyldar vörur. Þú Verður að úthluta skattflokkskóði fyrir vörur í birgðum og fjárhagsreikninga. Á sama hátt verður að úthluta skattsvæðiskóðum til viðskiptamanna, staðsetninga og eigin stillingar fyrirtækis. Uppsetningar með hjálp hjálpa þér að gera þetta.  

Hver skattsvæði er flokkaskipan söluskattslögsagnarumdæma sem byggðar eru á tiltekna landsvæði. Til dæmis innifela skattsvæði Miami, Florida þrjú lögsagnarumdæmi söluskatts: (Miami) bær, sýsla (Dade) og sýsla (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] felur í sér takmarkað safn skattsvæða, með sjálfgefinnar grunnstillingar, en hægt að breyta þeim og bæta við nýjum skattsvæði.  

Ef sett er upp ný skattsvæði og skattlögsögur þarf að ganga úr skugga um að fylla út reitina rétt. Í Bandaríkjunum, geta ríki, sýslur og bæir og bæjarfélag rukkað VSK. Í Canada, getur alríkisstjórnin og sveitarfélög rukkað söluskatt. Stofnanir safna og standa skil söluskattur til þessara stjórnvalda fyrir vörur seldar til notenda Söluskattur er einnig hægt að greiða til núverandi söluskattur. Til dæmis, skatta má reikna á sölureikningi upphæð sem þegar inniheldur skatt frá öðrum löndum.  

Í Kanada, verður skattfjárhæðirnar að vera ítarlegar fyrir hvern skattalögsögu. Allt að fjórir lögsagnarumdæmi hægt að sýna í skjali, og lögsagnarumdæmi sem hafa sama prenta röð eru sameinuð þegar þeir eru prentaðir.  

## <a name="tax-details"></a>Skattsundurliðun
Í **Skattasundurliðanir** glugginn sýnir mismunandi samsetningar söluskattlögsagaa og söluskatthópa til að finna gengi söluskatts. Fyrir hverja skatta lögsögu, mælum við með að þú stillir upp einn skatt hóp fyrir venjulega söluskattur, annar skatthópur fyrir vörur eða þjónustu sem ekki eru skattlagðar, og til viðbótar skatthóp fyrir hverja tegund af hlut eða þjónustu sem er stjórnað með mismunandi söluskatthlutfalli í þeirri lögsögu.  

Í Bandaríkjunum, þegar þú selur til viðskiptavina á stað þar sem þú þarft ekki að hafa *situs* - eða löglega staðsetningu í því ríki - innheimtirðu ekki VSK. Að stöðum þar sem þú ert ekki með situs, skal tryggja að bæði **skattur undir lágmarki ** og **skattur yfir hámarki ** reitir eru 0.00.  

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Söluskattur og vöru- og þjónustuskattur í Kanada](ca-finance-tax.md)  
[Uppsetning Söluskatts gert auðvelt](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

