---
title: Afbrigði
description: Walkwith til að fá upplýsingar um hvernig uppfæra á eftirspurnarspá fyrir hvert afbrigði af afurð í Viðskiptamiðinu.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 86b70b3caf1896804ffdc3c76610ffe10ae73c5c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524203"
---
# <a name="walkthrough-variants"></a>Walkthrough: afbrigði

Í þessari grein tökum við á móti þér leiðbeiningar til að nota contoso Coffee sýnigögnin til að fræðast um afbrigði.

## <a name="scenario"></a>Aðstæður

Þú ert framleiðslustjósinn í contoso Coffee. Uppfæra verður eftirspurnarspá fyrir hvert afbrigði af vöru SP-SCM1006, AutoDripLite. Þar sem þeir eru með mismunandi liti verður að ganga úr skugga um að rétt uppskrift sé notuð fyrir hvert afbrigði. Keyrið áætlunarvinnublaðið til að reikna framboðið.  

## <a name="steps"></a>Skref

1. Setja upp birgðahaldseiningar fyrir vöru SP-SCM1006, AutoDripLite. Úthlutið UPPSKRIFT fyrir birgðaafbrigði rautt og HVÍTT.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn *atriði* og veljið síðan tengda tengilinn.  

    2. Opnið vöru **SP-SCM1006, AutoDripLite**.

    3. Valið er **Stofna birgðahaldseining** aðgerð.  

    4. **Stilla stofna á** svæði til *birgðageymslu & afbrigði*.

    5. Setja þarf afmörkun fyrir staðsetningu til *norðurs* og velja **síðan OK** hnappinn.

    6. **Velja birgðahaldseiningar** aðgerðar.  

    7. Uppfæra framl. uppskriftir fyrir eftirtaldar birgðahaldseiningar:

        1. RAUÐUR að NORÐAN, stilltur SP-SCM1006-RAUÐUR  

        2. HVÍTT á Norður, sett SP-SCM1006-HVÍTT  

        3. Geymið framl. UPPSKRIFT nr. tóm til SVART á Norður  

2. Uppfæra uppsetningu framleiðslu og virða eftirspurnarspár fyrir staðsetningar og afbrigði.  

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn *uppsetningu* framleiðslu og veljið síðan tengda tengilinn.  

    2. Skipta á **notkunarspánni í birgðageymslusvæði**.

    3. Rof á **svæðinu nota spá um afbrigði**.

    4. Glugganum Uppsetning **framleiðslu er** lokað.

3. Stofna nýja mánaðarlega eftirspurnarspá, *autodrip*. Sía það eftir vöru SP-SCM1006 og staðsetning NORÐAR. Stilla eftirspurn í maí fyrir hvert afbrigði. 

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn *eftirspurnarspá* og veljið síðan tengda tengilinn.

    2. Stofnið nýja eftirspurnarspá með heitinu *autodrip*.

    3. **Veljið aðgerðina Breyta eftirspurnarspá**.

    4. **Í yfirliti eftir** svæði skal velja *mánuð*.

    5. Í reitnum Vöruafmörkun **er** valið *SP-SCM1006*

    6. Skipta á **notkunarspánni í birgðageymslusvæði**.

    7. **Í reitnum Birgðageymsluafmörkun** er valið *Norður*.

    8. Rof á **svæðinu nota spá um afbrigði**.

    9. Fyrir hverja línu uppfærð gildi í maí-dálknum

        1. RAUÐKA NORÐURSINS, sett 100

        2. HVÍTÁ á NORÐFIRÐI, sett 200

        3. SVARTÁ í NORÐRI, sett 300

    10. Gluggar í loka eftirspurnarspá

4. Keyra MPS Plan í maí fyrir stofnaðar eftirspurnarspár. Skoða íhluti til að sjá það að vara málning tengist afbrigði.

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn *Áætlunarblað* og veljið síðan tengda tengilinn.

    2. Velja **Reikna áætlun endurgerðar** aðgerðina.

    3. Skiptið yfir á **MPS** -reitinn.

    4. Skiptu yfir á **MPS** -reitinn.

    5. **Í reitnum Upphafsdagsetning** er valið *May, 1*

    6. **Í reitinn Lokadagsetning** er valið *May, 31*

    7. **Í svæðinu nota spá** skal velja *autodrip*

    8. **Veldu OK** aðgerðina.

    9. Fyrir hverja stofnaða línu skal velja **íhluti** aðgerðar og skoða hvaða málning er notuð.  

## <a name="see-also"></a>Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
