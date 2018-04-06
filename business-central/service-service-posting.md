---
title: "Bókun þjónustu | Microsoft Docs"
description: "Aðgerðin bókun þjónustu gerir skilvirka vinnslu á skjölum notandans mögulega og viðheldur árangursríkri stefnu í þjónustu við viðskiptamenn. Hægt er að búa til og uppfæra bókuð fylgiskjöl, og búa til fjárhagsfærslur í þjónustusvæði og öðrum einingum til þess að tryggja rétta uppfærslu."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b191b5e8fbe0a60a32d32bd2dc1ca0cca07c06e4
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="service-posting"></a>Þjónustubókun
Aðgerðin bókun þjónustu gerir skilvirka vinnslu á skjölum notandans mögulega og viðheldur árangursríkri stefnu í þjónustu við viðskiptamenn. Hægt er að búa til og uppfæra bókuð fylgiskjöl, og búa til fjárhagsfærslur í þjónustusvæði og öðrum einingum til þess að tryggja rétta uppfærslu.  

> [!NOTE]  
>  Eftirfarandi lýstir þjónustubókun burtséð frá því hvernig vörur eru efnislega meðhöndlaðar í vöruhúsinu.  
>   
>  Í þeim birgðageymslum sem ekki þurfa vöruhúsaafgreiðslu er bókun framkvæmd beint úr glugganum **Þjónustulínur**. Í birgðageymslum sem nota vöruhúsaafgreiðslu eru bókunaraðgerðirnar, fyrir utan Afhenda og Nota, framkvæmdar óbeint með ýmsum afhendingaraðgerðum vöruhúsa, eftir uppsetningu. Frekari upplýsingar, sjá [Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Afhenda  
Afhendingarvalkosturinn gerir kleift að skrá viðkomandi vörur og tímasetningu færslu í línur þjónustupöntunarinnar þegar þjónustu er lokið. Bókuð afhending er búin til og einingin Birgðir og aðrar einingar eru uppfærðar í [!INCLUDE[d365fin](includes/d365fin_md.md)] og gefur þannig til kynna að vörurnar hafi verið fjarlægðar úr birgðum og sendar viðskiptamanni. Einkum eru framleiddar birgðafærslur, virðisfærslur, þjónustufærslur og ábyrgðarfærslur.  

Ef birgðageymslan er sett upp þannig að hún krefjist vöruhúsaafgreiðslu virka afhending og færsla þjónustulínuvara á sama hátt og í öðrum upprunaskjölum. Eini munurinn er sá að hægt er að nota þjónustulínuvörurnar við ytri eða innri vinnslu, sem krefst tvenns konar mismunandi afhendingarvirkni.

## <a name="invoice"></a>Reikningsfæra  
Nota verður reikningsvalkostinn til þess að gefa út reikning til þess að færa þjónustu á kostnað viðskiptamanns. Yfirleitt er það mismunurinn á afhentu magni sem skráð er í virknina **Bóka afhendingu** og notað magn sem skráð er í virknina **Bóka notkun** sem er reikningsfært. Ekki er hægt að reikningsfæra það sem ekki er búið að afhenda. Þegar virknin **Bóka reikninga** er notuð er bókaður þjónustureikningur stofnaður og bókuð fylgiskjöl uppfærð til þess að gera þau samkvæm magninu sem skráð er í útgefinn reikning. Eins og gildir um aðrar bókunaraðferðir eru viðeigandi fjárhagsfærslur framleiddar og þar með taldar Fjárhagsfærslur.  

## <a name="ship-and-invoice"></a>Afhenda og reikningsfæra  
Valkosturinn afhenda og reikningsfæra gerir kleift að gefa út þjónustuafhendingu og reikning á sama tíma.  

## <a name="ship-and-consume"></a>Afhenda og nota  
Með valkostinum Afhenda og nota er hægt að skrá og bóka vörur, kostnað eða klukkustundir sem farið hafa í þjónustu en ekki er hægt að hafa innifalda í reikningi til viðskiptamanns. Reikningur er ekki gefinn út, en hægt er að gefa út þjónustuafhendingu og þjónustunotkun samtímis til þess að gefa til kynna að viðskiptamaður hefur fengið vörur eða klukkustundir án endurgjalds. Hliðstæðar fjárhagsfærslur eru líka búnar til svo notkunin sé skráð.  

> [!NOTE]  
>  Þjónustubókunaraðferðin gerir kleift að stofna hlutabókun. Hægt er að stofna afhendingu að hluta eða reikning að hluta með því að útfylla reitinn **Magn til afhendingar** og reitinn **Magn til reikningsfærslu** í hverri þjónustulínu í þjónustubeiðnunum áður en þær eru bókaðar. Bent er á að ekki er hægt að búa til reikning fyrir eitthvað sem ekki er afhent. Það er, áður en hægt er að gefa út reikning verður að skrá afhendingu eða velja að afhenda og stofna reikning á sama tíma.  

Að bókun lokinni er hægt að skoða bókuð þjónustuskjöl í samsvarandi gluggum **Bókuð þjónustuafhending** og **Bókaður þjónustureikningur**. Bókaðar færslur sem búnar hafa verið til er hægt að sjá í ýmsum gluggum með bókuðum færslum, svo sem **Fjárhagsfærslur**, **Birgðafærslur**, **Vöruhúsafærslur**, **Þjónustufærslur**, **Verkfærslur** og **Ábyrgðarfærslur**.  

## <a name="to-view-information-about-a-posted-service-document"></a>Viðbótarupplýsingar um bókuð þjónustuskjöl skoðaðar  
Þegar þjónustureikningur, þjónustuafhending eða þjónustukreditreikningur er bókaður flytjast upplýsingarnar í gluggana **Bókaður þjónustureikningur**, **Bókuð þjónustuafhending** eða **Bókaður þjónustukreditreikningur**, eftir því sem við á. Ekki er hægt að færa inn, breyta eða eyða nokkru í þessum gluggum. Hægt er að prenta afhendingu, reikning eða kreditreikning í þessum gluggum.  

Eftirfarandi aðgerð notast við bókaðan þjónustureikning sem dæmi, en sama aðferðin á við bókaðar þjónustuafhendingar og bókaða kreditreikninga.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir þjónustureikningar** og velja svo viðeigandi tengil.  
2. Opna bókaða þjónustureikninginn sem á að skoða.  
3. Til að fá yfirlit yfir bókaðan reikning er valin aðgerðin **Tölfræðilegar upplýsingar**.  

    Glugginn **Upplýsingar um þjónustupöntun** opnast. Glugginn sýnir upplýsingar á borð við magn, upphæð, VSK, kostnað, framlegð og hámarksskuld viðskiptamanns fyrir bókaða fylgiskjalið.

## <a name="see-also"></a>Sjá einnig  
[Bóka þjónustupantanir](service-how-to-post-service-orders.md)   
[Stofna þjónustupantanir](service-how-to-create-service-orders.md)

