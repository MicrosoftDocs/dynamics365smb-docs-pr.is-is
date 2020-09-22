---
title: Hvernig á að bóka mörg skjöl á sama tíma | Microsoft Docs
description: Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir fjöldabókun, annaðhvort fyrir bókun án tafar eða sem til að mynda er áætluð við lok dags.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782519"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bóka mörg skjöl á sama tíma

Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir bókun án tafar eða fyrir fjöldabókun samkvæmt áætlun, svo sem við lok dags. Þetta getur komið sér vel ef aðeins yfirmaður getur bókað skjöl sem aðrir notendur hafa búið til eða til að koma í veg fyrir vandamál tengd afköstum þegar bókun er gerð á vinnutíma.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Til að bóka margar innkaupapantanir strax

Eftirfarandi ferli útskýrir hvernig á að bóka margar innkaupapantanir strax. Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.
2. Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:
3. Í reitnum **númer** skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.
4. Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.
5. Veldu **Bókun** aðgerðina og svo aðgerðina **Bóka**.
6. Velja hnappinn **Já** á staðfestingarskilaboðunum.

## <a name="to-batch-post-multiple-purchase-orders"></a>Til að runubóka marga innkaupapantanir

Eftirfarandi ferli útskýrir hvernig á að fjöldabóka innkaupapantanir. Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl þar sem aðgerðin **Fjöldabóka** er í boði.

> [!NOTE]
> Fjöldabókun á skjölum fer fram í bakgrunninum. [!INCLUDE [prodshort](includes/prodshort.md)] á netinu inniheldur sjálfgefin verk fyrir bókun í bakgrunni og fjöldabókun. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.  
2. Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:
3. Í reitnum **númer** skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.
4. Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.
5. Veldu **Bókun** aðgerðina og svo aðgerðina **Fjöldabóka**.
6. Á síðunni **Innkaupapöntun fjöldabókunar** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velja hnappinn **Í lagi**.
8. Til að skoða möguleg vandamál sem komu upp við fjöldabókun á skjölum skal opna síðuna **Skráning villuboða**.

Innkaupapöntunum verður nú bætt við valda verkraðarfærslu, sem skilgreinir hvenær skjölin eru bókuð. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

Ef valið er **PDF** í reitnum **Skýrslufrálagsgerð** verða bókaðar innkaupapantanir sem heppnuðust tiltækar í hlutanum **Skýrsluinnhólf** í hlutverkamiðstöðinni.

## <a name="see-also"></a>Sjá einnig

[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
