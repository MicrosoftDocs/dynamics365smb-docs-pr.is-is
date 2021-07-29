---
title: Hvernig á að Reikna út áfyllingu hólfs | Microsoft Docs
description: Þegar birgðageymslan er sett upp þannig að hún noti beinan frágang og tínslu er forgangsröðun frágangssniðmátsins tekið með í reikninginn þegar verið er að ganga frá móttökum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d4987502db2d278dfe7757cd9e5a71cd516c1ca5
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443333"
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
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]