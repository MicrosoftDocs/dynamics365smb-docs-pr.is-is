---
title: Setja upp nýtt geymslurými
description: Walkof til að læra að setja upp nýja vinnustöð með getudagatali fyrir eina vakt í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: e47832b34778f1340000a87f9ac148a2ab230bcf
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524217"
---
# <a name="walkthrough-set-up-new-capacity"></a>Walkthrough: setja upp nýtt geymslurými

Í þessari grein tekur þú á móti skrefunum til að nota contoso Coffee sýnigögnin í hvernig þú stjórnar afkastagetu.  

## <a name="scenario"></a>Aðstæður

Þú ert framleiðslustjósinn í contoso Coffee. Setja þarf upp nýja vinnustöð, Prófunardeild til að bregðast við breytingum á vinnuhæð. Hin nýja vinnustöð er með eina vélaröð, prófun. Í nýjum miðstöðvum þarf að hafa getraunadagbók fyrir eina vakt frá 08:00:00. til 4:00:00 PM, mánudaga til föstudaga.  

## <a name="steps"></a>Skref

1. Setja upp vinnustöðin.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **vinnustöðvar** og veljið tengda tengilinn.  

    2. **Velja nýju** aðgerðina og síðan eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Nr.** |700|
        |**Heiti** |Prófunardeild|
        |**Kóði vinnustöðvaflokksins** |1, framleiðsludeild|
        |**Innkaupsverð**|3,25|
        |**Útreikningur kostnaðarverðs**|Tíma|
        |**Andlitsflæðiaðferð**|Handvirk|
        |**Bókunarflokkur framl. bókunar**|ENGINN VSK</br></br>Athugið að þetta val fer eftir bókhaldsuppsetningu og landi.|
        |**Mælieiningarkóti** |MÍNÚTUR|
        |**Getu** |1|
        |**Skilvirkni** |90|
        |**Kóði Verkstæðiskóða** |1|

        **Í reitnum kóti** verkstæðisreits er stilling 1 sú að ein vakt sé frá mánudegi til föstudags.

    3. Loka vinnustöðvarspjaldinu.

2. Setja upp vélarmiðstöðina.

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **vélastöðvar** og velja síðan tengda tengilinn.  

    2. **Velja nýju** aðgerðina og síðan eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Nr.** |760|
        |**Heiti** |Próf|
        |**Vinnustöðum nr.** |700, prófunardeild|
        |**Innkaupsverð**|3,25|
        |**Andlitsflæðiaðferð**|Handvirk|
        |**Bókunarflokkur framl. bókunar**|ENGINN VSK</br></br>Athugið að þetta val fer eftir bókhaldsuppsetningu og landi.|
        |**Getu** |1|
        |**Skilvirkni** |90|
    3. **Útvíkkið fastflipann Uppsetning** leiðar og í **reitnum Uppsetningartími** er fært inn *10*.  

3. Reikna út getudagatal vélastöðvarinnar.  

    1. Veljið aðgerðina **Dagatal**.  

    2. **Á síðunni dagatal** vélastöðvar, á **fastflipanum** festingar, Stillið **yfirlitið eftir** svæði til *mánaðar*.  

    3. Veljið aðgerðina **Sýna fylki**.  

    4. **Á síðunni dagatal** vélastöðvar skal velja **aðgerðina reikna**.  

    5. **Á síðunni dagatal** vélastöðvar, á **fastflipanum Valkostir**, Stillið **upphafsdag** reitsins í *janúar 01*.  

    6. Reiturinn Lokadagsetning **er** settur til 31. desember.  

    7. **Á flipanum Fastá vinnustöðvarinnar** í reitnum **Nr.** Reitinn Reitur, velja *760, prófa*.  

    8. Velja hnappinn **Í lagi**. Þegar keyrslunni lýkur svarar hann þér á **síðuna dagatal** vélastöðvar.  

    9. Velja aðgerðina **Uppfæra**.  

    10. Á línu fyrir vélastöð 760, prófun, borhola í gildið í janúar dálki.  

**Á síðunni dagatalsfærslur** eru Daglegar getufærslur í **afkastagetu (Total)** reits fyrir 480 mínútur. Þetta endurspeglar 1 8-tíma vakt hvers vinnudags fyrir sig. **Einnig sýnir afkastageta (skilvirkasta)** svæðið 432 mínútur. Þetta endurspeglar 90 prósenta skilvirknihlutfall sem úthlutað var til vélastöðvarinnar.  

## <a name="see-also"></a>Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
