---
title: "Hvernig á að tína vörur með Birgðatínslu | Microsoft Docs"
description: "Ef birgðageymsla er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota birgðatínsluskjöl til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7e5d30ec5775030c523b73f90490428531f49fec
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="pick-items-with-inventory-picks"></a>Vörur tíndar með birgðatínslu
Ef birgðageymsla er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota **birgðatínslu** gluggann til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl. Upprunaskjalið á útleið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun þar sem íhlutir eru tilbúnir til tínslu.

> [!NOTE]  
> Íhluti fyrir samsetningarpöntun er ekki hægt að tína eða bóka með birgðatínslum. Nota glugganum **Birgðahreyfing** í staðinn. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

>  Ef magn sölulínu tínslu og afhendingar er sett saman í pöntunina skal fylgja nokkrum reglum við stofnun birgðatínslulína. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu”.  

Þú getur búið til birgðatínslu á þrjá vegu:  

- Stofna tínsluna í tveim þrepum með því að biðja fyrst um birgðatínslu með því að gefa út upprunaskjalið. Þetta lætur vöruhúsið vita að upprunaskjalið er tilbúið fyrir tínslu. Síðan er hægt að stofna birgðatínsluna í glugganum **Birgðatínsla** byggt á upprunaskjalinu.  
- Tínslan er stofnuð í upprunaskjalinu sjálfu.  
- Hægt er að stofna birgðatínslu fyrir nokkur upprunaskjöl í einu með keyrslunni.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Til að biðja um birgðatínslu með því að gefa út upprunaskjalið  
Fyrir sölupantanir, innkaupaskilapantanir og millifærslupantanir á útleið er vöruhússbeiðnin stofnuð með því að gefa út pöntunina. Eftirfarandi lýsir því hvernig skal gera þetta frá sölupöntun.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.
2. Valinn er sölupöntun sem á að gefa út og velja síðan aðgerðina **Gefa út**.

Hvað framleiðslupantanir ræðir er vöruhúsabeiðnin um tínslu á íhlutum stofnuð sjálfvirkt, kallað *flæði*, þegar stöðu framleiðslupöntunar er breytt í **Útgefin** eða þegar útgefna framleiðslupöntunin er stofnuð. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md).

Þegar vöruhúsabeiðnin hefur verið stofnuð getur einhver sem stofnar tínslu í vöruhúsinu séð að upprunaskjalið sé tilbúið fyrir tínslu og stofnað nýtt tínsluskjal sem byggist á vöruhúsabeiðninni.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Birgðatínsla stofnaður á grundvelli upprunaskjals
Nú þegar beiðnin hefur verið stofnuð getur starfsmaður vöruhússins stofnað nýja birgðatínslu á grundvelli útgefins upprunaskjals.
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatínsla** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3. Í reitnum **Upprunaskjal** er valin sú tegund upprunaskjalsins sem verið er að tína fyrir.  
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Að öðrum kosti, skal velja **Sækja upprunaskjal** aðgerðina til að velja fylgiskjal úr lista yfir upprunaskjöl á útleið sem eru tilbúin til tínslu í birgðageymslu.  
6. Velja hnappinn **Í lagi** til að fylla út tínslulínur í samræmi við valið upprunaskjal.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Birgðatínsla stofnuð í upprunaskjali:  
1.  Í upprunaskjalinu, sem getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun, er valin aðgerðin **Stofna frágang/tínslu í birgðum**.
2.  Veljið gátreitinn **Stofna birgðatínslu**.  
3.  Velja hnappinn **Í lagi**. Ný birgðatínsla verður stofnuð.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Fleiri en ein birgðatínsla stofnuð með keyrslu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stofna frágang/tínslu í birgðum** og velja svo viðeigandi tengil.  
2.  Á flýtiflipanum **Vöruhúsabeiðni** eru reitirnir **Upprunaskjal** og **Upprunanúmer** notaðir til að afmarka eftir tilteknum gerðum fylgiskjala eða sviðum fylgiskjalanúmera. Til dæmis er hægt að stofna tínslu einungis fyrir sölupantanir.  
3. Á flýtiflipanum **Valkostir** veljið gátreitinn **Stofna birgðatínslu**.
4. Velja hnappinn **Í lagi**. Tilteknar birgðatínslur eru stofnaðar.

> [!NOTE]  
>  Ef magn sölulínu tínslu og afhendingar er sett saman í pöntunina skal fylgja nokkrum reglum við stofnun birgðatínslulína. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu”.  
>   
>  Í einfaldri vöruhúsagrunnstillingu eru vörur sem settar eru saman í sölupantanir tíndar út tengdri sölupöntun eins og útskýrt er í þessu efnisatriði. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu” í birgðatínslu.  

## <a name="to-record-the-inventory-picks"></a>Skrá Birgðatínslurnar  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatínsla** og velja svo viðeigandi tengil.  
2. í reitnum **Hólfakóði** í tínslulínunum, hólfið sem vörurnar þurfa að vera tíndar úr er tillaga á sjálfgefið hólf vörunnar. Hægt er að skipta um hólf í þessum glugga ef með þarf.  
3. Gengið er frá vörunum og upplýsingar um raunmagnið sem gengið var frá færðar inn í reitinn **Magn til afgreiðslu**.

    Ef tína þarf vörur í einni línu úr fleiri en eitt hólf, t.d. vegna þess að þau eru ekki tiltæk í útvalda hólfinu, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur**. Sjá [Skipta aðgerðalínum í vöruhúsi](warehouse-how-to-split-warehouse-activity-lines.md) fyrir nánari upplýsingar um að skipta línum.  
4. Þegar tínslunni er lokið skal velja aðgerðina **Bóka**.    

Í bókunarferlinu er afhending upprunaskjalslínanna sem hafa verið tínd bókuð eða notkun ef um er að ræða framleiðslupantanir. Ef hólf eru notuð í birgðageymslunni stofnar bókunin einnig vöruhúsafærslur til að bóka magnbreytingar í hólfum.  

## <a name="to-delete-inventory-pick-lines"></a>Til að eyða birgðatínslulínum  
Ef vörur í birgðatínslu eru ekki tiltækar er hægt að eyða þeim birgðatínslulínum eftir bókun og eyða síðan birgðatínsluskjalinu. Upprunaskjalið, til dæmis sölupöntun eða framleiðslupöntun, mun hafa eftirstandandi hluti til tínslu, sem hægt er að fá með nýrri birgðatínslu síðar þegar hlutirnir verða tiltækir.  

> [!WARNING]  
>  Þetta ferli er ekki mögulegt ef rað- og lotunúmer eru tilgreind í upprunaskjalinu. Til dæmis ef sölupöntunarlína inniheldur rað-/lotunúmer, þá verður þeirri rakningarlýsingu vöru eytt ef birgðatínslulínunni fyrir rað-/lotunúmerið er eytt.  
>   
>  Ef birgðatínslulínur hafa rað- eða lotunúmer sem ekki eru tiltæk má ekki eyða viðkomandi línum. Í staðinn skal breyta reitnum **Magn til afgreiðslu** í núll, bóka raunverulegar tínslur og eyða síðan birgðatínsluskjalinu. Þetta tryggir að hægt er að endurgera birgðatínslulínurnar fyrir þessi rað-/lotunúmer úr sölupöntuninni seinna.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun setja saman í pöntun íhluta við birgðatínslu
Glugginn **Birgðatínsla** er einnig notaður til að tína og senda vegna sölu þar sem vörur verða að vera samsettar áður en hægt er að senda þær. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Vörur sem á að afhenda eru ekki efnislega til staðar í hólfi fyrr en þær eru settar saman og bókaðar sem frálag í hólf í samsetningarsvæði. Þetta þýðir að tínsla vara sem sameina á í pöntun fyrir afhending fylgir ákveðnu flæði. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna. Bókaða birgðatínslan bókar svo samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Til að virkja þetta þarf að velja reitinn **Búa til hreyfingar sjálfvirkt** í **Uppsetning samsetningar** glugganum. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Birgðatínslulínurnar fyrir söluvörur eru stofnaðar á mismunandi hátt eftir því hvort ekkert, sumt eða allt magn sölulínunnar er sett saman í pöntun.

Í venjulegri sölu þar sem birgðatínsla er notuð til að bóka afhendingu birgðamagns, er ein birgðatínslulína búin til, eða fleiri ef varan er sett í mismunandi hólf. Þessi tínslulína grundvallast af magninu í reitnum **Magn til afhendingar**.

Í sölu með samsetningarpöntun þar sem allt magn línu sölupöntunarinnar er sett saman í pöntun er ein birgðatínslulína búin til fyrir magnið. Þetta þýðir að gildið í reitnum Magn til samsetningar er það sama og gildið í reitnum **Magn til afhendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna eru gildið í reitnum **Setja saman í pöntun hólfakóði** eða gildið í reitnum **Frá samsetningu hólfakóði**, í þeirri röð, sett inn í reitinn **Hólfakóði** í birgðatínslulínunni.

Ef enginn hólfskóði er gefinn upp í sölupöntunarlínunni og samsetningarfrálagsflæði hefur ekki verið sett upp fyrir birgðageymsluna er reiturinn **Hólfakóði** í birgðatínslulínunni er auður. Starfsmaður í vöruhúsi verður að opna gluggann **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Við blandaðar aðstæður, þar sem fyrst þarf að setja saman hluta magnsins og tína þarf annað magn úr birgðum, eru minnst tvær birgðatínslulínur búnar til. Ein tínslulína er fyrir sameiningarpöntunarmagnið. Hin tínslulínan fer eftir hvaða hólf geta uppfyllt eftirstöðvar úr birgðum. Hólfkóti á línunum tveimur er fylltur út er á mismunandi hátt eins og lýst er fyrir þessar tvær mismunandi sölutegundir. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

