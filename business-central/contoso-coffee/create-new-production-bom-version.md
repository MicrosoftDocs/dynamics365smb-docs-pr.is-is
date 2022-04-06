---
title: Stofna nýja framl. UPPSKRIFT og UPPSKRIFTARÚTGÁFU
description: Walkof til að læra hvernig á að bæta öðrum kaffibaunum saman við vörulínu contoso Coffee í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 3c631e0285e0fdc6db5bf70cd0f5167741f602f9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524196"
---
# <a name="walkthrough-create-a-new-production-bom-and-bom-version"></a>Walkthrough: Búa til nýja framl. UPPSKRIFT og uppskriftarútgáfu

Í þessari grein tökum við á móti þér leiðbeiningar til að nota contoso kaffi sýnigögnin til að vinna með uppskriftir í framleiðsluferlum.  

## <a name="scenario"></a>Aðstæður

Contoso Coffee hefur ákveðið að bæta öðrum kaffibaunum við vörulínuna sína: **SP-SCM1008 Airpot Lite**. Þessi kaffivél er eins og sú sem til er í vöru **SP-SCM1009 Airpot**, nema að hún inniheldur ekki hlýjan disk, **SP-BOM1104**. Í aðskildu skrefi er on/Off ljósið, **SP-BOM1106** fjarlægt fyrir útgáfu af Airpot Lite uppskriftinni.

Oscar, vinnsluverkfræðingur hjá Contoso Coffee, verður að setja upp nýja framleiðsluuppskrift til að skilgreina upphafskröfur íhluta fyrir Airpot Læsi. Hann verður þá að setja upp nýja uppskriftarútgáfu, með upphafsdegi 01. júlí, til að samræma við frekari áætlanir um að gefa út aðra útgáfu.

## <a name="steps"></a>Skref

1. Búa til nýja framl. UPPSKRIFT fyrir Airpot Lite.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **framl. uppskrift** og veljið síðan tengda tengilinn.  

    2. **Velja nýju** aðgerðina og síðan eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Nr.** |SP-SCM1008|
        |**Lýsing** |Airpot Lite|
        |**Mælieiningarkóti**|STYKKI  |

2. Afrita uppskriftaríhluti úr framleiðsluuppskrift **SP-SCM1009**.

    1. Velja skal **aðgerðina AFRITA uppskrift**.

    2. **Á síðunni framl uppskriftir** er hægt að velja línuna **SP-SCM1009, airpot** og velja **síðan OK** hnappinn.

3. Breyttu íhlutunum fyrir nýju framleiðsluuppskriftina eins og lýst er í atburðarásinni.

    1. **Á vöruflipanum línur** er valin lína fyrir vöruna **SP-BOM1104** og síðan er **valið aðgerðin eyða línu**.  

4. Lögð fram nýja UPPSKRIFTIN.  

    1. **Í reitinn Staða** skal velja *Vottað*.  

5. Stofnið framleiðsluuppskriftarútgáfu fyrir Airpot Læsi.

    1. **Veljið útgáfuaðgerðina**.

    2. **Á listasíðu** framl. uppskriftarútgáfunnar er valin **aðgerðin** og reitirnir síðan fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Kóði útgáfu** |02|
        |**Lýsing** |Airpot Lite, v2|
        |**Mælieiningarkóti**|STYKKI  |  
        |**Upphafsdagsetning**|Júlí 01  |  

6. Afrita íhlutalínur úr framleiðsluuppskriftinni í nýju UPPSKRIFTARÚTGÁFUNA.

    1. **Veljið aðgerðina AFRITA uppskrift** og veljið **svo Já** -hnappinn til að afrita ÍHLUTI úr upprunalegu framleiðsluuppskriftinni.

7. Fjarlægið vöruna **SP-BOM1106, kveikt/slökkt á ljósinu** frá útgáfuþáttunum.

8. Lögð fram ný UPPSKRIFTAÚTGÁFA.

    1. **Í reitinn Staða** skal velja *Vottað*.  

    2. Loka UPPSKRIFTAÚTGÁFUNNI

Nýja kaffiframleiðandann er nú sett upp sem framleiðsluuppskrift með einni útgáfu.  

## <a name="see-also"></a>Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
