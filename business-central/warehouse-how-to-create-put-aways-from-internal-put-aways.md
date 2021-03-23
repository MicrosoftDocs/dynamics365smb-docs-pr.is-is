---
title: Stofna Vöruskilapantanir innkaupa Frágangur úr innanhússfrágangi
description: Þegar gengið hefur verið frá vörum og áður en þær eru tíndar til að fylla upp í framleiðslupöntun eða afhendingu eru þær geymdar í vöruhúsinu sem hluti af tiltækum birgðum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d0f91182196aebf9b0123225603ed303cd39e66f
ms.sourcegitcommit: 026484766988b8727649c02fc8990b0646999bf1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5498613"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Tína og ganga frá án upprunaskjals
Þegar gengið hefur verið frá vörum og áður en þær eru tíndar til að fylla upp í framleiðslupöntun eða afhendingu eru þær geymdar í vöruhúsinu sem hluti af tiltækum birgðum.  

Þær aðstæður geta komið upp að taka þurfi vörur tímabundið úr tínsluhólfum vöruhússins, til dæmis til notkunar sem sýnishorn í sölukynningu. Þessar vörur eru enn í eigu fyrirtækisins og eru hluti af birgðum en eru ekki tiltæk í tínslu. Þær eru skráðar í sérstakt hólf sem stofnað er í þessum tilgangi; tæknilega eru vörurnar í vöruhúsinu en í raun gætu þær verið í fundarherbergi eða sýningarsal.  

Við aðrar aðstæður, gæti framleiðslueiningin óvænt þurft að fá nokkra hluti vegna vinnslu. Hægt er að tína vörur fyrir framleiðsluhólf með innanhússtínslunni. Þegar vinnslunni er lokið og úttak verður til er notkun vörunnar bókuð og framleiðsluhólfið tæmt sem síðan minnkar magn vörunnar í birgðageymslunni.  

Á sama hátt er hægt að skila vörum í vöruhúsið til frágangs. Varan gæti hafa verið tekin úr tiltækum birgðum og síðan aldrei notuð. Ganga verður frá þeim í hólfi til að þær verði tiltækar aftur í birgðum.  

**Innanhússfrágangar** gera þér kleift að framkvæma frágang án þess að vísa í ákveðið upprunaskjal. Auðvelt er að setja upp allar þær upplýsingar sem þarf til að stofna vöruhúsaleiðbeiningar um frágang.  

> [!NOTE]  
>  Ef ekki eru notaðar innanhússtínslur og innanhússfrágangar er hægt að gera þessar leiðréttingar með því að færa vörur úr hólfi í hólf eða að bóka magnleiðréttingar í hólfi.  
>   
>  þegar birgðageymslan notar beinan frágang og tínslu og því hólfategundir er ekki hægt að færa vörur handvirkt inn og út úr hólfi af tegundinni RECEIVE því vörur sem eru í hólfi af þeirri gerð verður að skrá sem frágengnar áður en þær verða hluti af tiltækum birgðum.  

## <a name="to-create-an-internal-pick"></a>Að búa til Innahússtínslur  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innanhústínsla vöruhúss** og veldu síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.
3. Fylla þarf út reitinn **Nr.**. reitinn **Staðsetningarkóði**, og reitinn **Kóði til-hólfs** í flýtiflipanum **Almennt**. Reiturinn **Kóði til-hólfs** tilgreinir hólfið sem staðsetja á tíndar vörur. Við framleiðslu væri þetta hólf innhólf framleiðslu eða opið búðarhólf. Annars skal velja hólfakóða með hólfi af tegund sem ekki er notuð við tínslu, oftast nær undirbúnings- eða afhendingarhólf eða hólf fyrir sérstök tilefni.  
4.  Vara er valin í reitnum **Vörunr.** og magnið sem á að tína fært inn.  
5. Veldu aðgerðina **Stofna tínslu**. Vöruhúsatínsluleiðbeiningar eru nú tilbúnar fyrir starfsmann vöruhúss. Einnig er hægt að velja aðgerðina **Losa** og stofna tiltekt í vöruhúsi með því að nota **Vinnublað tínslu**. Frekari upplýsingar má finna í [Áætla tínslu á vinnublöðum](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Stofna innanhússfrágang  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innanhússfrágangur vöruhúss** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.
3. Í haus nýja innanhússfrágangsins þarf að tilgreina að minnsta kosti **Nr.** og **Staðsetningarkóði**.
4. Fylla skal út eina línu fyrir hverja vöru sem flytja á í vöruhúsið. Aðeins þarf að fylla út í reitina **Vörunr.** og **Magn**.

  > [!NOTE]  
  > Þegar valinn er reiturinn **Vörunr.**, birtist **Innihaldslisti hólfs** í staðinn fyrir **vörulistann**. Það er vegna þess að það á að ganga frá vöru sem er í tilteknu hólfi *Innihaldi hólfs* ekki bara vöru, og þegar er vitað úr hvaða hólfi á að taka vöruna.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Til að fylla línurnar með öllu innihaldi hólfsins eða afmörkuðu innihald hólfa í birgðageymslunni, skal velja aðgerðina **Sækja hólfainnihald**.  
6. Veldu aðgerðina **Stofna frágang**. Leiðbeiningar um vöruhúsafrágang eru nú tilbúnar fyrir starfsmann vöruhúss. Einnig er hægt að velja aðgerðina **Losa** og stofna frágang í vöruhúsi með því að nota **Vinnublað frágangs**. Frekari upplýsingar má finna í [Áætla frágang á vinnublöðum](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
