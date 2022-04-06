---
title: Reikna út áfyllingu hólfs
description: Þegar birgðageymslan er sett upp þannig að hún noti beinan frágang og tínslu er forgangsröðun frágangssniðmátsins tekið með í reikninginn þegar verið er að ganga frá móttökum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 7315, 7351
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7495ddfae4a6a59caba08c0d40d97f5b9c5f0c85
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518654"
---
# <a name="calculate-bin-replenishment"></a>Reikna út áfyllingu hólfs
Þegar birgðageymslan er sett upp þannig að hún noti beinan frágang og tínslu er forgangsröðun frágangssniðmátsins tekið með í reikninginn þegar verið er að ganga frá móttökum. Á meðal forgangsatriða eru fast lágmarks- og hámarksmagn tiltekins hólfs og hólfaflokkanir. Því fyllist á mest notuðu hólfin eftir því sem þau tæmast ef vörur berast jafnt og þétt.  

En birgðir berast ekki alltaf í jöfnum skömmtum. Stundum eru vörur keyptar í miklu magni til að fá afslátt eða þá að framleitt er mikið í einu til að lækka einingarkostnað. Þá berast vörurnar ekki aftur í vöruhúsið í nokkurn tíma og færa þarf vörur með reglulegu millibili í tínsluhólf úr geymslusvæðum.  

Einnig getur verið að von sé á nýjum birgðum og tæma eigi geymslusvæðið áður en nýju vörurnar koma.  

Að lokum, hafi geymsluhólfin aðeins verið skilgreind fyrir **frágang** þ.e. tegund hólfanna er ekki með valda aðgerðina **Tína** þarf alltaf að hafa tínsluhólfin full þar sem ekki er ráðlagt að vörur séu tíndar úr hólfum sem eru bara fyrir frágang.  

## <a name="to-replenish-pick-bins"></a>Fyllt á tínsluhólf  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað hreyfingar** og velja síðan viðkomandi tengil.  
2.  Velja skal aðgerðina **Reikna áfyllingu hólfs** til að opna síður skýrslubeiðna.  
3.  Beiðnisíða keyrslunnar er fyllt út til að takmarka umfang áfyllingartillagna sem verða reiknaðar. Til dæmis gæti átt að leggja áherslu á tilteknar vörur, svæði eða hólf.  
4.  Velja hnappinn **Í lagi**. Línur eru stofnaðar fyrir áfyllingarhreyfingar sem þarf að framkvæma reglum sem settar hafa verið upp fyrir hólfin og innihald hólfa, þ.e. vörur í hólfum.  
5.  Eigi að framkvæma allar áfyllingar sem lagðar eru til skal velja aðgerðina **Stofna hreyfingu**. Starfsmenn geta nú fundið leiðbeiningar í valmyndaratriðinu **Hreyfingar**, fylgt þeim og skráð þær.  
6.  Eigi aðeins að framkvæma sumar af tillögunum skal eyða línunum sem skipta minna máli og stofna síðan hreyfingu.  

Næst þegar áfylling hólfa er reiknuð verða tillögurnar sem eytt er stofnaðar aftur ef þær eiga enn við á þeim tíma.  

> [!NOTE]  
>  Ef eftirfarandi skilyrðum er fullnægt vegna vöru:  
>   
>  -   Varan er fyrningadagsett, og  
> -   Reiturinn **Tína eftir FEFO** í birgðageymsluspjaldinu er valinn og  
> -   Aðgerðin **Reikna út áfyllingu hólfs** er notuð  
>   
>  þá verða **Frá-svæði** og **Frá-hólf** reitirnir auðir vegna þess að reiknisögnin sem notuð er til að reikna hvaðan á að færa vörurnar er aðeins virkjuð þegar aðgerðin **Stofna hreyfingu** er ræst.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Tínsla eftir FEFO](warehouse-picking-by-fefo.md)  
[Birgðir](inventory-manage-inventory.md)  
[Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md) 
[samsetningarstýring](assembly-assemble-items.md)
[hönnunar upplýsingar: vöruhúsastjórnun](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]