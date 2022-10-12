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
ms.date: 08/24/2022
ms.author: edupont
ms.openlocfilehash: a48687cb51e3708860b0d3b12b7f99a53e044f4f
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605597"
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Skilningur á fjárhag og bókhaldslyklum

Fjárhag (fjárhags-) geymir fjárhagsgögnin þín og bókhaldslykillinn (COA) sýnir reikningana sem allar fjárhagsfærslur eru bókaðar á. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Fjárhagsgrunnur og Almenn bókunaruppsetning

Uppsetning aðalbókarinnar er kjarninn í fjárhagslegum ferlum vegna þess að það skilgreinir hvernig þú sendir gögn. Tvær síður einkum gegna mikilvægu hlut í skilgreiningu á fjármálaferlum:  

* Á **síðu fjárhagsuppsetningarsíðunnar**

  Á síðunni **Uppsetning aðalbókarinnar** tilgreinir þú hvernig á að meðhöndla tiltekin reikningsskilaboð í fyrirtækinu þínu, svo sem:  

  * Sléttunarnákvæmni reikninga  
  * Snið aðseturs  
  * Fjárhagsskýrslugerð

  > [!TIP]
  > Síðan **Fjárhagsgrunnur** innheldur almenn svæði og svæði sem eiga sérstaklega við um heimaland þitt eða svæði. Ef þú ert ekki viss um merkingu reitar þá leggjum við til að þú starfi við bókhaldið til að ákvarða hvort það eigi við um fyrirtækið þitt. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Opnaðu síðuna [hér](https://businesscentral.dynamics.com/?page=118).
  
* **Síðan Almenn bókunaruppsetning**

  Á sama hátt er á síðunni **Almennur bókunargrunnur** tilgreint hvernig á að setja upp samsetningar almennra viðskiptabókunarflokka og almenna vörubókunarflokka. Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Ein lína er fyllt út fyrir hverja samsetningu viðskiptabókunarflokks og vörubókunarflokks. En einnig er hægt að opna hverja línu á eigin bókunaruppsetningarspjaldi. Frekari upplýsingar er að fá í [bókunarflokki uppsetningar](finance-posting-groups.md).  

  > [!TIP]
  > Ef þú sérð ekki reitina sem þú ert að leita að á **síðunni almennar bókunaruppsetningar** skaltu nota lárétta flettistiku neðst á síðunni til að fletta til hægri.  

  Opnaðu síðuna [hér](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Bókhaldslykilinn

Skýringin á reikningum sýnir allar almennar bókhaldsreikningar. Úr bókhaldslyklinum geturðu gert hluti eins og:  

* Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
* Lokaðu rekstrarreikningi þínum.  
* Opna skal fjárhagsreikningskort fjárhags (Fjárhagur) til að bæta við eða breyta stillingum.  
* Sjá lista yfir bókunarflokka fyrir þann lykil.
* Skoða aðskildar debet-og kreditstöður fyrir stakan lykil.

Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum. Til að koma í veg fyrir misræmi er ekki hægt að eyða almennum fjárhagslykli ef gögn þess eru notuð í bókhaldslyklum. Einnig að byrja með 2022 út bylgju 2, einnig er hægt að útiloka eyðingu lykla á viðkvæmum tímabilum. Frekari upplýsingar er [að fá í kaflanum eyðureikningar](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a>Lykiltegundir

Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.  

**Síðan Flokkur** fjárhagsreikninga sýnir tegundir og undirflokka og fjárhagsreikningana sem eru tengdir þeim. Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.  

Hægt er að stofna tegundaflokk með því að innskrá aðra undirflokka undir línu á **síðunni Fjárhagsreikningstegundir**. Tegundaflokkar gera það auðvelt að fá yfirlit þar sem hver flokkun sýnir heildarstöðu. Til dæmis er hægt að stofna undirflokka fyrir mismunandi gerðir eigna og stofna síðan tegundaflokka fyrir eignir á móti núverandi eignum.  

Hægt er að skilgreina hvort tilteknar gerðir skýrslna verða að innihalda lykla í hverri undirtegund. Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.  

### <a name="example"></a>Dæmi

Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir *Reiðufé* undir *Núgildandi eignir*. Ef efnahagsuppgjörið á að fjalla um fjárstreymi og athugun þarf að taka eftirfarandi skref:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Fjárhagsreikningstegundir** og velja síðan tengda tengilinn.
   1. Einnig er [hægt að opna síðuna hér](https://businesscentral.dynamics.com/?page=790).
2. Veldu aðgerðina **Breyta lista**.
3. Bættu við tveimur nýjum undirflokkum: einn fyrir reiðufé og einn fyrir athuginn reikning þinn:
   1. **Velja gildandi eignategund**.
   2. Valið er aðgerðin **Nýtt**.
   3. Færa skal inn undirtegundarheiti **í reitinn Lýsing**.
   4. **Á fjárhagsreikningum í tegundarsvæði** skal velja viðeigandi fjárhagsreikning.
   5. **Á svæðinu Viðbótarskýrsla** skal velja **valkostinn staðgreiðslureikningar**.
4. Haltu þeim í undirflokknum **Handbært fé**.
   1. Veljið undirflokkinn sem stofnaður er í skrefi 3.
   2. **Veljið aðgerðina Inndráttur**.
   3. **Velja aðgerðina Færa niður**.
   4. **Veljið aðgerðina Inndráttur** fyrir inndrátt undir **undirflokknum reiðufé**.

Þegar valin **er aðgerðin mynda fjárhagsskýrslur** — eða næst þegar skýrslan er mynduð, mun stöðuyfirlitið sýna eftirfarandi línur:

* Heildarstaða í reiðufé.
* Línur með stöðu fyrir fjársjóðsstreymi og lykil fyrir villuleit.  

> [!NOTE]
> Ef stofnaður er Fjárhagsreikningur án þess að úthluta lykiltegund, þegar reikningnum er úthlutað á bókunarflokk [!INCLUDE[prod_short](includes/prod_short.md)] úthlutar sjálfkrafa lykiltegundinni fyrir fjárhagsreikninginn fyrir reikninginn fyrir ofan lykilinn í bókhaldslyklinum. Til að taka nýja lykilinn með í fjárhagsskýrslum þarf þó að velja **aðgerðina búa til fjárhagslegar skýrslur** á **síðunni Fjárhagsreikningur tegunda**. Einnig er hægt að opna síðuna fjárhagsreikningaspjald, tilgreina lykiltegund og endurmeta síðan fjárhagsskýrsluna.

## <a name="get-a-quick-overview"></a>Fá flýtiyfirlit

**Síðan Bókhaldslykill** birtir lykla í stigveldislista sem býður upp á hraðan aðgang að lykilupplýsingum hvers lykils. Listinn er þó kyrrstæður og ef um marga reikninga er að ræða gæti þurft að fletta til að skoða ólíka lykla. Ef þú vilt aðeins fá fljótlegt yfirlit yfir grunnupplýsingar, t.d. nettóbreytingar og nettóstöður, er síðan **Yfirlit bókhaldslykils** gagnleg leið til þess. Dálkaútlitið á síðunni er nú það sama og þú munt finna á **síðu bókhaldslykilsins** (þó með færri dálka) svo þú munt ekki þurfa að endurraða þér. Hægt er að víkka út eða fella stigveldisstigin til að útvíkka yfirlitið. Til að auðvelda að skipta á milli síðna þá **er yfirlitssíður** bókhaldslykils tiltæk úr **síðunni Bókhaldslykill**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Aðgangur til að stofna og breyta reikningum og reikningsflokkum

Í litlu fyrirtæki, eins og CRONUS sýnifyrirtækinu, geta flestir notendur ritstýra bókhaldslyklinum, nema þeir notendur sem eru með leyfi frá teymismeðlim. Stærri stofnanir nota hins vegar yfirleitt hlutverk og heimildir til að takmarka aðgang að ritfærslulyklum. Ef þú ert kerfisstjóri, eða hefur *hlutverk Viðskiptastjóra* eða *endurskoðanda*, getur þú stjórnað notendaleyfi til að veita réttum einstaklingum aðgang að viðkomandi töflum. Frekari upplýsingar í [kaflanum til að fá yfirlit yfir heimildahluta](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions) notanda.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
