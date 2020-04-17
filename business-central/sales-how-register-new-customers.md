---
title: Stofna viðskiptamannaspjald til að skrá nýja viðskiptamenn | Microsoft Docs
description: Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða biðlara sem selt er til.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0bdc559f04064e2b4d49ef4ed7a8759c68be3579
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194044"
---
# <a name="register-new-customers"></a>Skrá nýja viðskiptamenn
Viðskiptamenn eru uppruni tekna. Þú verður að skrá þig hver viðskiptavinur sem þú selur sem viðskiptavinakort. Viðskiptamannaspjald inniheldur upplýsingarnar sem þarf til að selja vörur til viðskiptamannsins. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).  

Áður en hægt er að skrá nýja viðskiptamenn þarf að setja upp ýmsar sölukóða sem hægt er að velja úr þegar fyllt eru út viðskiptamannaspjöld. Nánari upplýsingar er að finna í [Uppsetning sölu](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

> [!NOTE]  
> Ef viðskiptamannasniðmát eru til fyrir mismunandi tegundir viðskipamanna, þá birtist sjálfkrafa síða þegar búið er til nýtt viðskiptamannaspjald og hægt er að velja viðeigandi sniðmát. Ef aðeins eitt viðskiptamanna sniðmát er fyrir hendi, nota ný viðskiptamannaspjöld alltaf það sniðmát.  

## <a name="to-create-a-new-customer-card"></a>Að stofna nýtt viðskiptamannaspjald
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.  
2. Á síðunni **Viðskiptamenn** skal velja aðgerðina **Nýtt**.

    Ef aðeins eitt viðskiptamannasniðmát er fyrir hendi, opnast nýtt viðskiptamannaspjald með reiti útfyllta með upplýsingum úr sniðmátinu.

    Ef fleiri en eitt viðskiptamannasniðmát er fyrir hendi, þá birtist sjálfkrafa síða með tiltækum viðskiptamannasniðmátum. Í því tilviki, fylgið næstu tveimur skrefum.
3. Á síðunni **Velja sniðmát fyrir nýjan viðskiptamann** skal velja sniðmátið sem á að nota fyrir nýja viðskiptamannaspjaldið.
4. Velja hnappinn **Í lagi**. Nýtt viðskiptamannaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í reitina.  
5. Því næst skal færa inn eða breyta reitum á viðskiptamannaspjaldinu eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Á flýtiflipanum **Söluverð** er hægt að sjá sérverð eða afslætti sem veittir eru fyrir viðskiptamanninn ef ákveðin skilyrði eru uppfyllt, svo sem vara, lágmarkspöntunarmagn eða lokadagur. Hver lína stendur fyrir sértilboðsverð eða línuafslátt. Hver dálkur táknar viðmiðun sem verða að sækja til að réttlæta sérstakt verð sem þú slærð inn í **Einingaverð** sviði, eða línuafslátt sem þú slærð inn í **Línuafsláttur %**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

Viðskiptamaðurinn hefur nú verið skráður og viðskiptamannaspjaldið má nú nota í söluskjölum.

Ef nota á þetta viðskiptamannaspjald sem sniðmát þegar ný viðskiptamannaspjöld eru búin til, vistið það sem sniðmát. Nánari upplýsingar eru í eftirfarandi kafla.

## <a name="to-save-the-customer-card-as-a-template"></a>Til að vista viðskiptamannaspjaldið sem sniðmát
1. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Vista sem sniðmát**. Síðan **Viðskiptamannasniðmát** opnast og sýnir viðskiptamannaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir viðskiptamanninn.
4. Breyta eða færa inn víddarkóða sem munu gilda fyrir ný viðskiptamannaspjöld sem stofnuð eru með sniðmátinu.  
5. Þegar lokið hefur verið við nýja viðskiptamannasniðmátið skal velja hnappinn **Í lagi**.

Viðskiptamannasniðmátinu verður bætt við lista viðskiptamannasniðmáta þannig að hægt er að nota það til að búa til ný viðskiptamannaspjöld.

## <a name="see-also"></a>Sjá einnig
[Skilgreina Greiðsluhætti](finance-payment-methods.md)  
[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Sala](sales-manage-sales.md)    
[Uppsetning sölu](sales-setup-sales.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
