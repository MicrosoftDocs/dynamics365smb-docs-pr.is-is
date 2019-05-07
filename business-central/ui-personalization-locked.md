---
title: Af hverju get ég ekki sérsniðið síðu | Microsoft Docs
description: Útskýrir hvers vegna þú getur ekki sérstillt síðu og hvað þú getur gert til að opna hana svo þú getir sérsniðið hana.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "911697"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Af hverju er síða læst og því ekki hægt að sérsníða hana

Það eru tvö skilyrði sem koma í veg fyrir að þú sérsníðir síðu. Annaðhvort er blaðsíðan læst (eins og kemur fram í ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás")) eða hún er útilokuð (eins og kemur fram í ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð")).

## <a name="locked-from-personalizing"></a>Læst fyrir sérstillingar

Ef táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") í borðanum **Sérstilling** þegar síða er opnuð (eins og sýnt er) merkir það að þú getir ekki gert neinar breytingar á sérstillingu síðunnar.

![Sérstilla lás](media/personalization-locked.png "Sérstilla lás")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Það kunna að vera tvær ástæður fyrir þessu:

1. Þú hefur sérstillt síðuna áður, en það var gert með eldri útgáfu af vörunni. Við breyttum því hvernig sérstilling virkar frá því að þú sérstilltir síðuna síðast. Því miður vinnur gamla og nýja aðferðin ekki saman.

2. Hingað til hefur þú aðeins notað [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til að sérsníða síðuna.

### <a name="unlocking-the-page"></a>Síða aflæst

Ef þú vilt taka síðu úr lás og halda áfram að sérstilla hana skaltu velja ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") og síðan **Taka úr lás**.  

Áður en síða er tekin úr lás skal hafa eftirfarandi í huga:

- Núverandi sérstilling á síðunni verður hreinsuð. Síðan mun fara aftur í upprunalegt útlit og þú verður að byrja frá byrjun.

- Í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], mun síðan vera eins og hún er og verður ekki fyrir áhrifum frá nýjum breytingum sérstillinga sem gerðar eru í biðlara Business Central. Í áframhaldinu verður sérstilling í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central biðlara aðskilin að fullu hvort frá öðru.

## <a name="blocked-from-personalizing"></a>Lokað fyrir sérstillingar

Ef táknið ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") er í borðanum fyrir sérstillingu merkir það að þú getir ekki gert neinar sérstillingar á síðunni.

![Sérstilla lás](media/personalization-blocked.png "Sérstilla lás")

Ástæðan fyrir þessu er að Mitt hlutverk eða prófíll sem er sem stendur tengdur við notandareikninginn þinn breytir þessari síðu sérstaklega fyrir hlutverkið þitt. Vinsamlegast hafðu samband við stjórnandann til að fá aðstoð eða, ef eitthvað vit er í því, reyndu að skipta yfir í hlutverk (frá [**Mínar stillingar**](https://businesscentral.dynamics.com?page=9176 "Fara beint í síðuna fyrir notandastillingarnar þínar í Business Central")) sem felur í sér sérsniðið hlutverk fyrir þessa síðu.

## <a name="see-also"></a>Sjá einnig
[Sérstillingar verksvæðis](ui-personalization-manage.md)  
[Sérstillingum stjórnað](ui-personalization-manage.md)  
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
