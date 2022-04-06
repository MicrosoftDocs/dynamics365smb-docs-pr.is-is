---
title: Stofna fastáætlaða framleiðslupöntun og breyta henni
description: Walkthrough fyrir framleiðslustjólögu á contoso Coffee sem vill búa til fastáætlaða framleiðslupöntun og breyta henni síðan.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 7a057e144ed6825435c62f565eeaaa73974fedf9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524219"
---
# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Walkthrough: stofna fastáætlaða framleiðslupöntun og breyta henni

Í þessari grein tökum við á móti þér leiðbeiningar til að nota contoso kaffi sýnigögnin til að vinna með framleiðslupantanir.  

## <a name="scenario"></a>Aðstæður

Eduardo, framleiðsluskipuleggjandi á contoso Coffee, verður að stofna nýja framleiðslupöntun fyrir 10 eininga vöru **SP-SCM1009, Airpot** sem verður að vera á gjalddaga 28. apríl. Hann afturvirkar tímaáætlun þessa og staðfestir að hann geti byrjað pöntun þann 27. apríl.  

Stuttu eftir að hann lýkur þessu verkefni er hann beðinn um að hækka pöntunina í 50 einingar. Þegar hann gerir þetta er afturvirk röðunarvirkni sem ýtir á upphafsdagsetningu pöntunar of snemma. Svo hann framsenda áætlun frá 23 apríl til þess að ákvarða raunhæfan lokadagsetningu.  

## <a name="steps"></a>Skref

1. Stofnið upphaflegu framleiðslupöntunina fyrir 10 einingar af vörunni **SP-SCM1009, Airpot**.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **fastáætlaða** framleiðslupöntun og veljið síðan tengda tengilinn.  

    2. **Velja nýju** aðgerðina og síðan eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Gildi:  |
        |---------|---------|
        |**Tegund uppruna** |Vara|
        |**Upprunnr.** |SP-SCM1009|
        |**Magn** |10|
        |**Gjalddaga**|Apríl 28  |

    3. **Velja aðgerðina Endurnýja framleiðslupöntun**.  

    4. **Á síðunni Endurnýja framleiðslupöntun** er tekið við öllum sjálfgildi og síðan er **hnappurinn í lagi** valinn til að hefja ferlið.  

        Í núgildandi uppsetningu notar þetta ferli afturvirkt röðun. Í nýju línunni í framleiðslupöntuninni er Upphafsdagsetningin 26 apríl.  

2. Breyið magni framleiðslupöntunarinnar í 50 einingar og tímasetja pöntunina.  

    1. **Í línunum** **í framleiðsluuppskriftinni** er valin Nýlega bætt lína og í **reitnum Magn** er fært inn *50*.  

3. **Velja aðgerðina Endurnýja framleiðslupöntun**.  

    Upphafsdagsetningunni hefur nú verið ýtt aftur í apríl 20. Þetta er ekki viðunandi dagsetning fyrir Eduardo.

4. Ræsa framvirkt röðun fyrir framleiðslupöntunina.

    1. **Á flipanum áætlun** er reiturinn Upphafsdagsetning **stilltur** á til *23* apríl.

    Byrjað verður til leygardagin nú 25 apríl og Lokadagsetningin er 2 maí. Gjalddagi fyrir pöntunina er settur einum degi síðar, 3 maí. Eduardo veit nú að það mun taka til maí 3 til að skila auknu pöntuninni.

> [!NOTE]
> Ef pöntun er röðunin á upphafs-eða lokadagsetningu þarf ekki að gera keyrsluna Endurnýja framleiðslupöntun **vegna þess að** allar dagsetningar endurreikast sjálfkrafa.

Nýja framleiðslupöntunin er nú sett upp og eru kröfur Eduardo uppfylltar.  

## <a name="see-also"></a>Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
