---
title: Skilja fjárhag og bókhaldslykil
description: Lýsir fjárhag, bókhaldslyklum og reikningsflokkum. Notaðu síðu fjárhagsuppsetningar til að tilgreina meðhöndlun bókhaldsvandamála í fyrirtækinu.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 17, 18, 20, 21, 37, 65, 99, 118, 312, 313, 314, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: 5f168132dc747e76c514ae1bd78e8d2f86a7b609
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/01/2022
ms.locfileid: "8366736"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Skilningur á fjárhag og bókhaldslykli

Fjárhagur geymir fjárhagsgögn,  og bókhaldslykill birtir reikningana sem allar fjárhagsfærslur eru bókaðar í. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Uppsetning Uppsetning fjárhags og uppsetning almenns bókunargrunnur

Uppsetning aðalbókarinnar er kjarninn í fjárhagslegum ferlum vegna þess að það skilgreinir hvernig þú sendir gögn.  

Á síðunni **Uppsetning aðalbókarinnar** tilgreinir þú hvernig á að meðhöndla tiltekin reikningsskilaboð í fyrirtækinu þínu, svo sem:  

* Sléttunarnákvæmni reikninga  
* Snið aðseturs  
* Fjárhagsskýrslugerð  

> [!TIP]
> Síðan **Fjárhagsgrunnur** innheldur almenn svæði og svæði sem eiga sérstaklega við um heimaland þitt eða svæði. Ef þú ert ekki viss um merkingu reits mælum við með því að þú hafir samband við endurskoðandann þinn til að ákvarða hvort hann skiptir máli fyrir fyrirtækið þitt.  

Á sama hátt er á síðunni **Almennur bókunargrunnur** tilgreint hvernig á að setja upp samsetningar almennra viðskiptabókunarflokka og almenna vörubókunarflokka. Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Ein lína er fyllt út fyrir hverja samsetningu viðskiptabókunarflokks og vörubókunarflokks. En einnig er hægt að opna hverja línu á eigin bókunaruppsetningarspjaldi. Nánari upplýsingar eru í [Uppsetning bókunarflokka](finance-posting-groups.md).  

> [!TIP]
> Ef ekki er hægt að sjá reitina sem leitað er að á **síðunni Alm. bókunargrunnur** skal nota lárétta skrunreinina neðst á síðunni til að fletta til hægri.  

## <a name="the-chart-of-accounts"></a>Bókhaldslykillinn

Skýringin á reikningum sýnir allar almennar bókhaldsreikningar. Úr bókhaldslyklinum geturðu gert hluti eins og:  

* Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
* Lokaðu rekstrarreikningi þínum.  
* Opna fjárhagsreikningsspjaldið (fjárhagsreikningur) til að bæta við eða breyta stillingum.  
* Sjá lista yfir pósthópa sem senda á þann reikning.
* Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning  

Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum. Til að koma í veg fyrir misræmi geturðu þó ekki eytt almennri aðalbókareikning ef gögnin eru notuð í töflureikningi.  

## <a name="account-categories"></a>tegundir reikninga

Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.  

Síðan **Tegundir fjárhagsreikninga** sýnir flokka og undirflokka og fjárhagsreikninga sem þeim er úthlutað. Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.  

Þú stofnar tegundaflokk með því að draga inn aðra undirflokka undir línu á síðunni **flokkar fjárhagsreikninga**. Það gerir það auðveldara fyrir þig að fá yfirlit, því hver flokkur sýnir heildarstöðu. Til dæmis er hægt að stofna undirflokka fyrir mismunandi tegundir eigna og síðan stofna tegundaflokka fyrir fastafjármunir miðað við veltufjármunir.  

Þú getur tilgreint hvort reikningarnir í hverjum undirflokki skuli innifalinn í tilteknum tegundum skýrslna. Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.  

### <a name="example"></a>Dæmi

Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir *Reiðufé* undir *Núgildandi eignir*. Ef þú vilt stöðuyfirlitið skaltu íhuga sjóði og ávísun og fara í gegnum eftirfarandi skref:  

1. Bættu við tveimur nýjum undirflokkum:

    * Einn fyrir sjóð  
    * Einn fyrir ávísanareikninginn þinn  
2. Tilgreindu viðbótarskýrslugerðina **Reiðufé** fyrir þessar undirflokka.  
3. Haltu þeim í undirflokknum **Handbært fé**.  

Í næsta skipti sem þú stofnar reikningaskipta birtist efnahagsreikningur þín í heildarjöfnuði fyrir peninga og tvær línur með jafnvægi fyrir smáskatta og eftirlitsreikning.  

## <a name="getting-a-quick-overview"></a>Flýtiyfirlit sótt

Á síðu bókhaldslykla eru sýndir reikningar í stigveldislista sem býður upp á skjótan aðgang að helstu upplýsingum fyrir hvern reikning. Ekki er þó hægt að breyta listanum og ef þú ert með mikið af reikningum gætirðu þurft að fletta töluvert til að skoða upplýingar fyrir mismunandi reikninga. Ef þú vilt aðeins fá fljótlegt yfirlit yfir grunnupplýsingar, t.d. nettóbreytingar og nettóstöður, er síðan **Yfirlit bókhaldslykils** gagnleg leið til þess. Útlit dálksins á síðunni er nú það sama og er að finna á síðu bókhaldslykils (það eru bara færri dálkar) og því þarftu ekki að flakka á milli og þú getur stækkað eða fellt saman stigveldin til að þjappa saman yfirlitinu. Til að auðvelda að fara á milli síðna er síðan **Yfirlit bókhaldslykils** aðgengileg á síðu bókhaldslykils.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Aðgangur til að stofna og breyta reikningum og reikningsflokkum

Í litlu fyrirtæki eins og CRONUS sýnifyrirtækinu geta flestir notendur breytt bókhaldslyklum nema notendur með TEAM MEMBER-leyfi. Í stærri samtökum takmarkast aðgangur að breytingum á bókhaldslyklum hinsvegar eftir hlutverkum og heimildum. Ef þú ert stjórnandi eða hefur hlutverkið *Viðskiptastjórnandi* eða *Endurskoðandi* getur þú athugað heimildir allra notenda til að tryggja að réttir aðilar hafi aðgang að viðeigandi töflum. Frekari upplýsingar er að finna í [Að fá yfirlit yfir leyfi notanda](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning eða breyting á bókhaldslykli](finance-setup-chart-accounts.md)  
[Viðskiptaupplýsingar](bi.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
