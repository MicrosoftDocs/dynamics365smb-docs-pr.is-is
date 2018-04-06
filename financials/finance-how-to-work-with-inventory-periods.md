---
title: "Hvernig á að vinna með birgðatímabil | Microsoft Docs"
description: "Hægt er að stjórna tímarammanum þar sem fólk getur bókað breytingar á birgðum með því að skilgreina birgðatímabil."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f3d24dda00e3234dfcf7538c7f4fb7fbc008221
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-inventory-periods"></a>Vinna við birgðatímabil
Birgðatímabil skilgreina tímabil þar sem hægt er að bóka breytingar á birgðum. Birgðatímabil afmarkast af dagsetningunni sem því lýkur á. Þegar birgðatímabili er lokað er ekki hægt að bóka neinar breytingar á birgðum, hvorki áætluðum né reikningsfærðum fyrir þessa lokadagsetningu. Ekki er heldur hægt að bóka nein ný gildi við birgðir fyrir lokadagsetninguna. Ef birgðafærslur eru hafðar opnar í lokaða tímabilinu, sem þýðir jákvætt magn sem ekki er búið að jafna saman við færslur á útleið, er samt hægt að jafna magn á útleið við þessar færslur, jafnvel þó að tímabilið sé lokað.  

Eftirfarandi hlutar útskýra hvernig á að standa að:  

* Stofna birgðatímabil.  
* Lokun birgðatímabila.  
* Enduropna birgðatímabil.  

## <a name="to-create-an-inventory-period"></a>Til að stofna birgðatímabil  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatímabil** og velja svo viðeigandi tengil.  
2. Stofnið nýja línu.  
3. Í reitinn **Lokadagsetning** er slegin inn síðasta dagsetningin í birgðatímabilinu sem ætlunin er að skilgreina. Þegar tímabilinu er lokað verður ekki hægt að bóka breytingar á birgðum fyrir þessa dagsetningu.  
4. Færa inn lýsandi heiti í reitinn **Heiti**. Velja hnappinn **Í lagi**.  

## <a name="closing-inventory-periods"></a>Lokun birgðatímabila  
Reiturinn **Lokað** gefur til kynna hvort birgðatímabilið er lokað fyrir breytingum á birgðagildum eður ei. Ekki er hægt að breyta þessum reit.  

Hægt er að loka hvaða birgðatímabili sem er, að því gefnu að eftirfarandi sé satt:  

* Engar birgðafærslur eru opnar það er að segja ekki neikvætt birgðamagn, á því tímabili.  
* Kostnaður allra vara hefur verið leiðréttur með keyrslunni **Leiðr. kostnað - Birgðafærslur**.  

Þetta þýðir að jafna þarf allt færslumagn á útleið, eins og magnið í sölupöntunum, millifærslum á útleið, sölureikningsfærslum, vöruskilum eða innkaupakreditreikningum við magn sem er fyrir í birgðum.  

### <a name="to-close-an-inventory-period"></a>Til að loka birgðatímabili  
1. Áður en birgðatímabili er lokað er keyrslan **Leiðr. kostnað - Birgðafærslur** keyrð til að tryggja það að allar kostnaðarleiðréttingar séu bókaðar. Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Leiðrétta kostnað - Birgðafærslur**.  

     Keyrð er skýrslan **Loka birgðatímabili - Prófun** til að ákvarða hvort einhverjar opnar birgðafærslur á útleið eru innan birgðatímabilsins eða einhverjar vörur sem ekki hafa fengið kostnað sinn leiðréttan.  
2. Velja skal **Loka birgðatímabili - Prófun** aðgerðina.  

     Keyrð er keyrslan **Bóka birgðabreytingar** til að tryggja það að allur kostnaður sé bókaður í fjárhaginn.  
3. Velja skal aðgerðina **Bóka birgðir í fjárhag**.  
4. Í glugganum **Birgðatímabil** skal velja birgðatímabilið sem á að loka.  
5. Velja aðgerðina **Loka tímabili**. Þegar birgðatímabilinu hafi verið lokað er ekki hægt að bóka breytingar á birgðum fyrir lokadagsetninguna. Leiðrétta þarf kostnað allra vara með keyrslunni **Leiðr. kostnað - Birgðafærslur** áður en birgðatímabilinu er lokað.  
6. Veldu hnappinn **Já** til að staðfesta það að ætlunin sé að loka tímabilinu, eða veldu **Nei** til að hætta við lokunina.  
7. Kerfið lokar birgðatímabilinu og sýnir staðfestingarskilaboð þegar því er lokið.  

## <a name="reopening-inventory-periods"></a>Enduropnun birgðatímabila  
Þegar birgðatímabili hefur verið lokað er ekki hægt að eyða birgðatímabilinu. Hægt er hins vegar að enduropna það til að leyfa bókun áður en að lokadagsetningu birgðatímabilsins er komið. Enduropnun tímabils enduropnar líka öll birgðatímabil með lokadagsetningar seinni en það tímabil sem er enduropnað.  

### <a name="to-reopen-an-inventory-period"></a>Til að enduropna birgðatímabil  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatímabil** og velja svo viðeigandi tengil.  
2. Velja skal birgðatímabilið sem á að enduropna.  
3. Velja aðgerðina **Enduropna tímabili**. Staðfesta að það eigi að enduropna tímabilið.  
4. Allir birgðahaldstímar með lokadagsetningu sem kemur síðar en valið tímabilið eru enduropnaðir.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: birgðahaldstími](design-details-inventory-periods.md)  
[Fjármál](finance.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með Financials](ui-work-product.md)

