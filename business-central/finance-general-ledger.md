---
title: Skilja fjárhag og bókhaldslykil
description: Lýsir fjárhag, bókhaldslyklum og reikningsflokkum. Notaðu síðu fjárhagsuppsetningar til að tilgreina meðhöndlun bókhaldsvandamála í fyrirtækinu.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: bb94f725c57f538f9d8704ba66e3d66e120d41d2
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079143"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Skilningur á fjárhag og bókhaldslyklum

Fjárhagur geymir fjárhagsgögn,  og bókhaldslykill birtir reikningana sem allar fjárhagsfærslur eru bókaðar í. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.

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

Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum. Til að koma í veg fyrir misræmi er ekki hægt að eyða almennum fjárhagslykli ef gögn þess eru notuð í bókhaldslyklum. Einnig að byrja með 2022 út bylgju 2, einnig er hægt að útiloka eyðingu lykla á viðkvæmum tímabilum. Sjá [Eyða reikningum](finance-setup-chart-accounts.md#delete-accounts) fyrir frekari upplýsingar.  

## <a name="account-categories"></a>Lykiltegundir

Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.  

**Síðan Flokkur** fjárhagsreikninga sýnir tegundir og undirflokka og fjárhagslykla sem er úthlutað á þá. Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.  

Þú stofnar tegundaflokk með því að draga inn aðra undirflokka undir línu á síðunni **flokkar fjárhagsreikninga**. Það gerir það auðveldara fyrir þig að fá yfirlit, því hver flokkur sýnir heildarstöðu. Til dæmis er hægt að stofna undirflokka fyrir mismunandi tegundir eigna og síðan stofna tegundaflokka fyrir fastafjármunir miðað við veltufjármunir.  

Þú getur tilgreint hvort reikningarnir í hverjum undirflokki skuli innifalinn í tilteknum tegundum skýrslna. Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.  

### <a name="example"></a>Dæmi

Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir *Reiðufé* undir *Núgildandi eignir*. Ef þú vilt stöðuyfirlitið skaltu íhuga sjóði og ávísun og fara í gegnum eftirfarandi skref:  

1. Bættu við tveimur nýjum undirflokkum:

    * Einn fyrir sjóð  
    * Einn fyrir ávísanareikninginn þinn  
2. Tilgreina skal annars staðgreiðslureikninga **annarrar skýrsluskilgreiningar** fyrir þessa undirflokka.  
3. Haltu þeim í undirflokknum **Handbært fé**.  

Í næsta skipti sem þú stofnar reikningaskipta birtist efnahagsreikningur þín í heildarjöfnuði fyrir peninga og tvær línur með jafnvægi fyrir smáskatta og eftirlitsreikning.  

## <a name="get-a-quick-overview"></a>Fá flýtiyfirlit

**Síðan Bókhaldslykill** birtir lykla í stigveldislista sem býður upp á hraðan aðgang að lykilupplýsingum hvers lykils. Listinn er þó kyrrstæður og ef um marga reikninga er að ræða gæti þurft að gera dálítið af rollu til að skoða upplýsingar fyrir ólíka lykla. Ef þú vilt aðeins fá fljótlegt yfirlit yfir grunnupplýsingar, t.d. nettóbreytingar og nettóstöður, er síðan **Yfirlit bókhaldslykils** gagnleg leið til þess. Dálkaútlitið á síðunni er nú það sama og þú munt finna á **síðu bókhaldslykilsins** (það eru bara færri af þeim) svo þú munt ekki þurfa að endurraða þér og þú getur stækkað eða fellt stigveldi til að þjappa yfirlitið. Til að auðvelda að skipta á milli síðna þá **er yfirlitssíður** bókhaldslykils tiltæk úr **síðunni Bókhaldslykill**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Aðgangur til að stofna og breyta reikningum og reikningsflokkum

Í litlu fyrirtæki eins og CRONUS sýnifyrirtækinu geta flestir notendur breytt bókhaldslyklum nema notendur með TEAM MEMBER-leyfi. Í stærri samtökum takmarkast aðgangur að breytingum á bókhaldslyklum hinsvegar eftir hlutverkum og heimildum. Ef þú ert stjórnandi eða hefur hlutverkið *Viðskiptastjórnandi* eða *Endurskoðandi* getur þú athugað heimildir allra notenda til að tryggja að réttir aðilar hafi aðgang að viðeigandi töflum. Frekari upplýsingar er að finna í [Að fá yfirlit yfir leyfi notanda](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)  
[Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md)  
[Viðskiptaupplýsingar](bi.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
