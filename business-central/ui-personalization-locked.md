---
title: Af hverju er síða læst og því ekki hægt að sérsníða hana
description: Lokað gæti verið á frá sérsníða síðu. Lestu hér um hvað þú getur gert til að aflæsa því þannig að þú getir aðlagað það.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.search.form: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 503ff89fd1e1c5c40b55929f80ce390d1a5fc307
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655437"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Af hverju er síða læst og því ekki hægt að sérsníða hana

Það eru tvö skilyrði sem koma í veg fyrir að þú sérsníðir síðu. Annað hvort er síðan læst (eins og ![með því að sérsníða læsa).](media/personalization-lock-icon.png "Sérstilla lás") teikn eða það er læst (eins og ![lokað er fyrir sérsnið.](media/personalization-blocked-icon.png "Sérstilling útilokuð") tákninu).

## <a name="locked-from-personalizing"></a>Læst fyrir sérstillingar

Ef til staðar er ![Persónuleikalæsing.](media/personalization-lock-icon.png "Sérstilla lás") Táknið í **Sérsníða** fylgiritið þegar þú opnar síðu, þú ert að koma í veg fyrir að þú gerir einhverjar sérstillingar breytingar á síðunni.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Ástæðurnar geta verið tvær:

1. Síðan var búin að sérsníða síðuna áður en hún var búin til með eldri útgáfu af vörunni. Við breyttum því hvernig sérstilling virkar frá því að þú sérstilltir síðuna síðast. Því miður er gamla leiðin og ný leið að gera hlutina ekki að virka saman.

2. Þar til núna, hefur þú aðeins notað bogalínu [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til að sérsníða síðuna.

### <a name="unlocking-the-page"></a>Síða aflæst

Ef þú vilt taka síðu úr lás og halda áfram að sérstilla hana skaltu velja táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") og síðan aðgerðina **Taka úr lás**.  

> [!CAUTION]
> Núverandi sérstilling á síðunni verður hreinsuð. Síðan fer aftur í upprunalegt skipulag og þá hefst allt frá grunni.  

## <a name="blocked-from-personalizing"></a>Lokað fyrir sérstillingar

Ef lokað ![er á teikn sérsniðar](media/personalization-blocked-icon.png "Sérstilling útilokuð") í **sérsniði** fylgibreytu er lokað fyrir þig með því að gera sérstillingar á síðunni.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Ástæðan er sú að hlutverkamiðstöð eða hlutverk sem nú tengist notandareikning breytir þessari síðu sérstaklega fyrir hlutverk þitt. Hafðu samband við stjórnanda til að fá aðstoð. Að öðrum kosti skal reyna að skipta yfir í Mitt hlutverk sem inniheldur hlutverkaleik fyrir þessa síðu. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

## <a name="see-also"></a>Sjá einnig

[Sérstilling verksvæðis](ui-personalization-user.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
