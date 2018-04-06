---
title: "Hvernig á að endurskipuleggja vöruhús | Microsoft Docs"
description: "Hugsanlega þarf að endurskipuleggja vöruhúsið með nýjum hólfakótum og hólfaeinkennum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d2820513ec95c43464979effd85d5113359886ef
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="restructure-warehouses"></a>Endurskipulagning vöruhúsa
Hugsanlega þarf að endurskipuleggja vöruhúsið með nýjum hólfakótum og hólfaeinkennum. Ekki er ráðist í þess háttar aðgerðir oft en þær aðstæður geta komið upp að endurflokkun sé nauðsynleg til þess að ná fram eða viðhalda skilvirkni. Dæmi:  

- Skipta þarf í hólfakóta sem styðja notkun sjálfvirkar gagnatöku, til dæmis með handtölvum.  
- Keypt hefur verið nýtt hillukerfi í vöruhúsið sem býður nýja möguleika við geymslu á vörum.  
- Fyrirtækið gæti hafa breytt vöruúrvali sínu og flutt sjálft vöruhúsið á nýjan stað til að bregðast við þessum breytingum.  

Ef vöruhúsið er sett upp fyrir hólf en ekki beinan frágang og tínslu skal endurskipuleggja vöruhúsið með því að búa til nú hólf sem nota á í framtíðinni.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a>Til að endurskipuleggja einfalt vöruhús sem notar aðeins hólf  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.  
2.  Á flýtiflipanum **Vöruhús** skal stilla reitinn **Sjálfgefið hólfaval** á **Síðast notaða hólf**.  
3.  Allt innihald hólfanna sem til eru fyrir er flutt í nýju hólfin sem stofnuð voru.  

    1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vöruendurflokkunarbók** og velja svo viðeigandi tengil.  
    2.  Veldu færslubókarlínu og svo **Sækja innihald hólfs** aðgerð.  
    3.  Á flýtiflipanum **Innihald hólfs** stillið afmarkanir í reitunum **Kóti birgðageymslu**, **Hólfkóti** og **Vörunr.** til að tilgreina efni sem á að færa.  
    4.  Velja **Í lagi** til að fylla út færslubókarlínu.  
    5.  Í reitnum **Nýr hólfkóti** er valið hólfið sem færa á vörurnar í.  
    6.  Endurtaka skal skref b til e fyrir allt hólfainnihald sem á að færa.  
    7.  Valið er **Bóka** aðgerðin.  

Nú hafa hólf verið tæmd þar sem vörur voru. Sjálfgefnu hólfin fyrir vörurnar eru nú nýju hólfin í færslubókarlínunum.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a>Til að endurskipuleggja ítarvöruhús sem notar stýrðan frágang og tínslu  

1.  Nýju hólfin sem nota á í framtíðinni eru stofnuð. Frekari upplýsingar eru í [Stofna hólf](warehouse-how-to-create-individual-bins.md).  
2.  Allt innihald hólfanna sem til eru fyrir er flutt í nýju hólfin sem stofnuð voru.  

    1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vöruhús endurflokkunarbók** og velja svo viðeigandi tengil.  
    2.  Fyrir hólf þar sem engin raunveruleg hreyfing er á vörum skal stofna eina línu fyrir hvert hólf sem til er fyrir í **Endurflokkunarbók vöruhúss** með gamla hólfakótanum **Kóti frá-hólfs** og nýja hólfakótanum **Kóti til-hólfs**.  
    3.  Feli hreyfingar í sér raunverulega tilfærslu sem starfsmenn eiga að framkvæma skal nota **Hreyfingavinnublöð** til að útbúa hreyfingaleiðbeiningar í stað þess að nota Vöruh.endurflokkunarbókina. Frekari upplýsingar eru í [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Þegar gömlu hólfin eru tæmd skal endurflokka þau sem hólf af gerðinni **GE** til að tryggja að þau séu ekki höfð með í vöruflæðum.  

    1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.  
    2.  Velja línu með birgðageymslunni og velja síðan **hólf** aðgerðina.  
    3.  Í glugganum **Hólf** í reitnum **Kóti hólfategundar**, færið inn **Utanflæðishólf** fyrir hvert eldra hólfanna sem tæmt er í skrefi 3 í fyrra ferli.  

Nú hafa hólfin verið fjarlægð úr vöruhúsaflæðinu og þær endurflokkaðar sem utanflæðishólf. Utanflæðishólf hafa engan af aðgerðareitunum í glugganum **Hólfategundir** valinn og eru því ekki tekin með í vöruflæðinu. Frekari upplýsingar eru í [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin"></a>Hólfi eytt:  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Staðsetningar** og velja svo viðeigandi tengil.  
2.  Veljið birgðageymsluna þar sem á að eyða hólfum. Velja aðgerðina **Hólf**.  
3.  Valdar eru línurnar með töflunum sem á að eyða.  
4.  Velja skal aðgerðina **Eyða**.  

Ef valinn er hnappurinn **Já** er hólfinu eytt en hólfakótinn helst sá sami í öllum vöruhúsafærslum.  

Ef endurnefna á hólf þannig að allar færslur sem tengjast hólfinu séu einnig endurnefndar þ.m.t. færslur sem innihalda hólfainnihald, aðgerðalínur vöruhúsa, skráðar aðgerðalínur vöruhúsa, vinnublaðalínur vöruhúsa, móttökulínur vöruhúsa, bókaðar móttökulínur vöruhúsa, afhendingarlínur vöruhúsa, bókaðar afhendingarlínur vöruhúsa og vöruhúsafærslur er hægt að gera það í glugganum **Hólf**.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a>Hólf endurnefnt og hólfkóta breytt í öllum færslum  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.  
2.  Veljið birgðageymsluna þar sem á að endurnefna hólf eða breyta hólfakóta og veljið síðan **Hólf** aðgerðina.  
3.  Veljið hólfið sem á að breyta og færið nýjan hólfkóta í reitinn **Kóti**.  
4.  Velja hnappinn **Já**.  

> [!NOTE]  
>  Ef **Já** er valið og margar færslur tengjast þessu hólfi, t.d. ef vöruhúsaskjölum hefur ekki verið eytt lengi, getur tekið nokkurn tíma að endurnefna allar færslurnar. Ef þessi aðferð er notuð ætti því að íhuga að keyra keyrsluna **Eyða skráðum vöruh. skjölum** áður en byrjað er að endurnefna. Einnig er bent á að einu skjölin sem er eytt í þessari runuvinnslu eru frágangur, tínslur og hreyfingar.  
>   
>  Ef verið er að endurnefna móttökuhólf eða afhendingarhólf verða allar bókaðar móttökur eða afhendingar sem tengjast viðkomandi hólfi endurnefndar.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

