---
title: Skilja fjárhag og bókhaldslykil
description: Lýsir fjárhag, bókhaldslyklum og lykiltegundum. Notaðu síðu fjárhagsuppsetningar til að tilgreina meðhöndlun bókhaldsvandamála í fyrirtækinu.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 08/23/2022
ms.author: edupont
ms.openlocfilehash: 1d246e342d286e75da5aacaf1e6a305c5d0559e4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534643"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Skilningur á fjárhag og bókhaldslyklum

Fjárhagsbókhald geymir Fjárhagsleg gögn þín. Bókhaldslyklinum sýnir reikningana sem fjárhagsfærslur eru bókaðar á. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Fjárhagsgrunnur og Almenn bókunaruppsetning

Uppsetning aðalbókarinnar er kjarninn í fjárhagslegum ferlum vegna þess að það skilgreinir hvernig þú sendir gögn. Tvær síður gegna mikilvægu hlut í skilgreiningu á fjármálaferlum:  

* Á **síðu fjárhagsuppsetningarsíðunnar**

  Á síðunni **Uppsetning aðalbókarinnar** tilgreinir þú hvernig á að meðhöndla tiltekin reikningsskilaboð í fyrirtækinu þínu, svo sem:  

  * Sléttunarnákvæmni reikninga  
  * Snið aðseturs  
  * Fjárhagsskýrslugerð  

  > [!TIP]
  > Síðan **Fjárhagsgrunnur** innheldur almenn svæði og svæði sem eiga sérstaklega við um heimaland þitt eða svæði. Ef þú ert ekki viss um merkingu reits mælum við með því að þú hafir samband við endurskoðandann þinn til að ákvarða hvort hann skiptir máli fyrir fyrirtækið þitt. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Opnaðu síðuna [hér](https://businesscentral.dynamics.com/?page=118)
* **Síðan Almenn bókunaruppsetning**

    Á sama hátt er á síðunni **Almennur bókunargrunnur** tilgreint hvernig á að setja upp samsetningar almennra viðskiptabókunarflokka og almenna vörubókunarflokka. Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Ein lína er fyllt út fyrir hverja samsetningu viðskiptabókunarflokks og vörubókunarflokks. En einnig er hægt að opna hverja línu á eigin bókunaruppsetningarspjaldi. Nánari upplýsingar eru í [Uppsetning bókunarflokka](finance-posting-groups.md).  

    > [!TIP]
    > Ef ekki er hægt að sjá svæðin sem leitað er að á **síðunni almennar bókunaruppsetningar** þá er lárétt Skrunrein notuð neðst á síðunni til að fletta til hægri.  

    Opnaðu síðuna [hér](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Bókhaldslykilinn

Skýringin á reikningum sýnir allar almennar bókhaldsreikningar. Úr bókhaldslyklinum geturðu gert hluti eins og:  

* Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
* Lokaðu rekstrarreikningi þínum.  
* Opna skal fjárhagsreikningskort fjárhags (Fjárhagur) til að bæta við eða breyta stillingum.  
* Sjá lista yfir pósthópa sem senda á þann reikning.
* Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning  

Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum. Til að koma í veg fyrir misræmi er ekki hægt að eyða almennum fjárhagslykli ef gögn þess eru notuð í bókhaldslyklum. Til að koma í veg fyrir mistök á viðkvæmum tímabilum er einnig hægt að útiloka eyðingu lykla. Sjá [Eyða reikningum](finance-setup-chart-accounts.md#delete-accounts) fyrir frekari upplýsingar.  

## <a name="account-categories"></a>Lykiltegundir

Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.  

**Síðan Flokkur** fjárhagsreikninga sýnir tegundir og undirflokka og fjárhagslykla sem er úthlutað á þá. Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.  

Þú stofnar tegundaflokk með því að draga inn aðra undirflokka undir línu á síðunni **flokkar fjárhagsreikninga**. Tegundaflokkar gera það auðvelt að fá yfirlit, því hver flokkun sýnir heildarstöðu. Til dæmis er hægt að stofna undirflokka fyrir mismunandi tegundir eigna og síðan stofna tegundaflokka fyrir fastafjármunir miðað við veltufjármunir.  

Þú getur tilgreint hvort reikningarnir í hverjum undirflokki skuli innifalinn í tilteknum tegundum skýrslna. Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.  

### <a name="example"></a>Dæmi

Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir *Reiðufé* undir *Núgildandi eignir*. Ef þú vilt stöðuyfirlitið skaltu íhuga sjóði og ávísun og fara í gegnum eftirfarandi skref:  

1. Bættu við tveimur nýjum undirflokkum:

    * Einn fyrir sjóð  
    * Einn fyrir ávísanareikninginn þinn  
2. Tilgreina skal aðra skýrslu **sjóðsreikninga** fyrir þessa undirflokka.  
3. Haltu þeim í undirflokknum **Handbært fé**.  

Næst þegar fjárhagsskemu eru mynduð birtist stöðuyfirlitið í eftirfarandi línum:

* Heildarstaða í reiðufé.
* Línur með stöðu fyrir fjársjóðsstreymi og lykil fyrir villuleit.  

> [!NOTE]
> Ef stofnaður er Fjárhagsreikningur án þess að úthluta lykiltegund, þegar reikningnum er úthlutað á bókunarflokk [!INCLUDE[prod_short](includes/prod_short.md)] úthlutar sjálfkrafa lykiltegundinni fyrir fjárhagsreikninginn fyrir reikninginn fyrir ofan lykilinn í bókhaldslyklinum. Til að taka nýja lykilinn með í fjárhagsskýrslum þarf þó að velja **aðgerðina búa til fjárhagslegar skýrslur** á **síðunni Fjárhagsflokkar** fjárhags. Einnig er hægt að opna síðuna fjárhagsreikningaspjald, tilgreina lykiltegund og endurmeta síðan fjárhagsskýrsluna.

## <a name="get-a-quick-overview"></a>Fá flýtiyfirlit

**Síðan Bókhaldslykill** birtir lykla í stigveldislista sem býður upp á hraðan aðgang að lykilupplýsingum hvers lykils. Listinn er hins vegar kyrrstæður. Ef þú ert með marga reikninga gætir þú þurft að fletta til að skoða mismunandi lykla. Ef þú vilt aðeins fá fljótlegt yfirlit yfir grunnupplýsingar, t.d. nettóbreytingar og nettóstöður, er síðan **Yfirlit bókhaldslykils** gagnleg leið til þess. Dálkaútlitið á síðunni er nú það sama og þú munt finna á **síðu bókhaldslykilsins** (þó með færri dálka) svo þú munt ekki þurfa að endurraða þér. Hægt er að víkka út eða fella stigveldisstigin til að útvíkka yfirlitið. Til að auðvelda að skipta á milli síðna þá **er yfirlitssíður** bókhaldslykils tiltæk úr **síðunni Bókhaldslykill**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Aðgangur til að stofna og breyta reikningum og reikningsflokkum

Í litlu fyrirtæki, eins og CRONUS sýnifyrirtækinu, geta flestir notendur ritstýra bókhaldslyklinum. Nema notendum með leyfi TEYMISMEÐLIM. Stærri stofnanir nota hins vegar yfirleitt hlutverk og heimildir til að takmarka aðgang að ritfærslulyklum. Ef þú ert kerfisstjóri, eða ert með **hlutverk Viðskiptastjóra** eða **endurskoðanda**, getur þú stýrt notendaleyfi til að veita réttum einstaklingum aðgang að viðkomandi töflum. Frekari upplýsingar er að finna í [Að fá yfirlit yfir leyfi notanda](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)  
[Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md)  
[Viðskiptaupplýsingar](bi.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
