---
title: Hvernig skal búa til frágangur úr Innra frágangur | Microsoft Docs
description: Þegar gengið hefur verið frá vörum og áður en þær eru tíndar til að fylla upp í framleiðslupöntun eða afhendingu eru þær geymdar í vöruhúsinu sem hluti af tiltækum birgðum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ad4d0a53f3a7c70ebfeecc9c513598a6ed8448c2
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881775"
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
2.  Fylla þarf út reitinn **Nr.**. reitinn og **Kóði til-hólfs** reitinn á flýtiflipanum **Almennt**. Reiturinn **Kóti til-hólfs** tilgreinir hólfið sem vörurnar eru sóttar í. Við framleiðslu væri þetta hólf innhólf framleiðslu eða opið búðarhólf. Annars skal velja Kóta til-hólfs með hólfi af tegund sem ekki er notuð við tínslu, oftast nær undirbúnings- eða afhendingarhólf eða hólf fyrir sérstök tilefni.  
3.  Vara er valin í reitnum **Vörunr.** og magnið sem á að tína fært inn.  
4. Veldu aðgerðina **Stofna tínslu**. Vöruhúsatínsluleiðbeiningar eru nú tilbúnar fyrir starfsmann vöruhúss.  

## <a name="to-create-an-internal-put-away"></a>Stofna innanhússfrágang  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innanhússfrágangur vöruhúss** og veldu síðan tengda tengilinn.  
2.  Fylla þarf út reitinn **Nr.**. og **Frá hólfakóða** reitina á flýtiflipanum **Almennt**. Reiturinn **Kóti frá-hólfs** tilgreinir hólfið þar sem vörurnar sem skila á í vöruhúsið, til dæmis úr framleiðslu, eru geymdar.  
3.  Vörunúmerin og magnið er fært inn í línurnar.  
4.  Veldu aðgerðina **Stofna frágang**. Leiðbeiningar um vöruhúsafrágang eru nú tilbúnar fyrir starfsmann vöruhúss.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
