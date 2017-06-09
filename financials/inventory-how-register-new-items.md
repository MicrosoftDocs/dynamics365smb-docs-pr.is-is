---
title: "Hvernig á að: Skráð nýjar vörur | Microsoft Docs"
description: "Búðu til spjöld fyrir nýjar vörur sem þú selur úr birgðum í t.d. stykki eða þjónustu sem þú selur sem klukkutíma."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 582e006291e51e19d80304d24ae055ce6ac8d698
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-items"></a>Hvernig á að Skrá nýjar vörur
Atriði, meðal annars vara, eru grundvöllur fyrirtækis þíns, vöru eða þjónustu sem þú viðskipti með. Hver vara verður að vera skráð sem birgðaspjald.

Birgðaspjald inniheldur upplýsingarnar sem þarf til að kaupa, selja, geyma og tilkynna vörur.

Birgðaspjaldið getur verið af gerðinni **Birgðir** eða **Þjónusta** til að tilgreina hvort vara er rauneining eða launatímaeining. Fyrir utan suma reiti sem tengjast efnislegum hlutum vöru, virka allir reitir birgðaspjaldi eins fyrir birgðavörur og þjónustu. Fyrir nánari upplýsingar um vörusölu, sjá [Hvernig á að: Selja vörur](sales-how-sell-products.md) eða [Hvernig á að: Reikningsfæra vörur](sales-how-invoice-sales.md).

Hlutur getur verið uppbyggður sem yfireining með undirliggjandi undireiningu í uppskrift. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er uppskrift vísað til sem samsetningaruppskrift. Þú notar samsetningaruppskrift til að byggja upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir. Nánari upplýsingar er að finna í [Hvernig á að: Vinna með uppskrift.](inventory-how-work-BOMs.md)

**Athugasemd**: Ef vörusniðmát er til fyrir mismunandi tegundir vara, þá birtist gluggi þar sem búið er til nýtt birgðaspjald og hægt er að velja viðeigandi vörusniðmát. Ef aðeins eitt vörusniðmát er fyrir hendi, nota ný birgðaspjöld alltaf það sniðmát.

## <a name="to-create-a-new-item-card"></a>Að búa til nýtt vöruspjald
1. Á heimasíðunni skal velja aðgerðina **vörur ** til að opna listann yfir núverandi vörur.  
2. Í glugganum **Vörur** skal velja aðgerðina **Nýtt**.

    Ef aðeins eitt vörusniðmát er fyrir hendi, opnast nýtt birgðaspjald með suma af reitunum útfyllta með upplýsingum úr sniðmátinu.
3. Í glugganum **Velja sniðmát fyrir nýja vöru** skal velja sniðmátið sem á að nota fyrir nýja birgðaspjaldið.
4. Velja hnappinn **Í lagi**. Nýtt birgðaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í suma reitina.
5. Því næst skal færa inn eða breyta reitum á birgðaspjaldinu eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Á **Verð og bókun** flýtiflipanum geturðu skoðað sérstakt verð eða afslætti sem þú veitir fyrir vöruna ef tilteknar viðmiðanir eru uppfylltar, svo sem viðskiptavina, lágmarksfjöldi eða lokadagur. Hver lína stendur fyrir sértilboðsverð eða línuafslátt. Hver dálkur táknar viðmiðun sem verða að sækja til að réttlæta sérstakt verð sem þú slærð inn í **Einingaverð** sviði, eða línuafslátt sem þú slærð inn í **Línuafsláttur (%**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

Varan hefur nú verið skráð og birgðaspjaldið má nú nota í skjölum vegna kaupa og sölu.

Ef nota á þetta birgðaspjald sem sniðmát þegar ný birgðaspjöld eru búin til, vistið það sem sniðmát. Nánari upplýsingar eru í eftirfarandi kafla.

## <a name="to-save-the-item-card-as-a-template"></a>Til að vista birgðaspjald sem sniðmát
1. Í glugganum **Birgðaspjald** skal velja aðgerðina **Vista sem sniðmát**. Glugginn **Vörusniðmát** opnast og sýnir birgðaspjaldið sem sniðmát.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Glugginn **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir vöruna.
4. Breyta eða færa inn víddarkóta sem munu gilda fyrir ný birgðaspjöld sem stofnuð eru með sniðmátinu.
5. Þegar lokið hefur verið við nýja vörusniðmátið skal velja hnappinn **Í lagi**.

Vörusniðmátinu verður bætt við lista vörusniðmáta þannig að hægt er að nota það til að búa til ný birgðaspjöld.

## <a name="see-also"></a>Sjá einnig
  [Birgðir](inventory-manage-inventory.md)  
  [Innkaup](purchasing-manage-purchasing.md)  
  [Sala](sales-manage-sales.md)  
  [Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
