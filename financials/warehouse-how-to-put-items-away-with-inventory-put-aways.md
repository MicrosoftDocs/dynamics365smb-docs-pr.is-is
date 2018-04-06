---
title: "Hvernig á að ganga frá vörum með birgðafrágangi | Microsoft Docs"
description: "Þegar birgðageymslan er sett upp þannig að krafist sé frágangsvinnslu en ekki móttökuvinnslu skal nota fylgiskjalið **Birgðafrágangur** til að skrá og bóka frágang og afhendingarupplýsingar fyrir upprunaskjölin. Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92eae2f24daf8181e39b3d22ea23c31a9ee85347
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="put-items-away-with-inventory-put-aways"></a>Ganga frá vörum með birgðafrágangi
Þegar birgðageymslan er sett upp þannig að krafist sé frágangsvinnslu en ekki móttökuvinnslu skal nota fylgiskjalið **Birgðafrágangur** til að skrá og bóka frágang og afhendingarupplýsingar fyrir upprunaskjölin. Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslu eða samsetningapöntun þar sem úttakið er tilbúið til frágangs.  

Þú getur búið til birgðafrágang á þrjá vegu:  

- Frágangurinn er stofnaður í tveim þrepum með því að stofna fyrst vöruhúsabeiðni í upprunaskjalinu sem gefur vöruhúsinu merki um að upprunaskjalið sé tilbúið fyrir frágang.   Síðan er hægt að stofna birgðafráganginn í glugganum **Birgðafrágangur** byggt á upprunaskjalinu.  
- Frágangurinn er stofnaður í upprunaskjalinu sjálfu.  
- Hægt er að stofna birgðafrágang fyrir nokkur upprunaskjöl í einu með keyrslunni.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Til að biðja um birgðafrágang með því að gefa út upprunaskjalið
Ef um er að ræða innkaupapantanir, söluvöruskilapantanir og millifærslupantanir á innleið og samsetningapantanir er vöruhússbeiðnin stofnuð með því að gefa út pöntunina. Eftirfarandi lýsir því hvernig skal gera þetta frá innkaupapöntun.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupapantanir** og velja svo viðeigandi tengil.
2. Valin er innkaupapöntun sem á að gefa út og velja síðan aðgerðina **Gefa út**.  

    Ef um er að ræða framleiðslupantanir, er hægt að stofna vöruhúsabeiðni með því að stofna innleiðarbeiðni í útgefnu framleiðslupöntuninni.  
3.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **útgefin framleiðslupantanir** og velja svo viðeigandi tengil.  
4. Velja skal aðgerðina **Stofna vöruh.beiðni á innleið**.  

> [!NOTE]  
>  Einnig er hægt að stofna á vöruhúsabeiðni á innleið með því að gátreitinn **Stofna beiðni á innleið** þegar framleiðslupöntun er endurnýjuð. Frekari upplýsingar, sjá [Uppfæra eða enduráætla framleiðslupantanir](production-how-to-replan-refresh-production-orders.md).  

Þegar vöruhúsabeiðnin hefur verið stofnuð getur starfsmaður vöruhússins sem úthlutað er frágangi séð að upprunaskjalið er tilbúið fyrir frágang og stofnað fylgiskjal fyrir birgðafrágang.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Birgðafrágangur stofnaður á grundvelli upprunaskjals:
Nú þegar beiðnin hefur verið stofnuð getur starfsmaður vöruhússins stofnað nýja birgðafrágang á grundvelli útgefins upprunaskjals.   
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **birgðafrágangur** og velja svo viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Í reitnum **Upprunaskjal** er valin sú tegund upprunaskjalsins sem verið er að ganga frá fyrir.  
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Að öðrum kosti, skal velja **Sækja upprunaskjal** aðgerðina til að velja fylgiskjal úr lista yfir upprunaskjöl á innleið sem eru tilbúin til frágangs í birgðageymslu.  
6. Velja hnappinn **Í lagi** til að fylla út frágangslínur í samræmi við valið upprunaskjal.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Birgðafrágangur stofnaður úr upprunaskjali:  
1.  Í upprunaskjalinu, sem getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun, skal velja aðgerðina **Stofna frágang/tínslu í birgðum**.  
2. Veljið gátreitinn **Stofna birgðafrágang**.
3. Velja hnappinn **Í lagi**. Nýr birgðafrágangur er stofnaður.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Fleiri en ein birgðafrágangur stofnuð með keyrslu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stofna frágang/tínslu í birgðum** og velja svo viðeigandi tengil.  
2.  Á flýtiflipanum **Vöruhúsabeiðni** í beiðniglugganum eru reitirnir **Upprunaskjal** og **Upprunanúmer** notaðir til að afmarka eftir tilteknum gerðum fylgiskjala eða sviðum fylgiskjalanúmera.  
3.  Á flýtiflipanum **Valkostir** skal velja gátreitinn **Stofna birgðafrágang**.
4.  Velja hnappinn **Í lagi**. Tiltekinn birgðafrágangar eru stofnaðar.

## <a name="to-record-the-inventory-put-away"></a>Skrá Birgðafráganginn  
1. Opna frágangsskjal sem þegar hefur verið stofnað með því að velja það úr glugganum **Birgðafrágangur**.  
2. Í reitnum **Hólfakóði** í tfrágangslínunum, hólfið sem vörurnar þurfa að vera tíndar úr er tillaga á sjálfgefið hólf vörunnar. Hægt er að skipta um hólf í þessum glugga ef með þarf.  
3. Gengið er frá vörunum og upplýsingar um magnið sem gengið var frá færðar inn í reitinn **Magn til afgreiðslu**.

    Ef setja þarf vörur í einni línu í fleiri en eitt hólf, t.d. af því úthlutaða hólfið er fullt, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur**. Sjá [Skipta aðgerðalínum í vöruhúsi](warehouse-how-to-split-warehouse-activity-lines.md) fyrir nánari upplýsingar um að skipta línum.  
4. Þegar fráganginum er lokið skal velja aðgerðina **Bóka**.  

Í bókunarferlinu bókast móttakan (eða úttakið í framleiðslupöntunum) á upprunaskjalslínum sem gengið hefur verið frá og ef hólf eru notuð í birgðageymslunni stofnar bókunin einnig vöruhúsafærslur til að bóka magnbreytingar í hólfum.

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

