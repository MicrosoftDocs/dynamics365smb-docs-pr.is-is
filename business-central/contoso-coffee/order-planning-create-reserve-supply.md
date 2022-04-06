---
title: Nota Pantanáætlanagerð til að stofna og taka frá framboð
description: Walkof til að læra að nota pantanáætlanagerð til að stofna nauðsynlega framleiðslupöntun fyrir framboðið í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 496eaa1fd1aa8828125018a554c701743bccd5db
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524204"
---
# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Walkthrough: Notaðu Pantanáætlanagerð til að stofna og taka frá framboð

Í þessari grein tekur þú á móti leiðbeiningum til að nota contoso kaffi sýnigögnin í Pöntunaráætlun.

## <a name="scenario"></a>Aðstæður

Þú ert framleiðslustjósinn í contoso Coffee. Hægt er að stofna framleiðslupöntun fyrir 100 einingar af vörunni **SP-SCM1009, Airpot** og ætlunin er að áætla undirsamsetningu fyrir þessa pöntun. Pöntunaráætlun er notuð til að stofna nauðsynlega framleiðslupöntun fyrir framboðið. Þar sem framleiðslupöntunin er stofnuð til að uppfylla þarfir tiltekinnar pöntunar er ákveðið að taka frálag framleiðslupöntunarinnar.  

## <a name="steps"></a>Skref

1. Stofnið nýja útgefna framleiðslupöntun fyrir 100 einingar af vöru **SP-SCM1009, Airpot**.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  

    2. **Velja nýju** aðgerðina og síðan eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Tegund uppruna** |Vara|
        |**Upprunnr.** |SP-SCM1009|
        |**Magn** |100%|
    3. **Velja aðgerðina Endurnýja framleiðslupöntun**.  

    Athugið númer útgefna framleiðslupöntunarinnar.

2. **Opnið Pöntunaráætlanagerðar** síðuna og reiknið út nýja áætlun.

    1. Veldu aðgerðina **Áætlun**.  

    2. Á síðunni **Pantanaáætlun** er smellt á **Reikna áætlun** aðgerðina.  

    3. Skrunað er niður að eftirspurnarlínu sem táknar útgefna framleiðslupöntun sem var stofnuð áður.  

    4. Útvíkkið línurnar til að skoða nákvæmar upplýsingar um eftirspurnarlínuna. Staðfestið að það sé tillaga að framleiðslupöntun sem 100 einingar af vöru 1001.  

3. Stofnið nýja framleiðslupöntun fyrir 100 einingar **BOM2000, Reservoir Assy.**, og frátaka af þessari framleiðslupöntun fyrir hönd viðkomandi yfirpöntunar.  

    1. Gátreiturinn er valinn í **reitnum taka frá** í eftirspurnarlínu fyrir 100-einingar af vöru SP-BOM2000.

    2. Velja **búa til Pantanir** aðgerð.  

    3. **Stillið pantanirnar fyrir** svæði í *virku línuna*.  

    4. **Stillið svæðið Stofna framl. röð** til að *Staðfesta áætlað*.

    5. Velja skal **OK** hnappinn til að stofna framleiðslupöntunina.

    6. **Á síðunni Pöntunaráætlun** þarf að staðfesta að eftirspurnarlínan fyrir 100 einingar af vöru 1001 sé fjarlægð.

Það er til þess að pantanáætlanagerð sé í [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="see-also"></a>Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
[Um framleiðslupantanir](../production-about-production-orders.md)  
