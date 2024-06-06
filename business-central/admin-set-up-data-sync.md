---
title: Setja upp fyrirtæki til að samstilla aðalgögn
description: Læra að setja upp eitt eða fleiri fyrirtæki til að samstilla aðalgögn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Tilbúinn til að samstilla aðalgögn

Þegar tvö eða fleiri fyrirtæki nota nokkur af sömu aðalgögnum er hægt að samstilla gögnin frekar en að bæta þeim handvirkt við hvert fyrirtæki. Samstilling gagna er til dæmis gagnleg þegar verið er að setja upp ný dótturfyrirtæki.

Aðalgögn innihalda stillingar og upplýsingar sem ekki eru viðskiptalegar um viðskiptaeiningar. Til dæmis viðskiptamenn, lánardrottna, vörur og starfsmenn. Gögnin veita samhengi viðskiptafærslna. Eftirfarandi eru nokkur dæmi um aðalgögn viðskiptamanns:

* Nafn
* Kenninúmer
* Netfang
* Greiðsluskilmálar
* Hámarksskuld

Samstilling er sett upp í dótturfyrirtækjunum. Með því að nota togalíkan eru dótturfyrirtæki að draga gögnin frá upprunafyrirtækinu sem þau þurfa að eiga viðskipti við. Þegar búið er að setja upp samstillingu og samstilla gögn í fyrsta skipti eru öll stillt. Verkraðarfærslur uppfæra paraðar færslur í dótturfyrirtækjunum þegar einhver breytir gögnum í upprunafyrirtækinu.

## Eingöngu samstilling í stefnu

Aðeins er hægt að samstilla gögn frá upprunafyrirtækinu við dótturfyrirtækin á toga í tísku. Dótturfyrirtæki geta ekki ýtt gögnum til upprunafyrirtækisins.

> [!NOTE]
> Þó það sé mögulegt er ekki mælt með því að sett sé upp tvístefnusamstilling. Það er að samstilla gögn frá upprunafyrirtækinu við dótturfyrirtækin og frá dótturfyrirtækjum til upprunafyrirtækisins. Samstilling gagna í báðar áttir getur leitt til árekstra eða óumbeðinna skrifara.

## Verður að byrja fyrir

Eftirfarandi eru þarfir til að setja upp samstillingu.

* Öll fyrirtæki verða að vera í sama umhverfi.
* Notandinn sem setur upp dótturfyrirtækið verður að hafa **Essential,Premium** **eða** **Basic ISV** leyfi.

> [!NOTE]
> Meðlimur teymismeðlims og innri kerfisstjóra er hægt að opna en ekki breyta færslum svo ekki sé hægt að nota þær til að setja upp samstillinguna. Úthlutuð stjórnunarskírteini leyfir ekki tímasetningu bakgrunnsverka, svo ekki er hægt að ljúka uppsetningunni.

## Tilgreina upprunafyrirtækið

Fyrstu skrefin eru að tilgreina fyrirtækið sem verður gagnagjafinn og gera samstillingu virka. Dótturfyrirtæki draga gögn frá upprunafyrirtækinu.

> [!NOTE]
> Þegar samstilling er gerð virk stofnar [!INCLUDE [prod_short](includes/prod_short.md)]  og tímasetur verkraðarfærslur sem samstilla gögnin. Það lítur út eins og færslurnar samstilli gögnin samstundis, en það er ekki raunin. Stofnaðar verkraðarfærslur samstilla aðeins nokkrar færslur og á þessum tímapunkti hefur notandinn ekki sett það upp ennþá. Samstilling hefst eftir að [töflur og reitir og reitir eru gerðir virkir eða gerðir óvirkir](#enable-or-disable-tables-and-fields) í [fyrsta skipti](#synchronize-for-the-first-time).

1. Í dótturfyrirtæki skal velja ![Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Aðalgagnastjórnunargrunnur** og velja síðan viðeigandi tengil.
1. Í reitnum **Upprunafyrirtæki** er tilgreint fyrirtækið sem gera á breytingar frá.
1. Kveikja á **víflipunni Gera samstillingar virka** .
1. Í staðfestingarsvarglugganum skal velja **Í lagi**. [!INCLUDE [prod_short](includes/prod_short.md)] finna töflur og reiti sem eru tiltækir frá upprunafyrirtækinu.

Næsta skref er að virkja töflur og reiti fyrir samstillingu.

## Gera töflur og svæði virk eða óvirk

Til að spara tíma birtir [!INCLUDE [prod_short](includes/prod_short.md)]  listi yfir töflur sem fyrirtæki samstilla oft. Töflurnar eru sjálfgefið virkar fyrir samstillingu. Hægt er að breyta, gera þær óvirkar eða eyða þeim eftir hentugleika. Sem aukatímasparnaður eru sumir reitir í töflunum þegar óvirkir þar sem þeir eiga líklega ekki við um dótturfyrirtækið.

> [!NOTE]
> Ef einn eða fleiri viðaukar eru uppsettir í upprunafyrirtækinu, þegar dótturfyrirtæki setur upp samstillingu **á síðunni Samstillingartöflur** eru töflur úr viðbótunum og hægt er að opna reiti þeirra. Ef upprunafyrirtækið bætir við viðbót eftir að samstilling hefur verið sett upp verður hvert dótturfyrirtæki að bæta töflunum handvirkt við. Nánari upplýsingar um hvernig töflum er bætt við er farið í [Bæta við eða eyða töflum af lista](#add-or-delete-tables-from-the-synchronization-tables-list) samstillingartöflunnar. Nánari upplýsingar um framlengingu [!INCLUDE [prod_short](includes/prod_short.md)] fást með því að [fara í Þróun viðbóta í Visual Studio Kóti](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Aðalgagnastjórnunargrunnur** og velja síðan viðeigandi tengil.
1. Veljið aðgerðina **Samstillingartöflur** .
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Reiturinn **Töfluafmörkun** er gagnlegur til að stjórna því hvað á að samstilla fyrir töflu. Hægt er að setja upp afmarkanir til að samstilla aðeins þegar ákveðnum skilyrðum er fullnægt. Til dæmis er hægt að bæta við afmörkunum sem tilgreina að aðeins séu samstilltir lánardrottnar á tilteknu svæði. Eða viðskiptamenn sem nota tiltekinn gjaldmiðil.
>
> Ef dótturfyrirtækið er þegar með gögn í töflum sínum er önnur góð leið til að setja skilyrði fyrir samstillingu til að setja upp samsvörunarmiðaða festingu. Nánari upplýsingar um samsvörun fást með því að [fara í Nota samsvörunarfyrirkomulag](#use-match-based-coupling).

1. Til að virkja reiti fyrir töflu skal velja töfluna og velja svo aðgerðina **Reitir** .
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Fljótleg leið til að gera marga reiti virka eða óvirka samtímis er að velja þá á listanum og nota annaðhvort **aðgerðirnar Gera virka** eða **óvirka** .

### Nota samsvörunarmiðaða jöfnun

Hægt er að tilgreina gögnin sem á að samstilla fyrir töflu með því að samsvara færslum sem byggjast á skilyrðum. Á síðunni **Aðalgagnastjórnunargrunnur** skal velja aðgerðina **Samsvörun afsláttar** til að opna **síðuna Velja afsláttarskilyrði** . Hægt er að skilgreina eftirfarandi skilyrði fyrir samsvörun:

* Hvort samstilla eigi eftir nokkrar færslur.
* Hvort stofna eigi nýja færslu í dótturfyrirtækinu ef einstaka samsvörun er að finna með því að nota samsvörunarskilyrðin. Til að virkja þennan möguleika skal kveikja á Aðgerðin **Stofna nýja ef ekki er hægt að finna samsvörun** .
* Reitirnir sem nota á til að passa við færslur og hvort samsvörunin sé háð hástöfum.
* Forgangsraða röðinni þar sem leitað er að færslum með því að tilgreina samsvörunarforgang. [!INCLUDE [prod_short](includes/prod_short.md)] leitar að samsvörun í hækkandi röð eftir samsvörunarforgangi. Autt gildi er forgangur 0 sem er mesti forgangurinn. Reitir með 0 forgang eru fyrst teknir til greina.

## Samstilla í fyrsta skipti

Þegar notandi er tilbúinn skal velja aðgerðina Hefja samstillingu **á síðunni** Uppsetning aðalgagnastjórnunar **.**  Á síðunni **Samstilling** aðalgagna er valin sú tegund samstillingar sem á að nota fyrir hverja töflu.

* Ef þú ert þegar með færslur bæði í uppruna- og dótturfyrirtækjunum og þú vilt passa við fyrirliggjandi færslur skal velja aðgerðina **Nota samsvörunarjöfnun** . [!INCLUDE [prod_short](includes/prod_short.md)] samsvarar færslum í dótturfyrirtækinu við færslur í upprunafyrirtækinu. Samsvörunin byggist á samsvarandi skilyrðum sem notandi skilgreinir. Í nokkrum sjálfgefnum töflum [!INCLUDE [prod_short](includes/prod_short.md)]  hefur þegar verið samsvörun fyrirliggjandi færslna með því að nota aðallykil þeirra, en hægt er að breyta því ef þess er óskað. Einnig er hægt að láta samstillinguna stofna nýjar færslur í dótturfyrirtækinu fyrir færslur í upprunafyrirtækinu sem dótturfyrirtækið hefur ekki. Nánari upplýsingar um samsvörun fást með því að [fara í Nota samsvörunarfyrirkomulag](#use-match-based-coupling).
* Ef valið **er Að keyra fulla samstillingu** stofnar samstillingin nýjar færslur fyrir allar færslur í upprunafyrirtækinu sem ekki hafa verið teknar saman ennþá. Þessi valkostur er til dæmis gagnlegur í eftirfarandi tilvikum:

    * Dótturfyrirtækið hefur ekki gögn í töflunni.
    * Bæta á við færslum frá upprunafyrirtækinu án samsvörunar.  

Þegar valkosturinn sem á að nota hefur verið valinn skal velja aðgerðina **Hefja allt** til að hefja samstillinguna.

Á meðan samstilling er í gangi sýnir dálkurinn **Staða** verks á **aðalgögnum upphaflegrar fullrar samstillingar** stöðu hverrar verkraðarfærslu. Stutt er **á F5** á lyklaborðinu til að uppfæra stöðuna.

> [!TIP]
> Töflur samstilla í fyrirfram skilgreindri röð. Ef samstilling festist á töflu skal velja töfluna og velja svo aðgerðina **Endurræsa** til að fá hana aftur.

Til að fá aðgang að upplýsingum, svo sem fjölda færslna sem er sett inn eða þeim breytt, skal velja gildið í dálknum **Staða** verks til að opna **síðuna Skoða - Samstillingarsamstillingarverk** . Fyrir færslur sem settar voru inn er hægt að velja númerið í dálknum **Sett inn** til að fá aðgang að nánari upplýsingum um nýju færslurnar.

## Bæta við eða eyða töflum af lista samstillingartöflu

### Bæta við töflu

> [!IMPORTANT]
> Þó svo að töflur með færslugögnum séu tiltækar á listanum, svo sem töflur með færslum, ætti ekki að velja þær. Samstilling virkar aðeins fyrir töflur sem innihalda gögn sem ekki eru í færslum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **samstillingartöflur** og velja síðan viðeigandi tengil.
1. Velja skal **Nýtt** og velja svo töfluna sem á að bæta við.
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### Eyða töflu

> [!NOTE]
> Ef færslu er eytt í upprunafyrirtækinu er henni ekki heldur eytt í dótturfyrirtækinu. Þetta hjálpar til við að koma í veg fyrir óæskilegt gagnatap. Dótturfyrirtækið getur ákveðið að eyða töflunni ef það vill.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **samstillingartöflur** og velja síðan viðeigandi tengil.
1. Velja skal aðgerðina **Eyða**.

## Nota út- og innflutning til að samnýta samstillingaruppsetningu

Ef verið er að setja upp nokkur dótturfyrirtæki sem nota sömu eða svipaðar samstillingarstillingar þá er til tímasparnaður. Setja upp eitt dótturfyrirtæki og flytja uppsetningu þess út í .xml skrá. Skráin inniheldur alla uppsetninguna, þar á meðal töflu- og reitavörpun og afmörkunarskilyrði. Síðan er hægt að flytja skrána inn í næsta dótturfyrirtæki. Til að flytja uppsetningu inn eða út er á síðunni Aðalgagnastjórnunargrunnur **notaðu** aðgerðirnar Flytja inn **eða** út **.** 

## Sjá einnig

[Stjórna samstillingu aðalgagna](admin-sync-master-data.md)