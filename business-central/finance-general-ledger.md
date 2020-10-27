---
title: Kynntu þér fjárhag og bókhaldslykla| Microsoft Docs
description: Lýsir fjárhag og bókhaldslyklar, sem og reikningsflokkum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f370bf9bb7e6aa4571a88d4b868ff86376ecb605
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917152"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Skilja fjárhag og bókhaldslykil

Fjárhagur geymir fjárhagsgögn,  og bókhaldslykill birtir reikningana sem allar fjárhagsfærslur eru bókaðar í. [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Uppsetning Uppsetning fjárhags og uppsetning almenns bókunargrunnur

Uppsetning aðalbókarinnar er kjarninn í fjárhagslegum ferlum vegna þess að það skilgreinir hvernig þú sendir gögn.  

Á síðunni **Uppsetning aðalbókarinnar** tilgreinir þú hvernig á að meðhöndla tiltekin reikningsskilaboð í fyrirtækinu þínu, svo sem:  

* Sléttunarnákvæmni reikninga  
* Snið aðseturs  
* Fjárhagsskýrslugerð  

Á sama hátt er á síðunni **Almennur bókunargrunnur** tilgreint hvernig á að setja upp samsetningar almennra viðskiptabókunarflokka og almenna vörubókunarflokka. Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Ein lína er fyllt út fyrir hverja samsetningu viðskiptabókunarflokks og vörubókunarflokks. Nánari upplýsingar eru í [Uppsetning bókunarflokka](finance-posting-groups.md).  

> [!TIP]
> Síðan **Fjárhagsgrunnur** innheldur almenn svæði og svæði sem eiga sérstaklega við um heimaland þitt eða svæði. Ef þú ert ekki viss um merkingu reits mælum við með því að þú hafir samband við endurskoðandann þinn til að ákvarða hvort hann skiptir máli fyrir fyrirtækið þitt.  

## <a name="the-chart-of-accounts"></a>Bókhaldslykillinn

Skýringin á reikningum sýnir allar almennar bókhaldsreikningar. Úr bókhaldslyklinum geturðu gert hluti eins og:  

* Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
* Lokaðu rekstrarreikningi þínum.  
* Opnið fjárhagsreikningskortið til að bæta við eða breyta stillingum.  
* Sjá lista yfir pósthópa sem senda á þann reikning.
* Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning  

Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum. Til að koma í veg fyrir misræmi geturðu þó ekki eytt almennri aðalbókareikning ef gögnin eru notuð í töflureikningi.  

## <a name="account-categories"></a>tegundir reikninga

Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.  

Síðan **Fjárhagsreikningsflokkar** sýnir flokka og undirflokka og fjárhagsreikninga sem eru úthlutað þeim. Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.  

Þú stofnar tegundaflokk með því að draga inn aðra undirflokka undir línu á síðunni **flokkar fjárhagsreikninga** . Það gerir það auðveldara fyrir þig að fá yfirlit, því hver flokkur sýnir heildarstöðu. Til dæmis er hægt að stofna undirflokka fyrir mismunandi tegundir eigna og síðan stofna tegundaflokka fyrir fastafjármunir miðað við veltufjármunir.  

Þú getur tilgreint hvort reikningarnir í hverjum undirflokki skuli innifalinn í tilteknum tegundum skýrslna. Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.  

Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir reiðufé í eignum. Ef þú vilt jafnvægisyfirlitið skaltu íhuga smápeninga og stöðva getur þú:  

1. Bættu við tveimur nýjum undirflokkum. Einn fyrir sjóð og einn fyrir reikninginn þinn.  
2. Tilgreindu viðbótarskýrslugerðina **Reiðufé** fyrir þessar undirflokka.  
3. Haltu þeim í undirflokknum **Handbært fé** .  

Í næsta skipti sem þú stofnar reikningaskipta birtist efnahagsreikningur þín í heildarjöfnuði fyrir peninga og tvær línur með jafnvægi fyrir smáskatta og eftirlitsreikning.  

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning eða breyting á bókhaldslykli](finance-setup-chart-accounts.md)  
[Viðskiptaupplýsingar](bi.md)  
