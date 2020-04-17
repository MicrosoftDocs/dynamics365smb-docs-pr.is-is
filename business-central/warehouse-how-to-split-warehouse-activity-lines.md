---
title: Hvernig á að skipta vöruhúsaaðgerðalínum | Microsoft Docs
description: Í vöruhúsafrágöngum, hreyfingum eða tínslum og í birgðafrágöngum og birgðatínslum eru lögð til hólf fyrir frágang eða tínslu vara. Raunmagnið kann að vera ónægilegt eða ekki er nægilegt rými í hólfinu sem er lagt til til að ganga frá tilskyldu magni. Þá þarf að skipta línunni svo að vörur í einni línu séu teknar úr eða settar í fleiri en eitt hólf.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c6d4f6926389215745124183406940fa24b00db9
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196092"
---
# <a name="split-warehouse-activity-lines"></a>Skipta aðgerðalínum vöruhúss
Í vöruhúsafrágöngum, hreyfingum eða tínslum og í birgðafrágöngum og birgðatínslum eru lögð til hólf fyrir frágang eða tínslu vara. Raunmagnið kann að vera ónægilegt eða ekki er nægilegt rými í hólfinu sem er lagt til til að ganga frá tilskyldu magni. Þá þarf að skipta línunni svo að vörur í einni línu séu teknar úr eða settar í fleiri en eitt hólf.  

Eftirfarandi ferli á við öll vöruhúsaskjöl, s. s. frágangur í vöruhúsi, tilfærsla, og tínslulínur, eða frágangur birgða, tilfærsla og tínslulínur.  

## <a name="to-split-warehouse-activity-lines"></a>Til að skipta vöruhúsaaðgerðalínum  
1.  Opna vöruhúsaaðgerðalínu þar sem þú ert að reyna að meðhöndla ófullnægjandi magn.  
2.  Í reitnum **Magn til afgreiðslu** er fært inn minnkað magn sem mögulegt er að meðhöndla.  
3.  Á flýtiflipanum **Línur** skal velja aðgerðina **Aðgerðir**, velja aðgerðina **Aðgerðir** og loks velja aðgerðina **Skipta línu**. Ný lína birtist, eins og sú upphaflega, nema að reiturinn **Magn til afgreiðslu** er með magninu sem var fjarlægt úr upphaflegu línunni.  
4.  Réttu hólfi (og svæði ef notaður er beinn frágangur og tínsla) er úthlutað á þessa línu eða haldið áfram að skipta línunni eftir þörfum þar til fundist hafa rétt hólf fyrir allt magnið.  

> [!NOTE]  
>  Ef ef notaður er beinn frágangur og tínsla og línunum er skipt þarf notandinn að hafa þekkingu á vöruhúsinu og geta valið hólf sem hentar geymsluþörfum vörunnar og sem uppfyllir almennar kröfur í vöruhúsaskjalinu. Til dæmis ætti ekki að skipta upp línu á tínsluskjali og setja sumar vörur í magngeymslu.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
