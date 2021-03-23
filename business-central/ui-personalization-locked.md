---
title: Af hverju get ég ekki sérsniðið síðu | Microsoft Docs
description: Útskýrir hvers vegna þú getur ekki sérstillt síðu og hvað þú getur gert til að opna hana svo þú getir sérsniðið hana.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 41b0989d388ee7ded2619136ded0a03d5830b78b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387551"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Af hverju er síða læst og því ekki hægt að sérsníða hana

Það eru tvö skilyrði sem koma í veg fyrir að þú sérsníðir síðu. Annaðhvort er síðan læst (eins og kemur fram í ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás")) tákninu eða hún er útilokuð (eins og kemur fram í ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") tákninu).

## <a name="locked-from-personalizing"></a>Læst fyrir sérstillingar

Ef táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") í borðanum **Sérstilling** þegar síða er opnuð merkir það að þú getir ekki gert neinar breytingar á sérstillingu síðunnar.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Það kunna að vera tvær ástæður fyrir þessu:

1. Þú hefur sérstillt síðuna áður, en það var gert með eldri útgáfu af vörunni. Við breyttum því hvernig sérstilling virkar frá því að þú sérstilltir síðuna síðast. Því miður vinnur gamla og nýja aðferðin ekki saman.

2. Hingað til hefur þú aðeins notað [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til að sérsníða síðuna.

### <a name="unlocking-the-page"></a>Síða aflæst

Ef þú vilt taka síðu úr lás og halda áfram að sérstilla hana skaltu velja táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") og síðan aðgerðina **Taka úr lás**.  

Áður en síða er tekin úr lás skal hafa eftirfarandi í huga:

- Núverandi sérstilling á síðunni verður hreinsuð. Síðan mun fara aftur í upprunalegt útlit og þú verður að byrja frá byrjun.

- Í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], mun síðan vera eins og hún er og verður ekki fyrir áhrifum frá nýjum breytingum sérstillinga sem gerðar eru í biðlara Business Central. Í áframhaldinu verður sérstilling í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central biðlara aðskilin að fullu hvort frá öðru.

## <a name="blocked-from-personalizing"></a>Lokað fyrir sérstillingar

Ef táknið ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") í borðanum **Sérstilling** merkir það að þú getir ekki gert neinar sérstillingar á síðunni.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

Ástæðan fyrir þessu er að Mitt hlutverk eða hlutverk sem er sem stendur tengt við notandareikninginn þinn breytir þessari síðu sérstaklega fyrir hlutverkið þitt. Hafðu samband við stjórnanda til að fá aðstoð. Að öðrum kosti skal reyna að skipta yfir í Mitt hlutverk sem inniheldur hlutverkaleik fyrir þessa síðu. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

## <a name="see-also"></a>Sjá einnig
[Sérstilling verksvæðis](ui-personalization-user.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]