---
title: Setja upp og vinna Úthýsingaraðgerð
description: Walkmeð til að læra hvernig setja á upp og vinna undirverktaka í Viðskiptamiðinu.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 9227abbfe25ca5a1b3c6775865712f22b31f721b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524213"
---
# <a name="set-up-and-process-a-subcontracting-operation"></a>Setja upp og vinna Úthýsingaraðgerð

Í þessari grein tekur þú á móti skrefunum til að nota contoso Coffee sýnigögnin í úthýsingu.

## <a name="scenario"></a>Aðstæður

Þú ert framleiðslustjósinn í contoso Coffee. Vegna takmarkana á afkastagetu er ætlunin að nota undirverktaka til að framleiða vöruna **SP-SCM1009, Airpot**.

Hér er stofnuð ný Útgefin framleiðslupöntun fyrir 12 eininga vöru SP-SCM1009, Airpot, með leiðara-SP-SCM1009-SUB-2. Nota skal undirvinnublaðið til að mynda innkaupapöntun fyrir framleiðsluna og ljúka aðgerðinni með því að taka við og reikningsfæra innkaupapöntunina.

## <a name="steps"></a>Skref

1. Stofnið nýja útgefna framleiðslupöntun fyrir 12 eininga vöru SP-SCM1009, Airpot.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  

    2. **Velja nýju** aðgerðina og síðan eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Tegund uppruna** |Vara|
        |**Upprunnr.** |SP-SCM1009|
        |**Magn** |100%|
    3. **Velja aðgerðina Endurnýja framleiðslupöntun**.  

2. Skipta um leið í SP-SCM1009-SUB-2 í framleiðslupöntunarlínunni og endurnýjast síðan framleiðslupöntunin aðeins fyrir leiðarkerfi.  

    1. Bæta reitnum framleiðsluleið við línurnar í útgefinni framleiðslupöntun.<!--in code, this is marked as visible=false-->

    2. **Breyta leiðarnúmeri** reits úr *SP-SCM1009-raðganga* í *SP-SCM1009-SUB-2*.  

    3. **Velja aðgerðina Endurnýja framleiðslupöntun**.  

    4. **Á beiðni um endurnýjun framleiðslupöntunar** skal hreinsa **reiti lína** og **íhluta** svo að verkið verði aðeins keyrt fyrir leiðara og velja svo hnappinn í **lagi**.

3. Nota skal undirvinnublaðið til að mynda innkaupapöntun fyrir undirverktaka-aðgerðina í framleiðslupöntuninni sem var stofnuð í skrefi 2.  

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **úthýsingu vinnublaða** og velja síðan tengda tengilinn.  

    2. **Velja aðgerðina reikna Undirsamninga**.

    3. **Velja reitinn Samþykkja aðgerðaboð** fyrir nýju línuna.

    4. Veljið aðgerðina **Framkvæma aðgerðaboð**.  

    5. **Á síðunni framkvæma aðgerðarnr. –** beiðni um boð, samþykkja öll sjálfgefin gildi og velja **síðan OK** hnappinn.

    6. Að keyrslunni lokinni skal velja hnappinn í **lagi** til að loka vinnublaði undirverktaka.  

4. Taka við og reikningsfæra innkaupapöntunina.  

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **innkaupapantanir** og velja síðan tengda tengilinn.  

    2. **Á lista innkaupapantana** er fundin innkaupapöntun úr undirverktökum lánardrottins 82000.

    3. **Í reitinn lánardrottnareikningur** er fært inn *542349*.

    4. **Á flipanum Línur** er línan valin og síðan er **reiturinn Beinn kostnaður** stilltur á *18*.

    5. Valið er **Bóka** aðgerðin.  

    6. Veldu **móttöku og reikningvalkostinn** í beiðninni.  

Úrtak vöru SP-SCM1009 Airpot er nú skráð.

## <a name="see-also"></a>Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
