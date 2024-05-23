---
title: Að skilja fjárhag og bókhaldslykil
description: 'Lýsir fjárhag og bókhaldslyklar, sem og reikningsflokkum. Notaðu síðu fjárhagsuppsetningar til að tilgreina meðhöndlun bókhaldsvandamála í fyrirtækinu.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Að skilja fjárhag og bókhaldslykil

Fjárhagurinn (fjárhagur) geymir fjárhagsgögnin og bókhaldslykillinn (COA) sýnir reikningana sem fjárhagsfærslur eru bókaðar á. [!INCLUDE[prod_short](includes/prod_short.md)] felur í sér staðlaðan bókhaldslykil sem er tilbúinn til að styðja við reksturinn.

## Uppsetning Uppsetning fjárhags og uppsetning almenns bókunargrunnur

Uppsetning aðalbókarinnar er kjarninn í fjárhagslegum ferlum vegna þess að það skilgreinir hvernig þú sendir gögn. Tvær síður gegna einkum mikilvægu hlutverki í að stilla fjármálaferli þín:  

* **Fjárhagsgrunnur**
* **Alm. bókunargrunnur**

### **Uppsetning fjárhags** síðan

Nota síðuna **Fjárhagsgrunnur** til að tilgreina hvernig fara skuli með ákveðin bókhaldsmál í fyrirtækinu, svo sem:  

* Sléttunarnákvæmni reikninga  
* Snið aðseturs  
* Fjárhagsskýrslugerð

> [!TIP]
> Síðan **Fjárhagsgrunnur** inniheldur almenna reiti og reiti sem eiga sérstaklega við um landið eða svæðið. Ef þú ert óviss um merkingu reits leggjum við til að þú vinnir með endurskoðanda þínum til að ákvarða hvort það eigi við fyrirtækið. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Til að opna síðuna núna skal nota eftirfarandi tengil [Fjárhagsgrunnur](https://businesscentral.dynamics.com/?page=118).

### Síðan **Almennur bókunargrunnur**

Nota síðuna **Alm. bókunargrunnur** til að setja upp samsetningar almennra viðskipta- og almennra vörubókunarflokka. Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Ein lína er fyllt út fyrir hverja samsetningu viðskiptabókunarflokks og vörubókunarflokks. En einnig er hægt að opna hverja línu í eigin bókunargrunnsspjaldi. Frekari upplýsingar er að finna í [Uppsetningar bókunarflokka](finance-posting-groups.md).  

> [!TIP]
> Ef þú getur ekki séð reitina sem þú leitar að á síðunni **Almennur bókunargrunnur** skaltu nota láréttu flettistikuna neðst á síðunni til að fletta til hægri.  

Til að opna síðuna núna skal nota eftirfarandi tengil [alm. bókunargrunnur](https://businesscentral.dynamics.com/?page=314).

## Bókhaldslykillinn

Síðan **Bókhaldslykill** sýnir alla fjárhagsreikninga. Úr bókhaldslyklinum geturðu gert hluti eins og:  

* Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
* Lokaðu rekstrarreikningi þínum.  
* Opnaðu fjárhagsreikningaspjaldið til að bæta við eða breyta stillingum.  
* Skoða lista yfir bókunarflokka fyrir þann aðgang.
* Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

Nánari upplýsingar er farið [í Að skilja bókhaldslykilinn](finance-chart-of-accounts.md).

## tegundir lykla

Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.  

Síðan **Fjárhagsreikningsflokkar** sýnir flokka og undirflokka og fjárhagsreikninga sem þeim er úthlutað. Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.  

Þú getur stofnað tegundaflokk með því að draga inn aðra undirflokka undir línu á síðunni **flokkar fjárhagsreikninga**. Með tegundaflokkum er auðveldara að fá yfirlit vegna þess að hver flokkun sýnir heildarstöðu. Til dæmis er hægt að stofna undirflokka fyrir mismunandi tegundir eigna og síðan stofna tegundaflokka fyrir fastafjármuni miðað við veltufjármunir.  

Þú getur skilgreint hvort tilteknar gerðir af skýrslum verði að innihalda reikninga í hverjum undirflokki. Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.  

### Dæmi

Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir *Reiðufé* undir *Núgildandi eignir*. Ef stöðuyfirlitið á að taka tillit til smágreiðslna og athugunar skal taka eftirfarandi skref:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Fjárhagsreikningsflokka** og velja síðan viðkomandi tengil.
   1. Að öðrum kosti skal [opna síðuna hér](https://businesscentral.dynamics.com/?page=790).
2. Veldu aðgerðina **Breyta lista**.
3. Bættu við tveimur nýjum undirflokkum: Einn fyrir handbært fé og einn fyrir ávísanareikning:
   1. Veldu flokkinn **Núverandi eignir**.
   2. Valið er aðgerðin **Nýtt**.
   3. Sláðu inn heiti undirflokksins í reitinn **Lýsing**.
   4. Í reitnum **Fjárhagsreikningar í flokki** skal velja viðeigandi fjárhagsreikning.
   5. Í reitnum **Frekari skýrsluskilgreining** skal velja valkostinn **Sjóðsreikningar**.
4. Haltu þeim í undirflokknum **Handbært fé**.
   1. Veldu undirflokkinn sem búinn var til í skrefi 3.
   2. Veldu aðgerðina **Inndráttur**.
   3. Veldu aðgerðina **Færa niður**.
   4. Veldu aðgerðina **Inndráttur** til að draga inn undir undirflokknum **Reiðufé**.

Þegar aðgerðin **Mynda fjárhagsskýrslu** er valin eða næst þegar skýrslan er mynduð sýna stöðuyfirlitin eftirfarandi línur:

* Heildarstaða fyrir reiðufé.
* Línur með innistæðum fyrir handbært fé og tékkareikninginn.  

> [!NOTE]
> Ef þú stofnar fjárhagsreikning án þess að úthluta reikningsflokki, þegar þú úthlutar reikninginn á bókunarflokk mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa úthluta reikningsflokknum úr fjárhagsreikningnum strax fyrir ofan reikninginn í bókhaldslyklinum þínum. Til að taka með nýja reikninginn í fjárhagsskýrslurnar þarftu hins vegar að velja aðgerðina **Búa til fjárhagsskýrslur** á síðunni **Fjárhagsreikningsflokkar**. Einnig er hægt að opna síðuna Fjárhagsspjald, tilgreina reikningsflokk og endurgera svo fjárhagsskýrsluna.

## Aðgangur að stofnun og breytingum á fjárhagsreikningum og reikningstegundum

Í litlu fyrirtæki, svo sem CRONUS sýnifyrirtækinu, geta flestir notendur ritfært fjármálaeiningar eins og fjárhagsreikninga, reikningsflokka og bókhaldslykilinn, nema þá notendur sem hafa TEAM MEMBER leyfi. Hins vegar nota stærri fyrirtæki yfirleitt hlutverk og heimildir til að takmarka aðgang að breytingum á þessum einingum. Ef þú ert stjórnandi eða ert með hlutverkið *Viðskiptastjórnandi* eða *Endurskoðandi* geturðu stjórnað heimildum notanda til að gefa rétta fólkinu aðgang að viðeigandi töflum. Nánari upplýsingar eru notaðar til að [fá yfirlit yfir heimildir](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions) notanda.  

## Nota víddir til að einfalda bókhaldslykilinn

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá. Í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað víddir sem grundvöll fyrir greiningu og forðast að þurfa að stofna flókna bókhaldslykla.

Til að fræðast meira um víddir er farið í Setja upp sjálfgefnar víddir fyrir viðskiptamenn, lánardrottna og aðra [reikninga](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## Sjá einnig .

[Skilja bókhaldslykilinn](finance-chart-of-accounts.md)  
[Vinna með víddir](finance-dimensions.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
