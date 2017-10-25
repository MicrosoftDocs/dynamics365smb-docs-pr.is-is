---
title: "Hvernig á að Stofna hólf | Microsoft Docs"
description: "Skilvirkasta leiðin til að stofna hólf í vöruhúsinu er að stofna flokka samskonar hólfa á vinnublaði hólfastofnunar, en einnig er hægt að stofna stök hólf."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 37a79ad08113b16bf0240d4c92eac6464015db07
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-bins"></a>Hvernig á að: Stofna hólf
Skilvirkasta leiðin til að stofna hólf í vöruhúsinu er að stofna flokka samskonar hólfa á vinnublaði hólfastofnunar, en einnig er hægt að stofna stök hólf frá birgðageymsluspjaldi. Einnig er hægt að nota virkni í glugganum **Hólfastofnunarvinnublaði** til að stofna hólfs sjálfvirkt.  

## <a name="to-create-a-bin-from-the-location-card"></a>Hólf stofnaða af birgðageymsluspjaldinu:  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Birgðageymslur** og velja svo viðeigandi tengil.  
2.  Veljið birgðageymsluna þaðan sem á að stofna hólfið og veljið síðan aðgerðina **Hólf**.  
3. Valið er **Nýtt** aðgerð.
4. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Stök hólf stofnuð á Hólfastofnunarvinnublaði:  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vinnublað f. stofnun hólfs** og velja svo viðeigandi tengil.  
2.  Reitirnir í hverri línu sem nauðsynlegir eru til að nefna og sérsníða hólfin sem verið er að stofna eru fylltir út.  
3.  Veldu aðgerðina **Stofna hólf**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Hólf stofnuð sjálfvirkt á vinnublaði hólfastofnunar  
Áður en byrjað er að stofna hólf sjálfvirkt ætti að skilgreina hvaða tegund af hólfum eru nauðsynleg fyrir starfsemina ásamt skilvirkasta vöruflæðinu gegnum raunskipulag vöruhússins.  

> [!NOTE]  
>  Um leið og hólf hefur verið notað er ekki hægt að eyða því nema það sé tómt. En ef á að nota annað nafnakerfi fyrir hólf er hægt að nota endurflokkunarbókina til að færa í raun vörurnar í nýja hólfakerfið. Þetta ferli er handvirkt og tímafrekt þannig að best er að setja hólfin rétt upp í upphafi.  

Til að vinna með **Hólfastofnunarvinnublaði** gluggann þarftu að vera settur upp sem starfsmaður í vöruhúsi á staðsetningunni þar sem hólfin eru. Frekari upplýsingar eru í [Hvernig á að: Setja upp starfsmenn vöruhúss](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vinnublað f. stofnun hólfs** og velja svo viðeigandi tengil.  
2.  Veldu aðgerðina **Reikna út hólf**.
3. Í glugganum **Reikna út hólf** í reitnum **Kóti hólfasniðmáts**, skal velja hólfasniðmátið sem nota á sem grunn fyrir hólfin sem á að stofna.
4.  Rituð er lýsing á hólfunum sem verið er að stofna.  
5.  Hólfakóðarnir eru stofnaðir með því að fylla út reitina **Frá nr.** og **Til nr.** í flokkunum þrem sem sýndir eru í glugganum: **Rekki**, **Geiri** og **Stig**. Hólfakótinn getur haft allt að 20 stafi.  

    > [!NOTE]  
    >  Fjöldi stafa sem færðir eru inn í flokkunum þrem fyrir hvorn reit, til dæmis stafirnir sem færðir eru inn fyrir alla þrjá reitina **Frá nr.** ásamt reitaskiltáknum, ef einhver eru, verður að vera 20 eða minni.  

     Hægt er að nota bókstafi í kóðanum sem auðkennandi samsetningu, en bókstafurinn sem notaður er verður að vera sá sami í reitunum **Frá nr.** og **Til nr.** Reitir Til dæmis væri hægt að skilgreina rekkahluta kótans sem **Frá nr. A01** og **Til nr. A10**. Kerfið er ekki sett upp til að búa til kóta með bókstafaröðum, til dæmis frá A01 til F05.  

6.  Eigi að nota tákn eins og bandstrik til að aðgreina flokkareitina sem skilgreindir hafa verið sem hluti af hólfakótanum er það tákn fært inn í reitinn **Reitaskiltákn**.  
7.  Ef kerfið á ekki að stofna línu fyrir hólf ef það er þegar til skal velja reitinn **Kanna í hólfi sem til er**.  
8. Þegar lokið hefur verið við að fylla út reitina er hnappurinn **Í lagi.** valinn.

    Kerfið stofnar línu fyrir hvert hólf á vinnublaðinu. Nú er hægt að eyða sumum hólfunum, til dæmis ef til er rekki með gönguleið gegnum fyrstu tvö stigin í nokkrum geirum.  

9. Þegar öllum óþarfa hólfum hefur verið eytt er aðgerðin **Stofna hólf** valin og þá stofnar kerfið hólf fyrir hverja línu á vinnublaðinu.  

Þetta ferli er endurtekið fyrir annan hóp hólfa þar til öll hólf í vöruhúsinu hafa verið stofnuð.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

