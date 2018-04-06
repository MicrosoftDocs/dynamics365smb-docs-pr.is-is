---
title: "Stofna birgðaspjald fyrir vörur eða þjónustu| Microsoft Docs"
description: "Þú býrð til spjöld fyrir þjónustu sem þú selur sem klukkutíma og fyrir efnislegar vörur eins og t.d. samsetningaríhlutir, fullunnar vörur eða hráefni sem þú selur úr birgðum."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9643e71c29adf4b4be1d9d474832e3e29f2c21d8
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="register-new-items"></a>Skrá nýjar vörur
Vörur, ásamt öðrum framleiðsluvörum, eru grundvöllur fyrirtækisins, vörurnar eða þjónustan sem þú stundar viðskipti með. Hver vara verður að vera skráð sem birgðaspjald.

Birgðaspjald inniheldur upplýsingarnar sem þarf til að kaupa, selja, geyma og tilkynna vörur.

Birgðaspjaldið getur verið af gerðinni **Birgðir** eða **Þjónusta** til að tilgreina hvort vara er rauneining eða launatímaeining. Fyrir utan suma reiti sem tengjast efnislegum hlutum vöru, virka allir reitir birgðaspjaldi eins fyrir birgðavörur og þjónustu. Fyrir nánari upplýsingar um vörusölu, sjá [Selja vörur](sales-how-sell-products.md) eða [Reikningsfæra vörur](sales-how-invoice-sales.md).

Hlutur getur verið uppbyggður sem yfireining með undirliggjandi undireiningu í uppskrift. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] getur uppskrift verið annað hvort framleiðsluuppskrift eða samsetningaruppskrift, út frá notkun. Nánari upplýsingar er að finna í [Vinna með uppskrift.](inventory-how-work-BOMs.md)

> [!NOTE]  
>   Ef vörusniðmát er til fyrir mismunandi vörutegundir, þá birtist gluggi þar sem búið er til nýtt birgðaspjald og hægt er að velja viðeigandi vörusniðmát. Ef aðeins eitt vörusniðmát er fyrir hendi, nota ný birgðaspjöld alltaf það sniðmát.

Ef sama varan er keypt frá fleiri en einum lánardrottni, er hægt að tengja þessa lánardrottna við birgðaspjaldið. Lánardrottnarnir munu þá birtast í **Vörulisti lánardrottins** glugganum, þannig að þú getir auðveldlega valið annan lánardrottinn.

## <a name="to-create-a-new-item-card"></a>Að búa til nýtt vöruspjald
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.  
2. Í glugganum **Vörur** skal velja aðgerðina **Nýtt**.

    Ef aðeins eitt vörusniðmát er fyrir hendi, opnast nýtt birgðaspjald með suma af reitunum útfyllta með upplýsingum úr sniðmátinu.
3. Í glugganum **Velja sniðmát fyrir nýja vöru** skal velja sniðmátið sem á að nota fyrir nýja birgðaspjaldið.
4. Velja hnappinn **Í lagi**. Nýtt birgðaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í suma reitina.
5. Því næst skal færa inn eða breyta reitum á birgðaspjaldinu eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Í reitnum **Aðferð kostnaðarútreiknings** seturðu upp hvernig kerfið reiknar út kostnaðarverð með því að áætla vöruflæði fyrirtækisins. Fimm aðferðir kostnaðarútreiknings eru í boði, út frá gerð vörunnar. Nánari upplýsingar eru í [Upplýsingar um hönnun: Kostnaðarútreikningar](design-details-costing-methods.md).
>
> Ef þú velur **Meðaltal** er kostnaðarverð vöru reiknað sem meðaleiningaverð vara á hverjum tímapunkti eftir innkaup. Fyrir verðmat birgða, er gert ráð fyrir að allar birgðir verði seldar á sama tíma. Með þessar stillingar geturðu valið **kostnaðarverð** reitinn í glugganum **Meðalkostnaður útreiknaður yfirlit** til að skoða færslusöguna sem meðalkostnaður er reiknaður út frá.

Á **Verð og bókun** flýtiflipanum geturðu skoðað sérstakt verð eða afslætti sem þú veitir fyrir vöruna ef tilteknar viðmiðanir eru uppfylltar, svo sem viðskiptavina, lágmarksfjöldi eða lokadagur. Hver lína stendur fyrir sértilboðsverð eða línuafslátt. Hver dálkur táknar viðmiðun sem verða að sækja til að réttlæta sérstakt verð sem þú slærð inn í **Einingaverð** sviði, eða línuafslátt sem þú slærð inn í **Línuafsláttur %**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

Varan hefur nú verið skráð og birgðaspjaldið má nú nota í skjölum vegna kaupa og sölu.

Ef nota á þetta birgðaspjald sem sniðmát þegar ný birgðaspjöld eru búin til, vistið það sem sniðmát. Nánari upplýsingar eru í eftirfarandi kafla.

## <a name="to-save-the-item-card-as-a-template"></a>Til að vista birgðaspjald sem sniðmát
1. Í glugganum **Birgðaspjald** skal velja aðgerðina **Vista sem sniðmát**. Glugginn **Vörusniðmát** opnast og sýnir birgðaspjaldið sem sniðmát.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Glugginn **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir vöruna.
4. Breyta eða færa inn víddarkóta sem munu gilda fyrir ný birgðaspjöld sem stofnuð eru með sniðmátinu.
5. Þegar lokið hefur verið við nýja vörusniðmátið skal velja hnappinn **Í lagi**.

Vörusniðmátinu verður bætt við lista vörusniðmáta þannig að hægt er að nota það til að búa til ný birgðaspjöld.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Margir lánardrottnar settir upp fyrir vörur  
Ef sama varan er keypt frá fleiri en einum lánardrottni þarf að færa inn upplýsingar um hvern lánardrottinn eins og verð, afhendingartími, afsláttur o.s.frv.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.  
2.  Velja skal viðeigandi vöru og síðan aðgerðina **Breyta**.  
3.  Veljið **Lánardrottinn** aðgerðina.  
4.  Velja reitinn **Nr. lánardrottins** og síðan velja þann lánardrottinn sem setja á upp fyrir vöruna.  
5.  Einnig er hægt að fylla inn í þá reiti sem eftir eru.  
6.  Endurtakið skref 2 til 5 fyrir hvern þann lánardrottinn sem þú vilt kaupa vöru af.

Lánardrottnarnir munu nú birtast í **Vörulisti lánardrottins** glugganum, sem þú opnar frá birgðaspjaldinu, þannig að þú getir auðveldlega valið annan lánardrottinn.

## <a name="see-also"></a>Sjá einnig
  [Birgðir](inventory-manage-inventory.md)  
  [Innkaup](purchasing-manage-purchasing.md)  
  [Sala](sales-manage-sales.md)  
  [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

