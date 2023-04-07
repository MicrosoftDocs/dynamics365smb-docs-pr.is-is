---
title: Setja upp fyrirtæki sem á að samstilla aðalgögn
description: Lærðu að setja upp eitt eða fleiri fyrirtæki til að samstilla aðalgögn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Fá tilbúinn til að samstilla aðalgögn

Þegar um er að ræða tvö eða fleiri fyrirtæki sem nota a.m.k. einhver af sömu aðalgögnunum er hægt að vista tíma til að færa inn gögn með því að samstilla það í fyrirtækjunum. Samstillingargögn eru sérstaklega gagnleg þegar verið er að setja upp ný dótturfyrirtæki.

Aðalgögn eru með stillingar og ótransactional upplýsingar um viðskiptaeiningar, eins og viðskiptamenn, lánardrottna, vörur og starfsmenn. Gögnin veita samhengi fyrir viðskiptafærslur. Eftirfarandi eru örfá dæmi um aðalgögn fyrir viðskiptavin:

* Nafn
* Auðkennisnúmer
* Aðsetur
* Greiðsluskilmálar
* Lánamark

Samstilling er sett upp í dótturfyrirtækjunum. Með því að nota togalíkan draga dótturfélög þau gögn frá upprunafélaginu sem þau þurfa að gera í viðskiptum við þau. Þegar búið er að setja upp samstillingu og samstilla gögn í fyrsta sinn eru öll sett. Færslur í töflunum eru miðaðar og vinnsluraðarfærslur hefjast strax við uppfærslu gagna í dótturfyrirtækjum þegar einhver gerir breytingu á upprunafélaginu.

## Uni-stefnumiðuð samstilling aðeins

Aðeins er hægt að samstilla gögn frá upprunafélaginu til dótturfyrirtækja í togtísku. Dótturfélag má ekki ýta gögnum til upprunafélagsins.

> [!NOTE]
> Þó að það sé hægt þá mælum við ekki með því að sett sé upp samtalen bi-stefnumarkandi samstilling. Þ.e. samstillingu gagna frá upprunafélaginu til dótturfélags og frá dótturfélagi til frumfyrirtækis. Samstilling gagna í báðar áttir getur leitt til árekstra eða óæskilegra skrifla.

## Verður að byrja fyrir

Þetta eru kröfur um uppsetningu samstillingar.

* Öll fyrirtæki þurfa að vera í sama umhverfi.
* Notandinn sem setur upp dótturfyrirtækið verður að hafa  **aðalgögnin Mgt.-Skoða**  heimildasafn. Heimild sett er fyrir hendi í iðgjöldum og nauðsynlegum leyfum. Leyfisveitandi Team meðlim leyfishafa er einhver aðgangur en ekki breyta færslum svo ekki er hægt að nota það til að setja upp samstillinguna.

## Tilgreinið upprunafélagið

Fyrstu skrefin eru að tilgreina fyrirtæki sem verður gagnagjafi og virkjar samstillingu. Dótturfyrirtæki með draga gögn úr upprunafélaginu.

1. Í dótturfyrirtæki skal velja þá  ![ljósaperu sem opnar aðgerðina segja mér upp](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa inn  **uppsetningu** á aðalgagnateikni og velja síðan tengda tengilinn.
1.  **Í reitnum Upprunafélagið**  skal tilgreina fyrirtækið sem á að draga breytingar úr.
1. Kveikja á Virkja skipta á  **samstillingu** .
1. Veldu  **í lagi** í staðfestingarglugganum. [!INCLUDE [prod_short](includes/prod_short.md)] finnur töflurnar og svæðin sem eru tiltæk frá upprunafélaginu.

Næsta skref er að gera töflur og svæði virk fyrir samstillingu.

## Gera töflur og svæði virk eða óvirk

Til að spara tíma,  [!INCLUDE [prod_short](includes/prod_short.md)]  gefur upp lista yfir töflur sem fyrirtæki samstilla oft. Sjálfgefið er að þessar töflur séu virkar fyrir samstillingu en hægt er að breyta, gera óvirkar eða eyða þeim eins og þú sérð. Sem viðbót við tíma-Saver eru sum svæði á töflunum þegar óvirk vegna þess að þau eiga líklega ekki við um dótturfyrirtæki.

> [!NOTE]
> Ef einn eða fleiri Viðaukar eru settir upp í upprunafélaginu þegar dótturfyrirtæki setur upp samstillingu á  **síðunni samstillingartöflur**  eru töflur úr viðaukunum og aðgangur að svæðum þeirra. Hins vegar ef Upprunafyrirtækið bætir við framlengingu eftir að samstilling hefur verið sett upp verður hvert dótturfyrirtæki að bæta töflunum handvirkt við. Til að fá frekari upplýsingar um að bæta við töflum er farið að  [Bæta við eða eyða töflum af listanum](#add-or-delete-tables-from-the-synchronization-tables-list) samstillingartöflur. Til að fræðast meira um víkinga  [!INCLUDE [prod_short](includes/prod_short.md)] er farið í að  [þróa viðauka í  Visual Studio  kóða](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **uppsetningu** á aðalgagnateikni og velja síðan tengda tengilinn.
1. Velja skal  **aðgerðina Samstillingartöflur** .
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
>  **Töfluafmörkunarreiturinn**  er hjálplegur til að stýra því hvað á að samstilla töflu. Hægt er að setja afmarkanir til að samstilla aðeins þegar tiltekin skilyrði eru uppfyllt. Til dæmis er hægt að bæta við síum sem tilgreina að aðeins Lánardrottnar séu samstilltir á ákveðnu svæði. Eða, viðskiptamenn sem nota ákveðinn gjaldmiðil.
>
> Ef dótturfyrirtæki er þegar með gögn í töflum sínum er önnur góð leið til að setja skilyrði fyrir samstillingu að setja upp samsvörun byggða á grunni. Til að fræðast meira um samsvörun er farið í  [samsvörunarjöfnun samkvæmt](#use-match-based-coupling) notkun.

1. Til að virkja svæði fyrir töflu, veljið töfluna og veljið  **svo svæðaðgerðina** .
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Fljótleg leið til að gera mörg svæði virk eða óvirk á sama tíma er að velja þau í listanum og nota síðan annað hvort  **Aðgerðir til að virkja**  eða  **slökkva**  á þeim.

### Nota sambyggða festingu

Hægt er að tilgreina gögnin sem á að samstilla fyrir töflu með samsvarandi færslum sem byggðar eru á skilyrðum. Á uppsetningarsíðu  **Aðalgagnabanka er valin aðgerð sem**  byggir  **á samsvörun til að opna**  síðuna velja afsláttarskilyrði  **.**  Hægt er að tilgreina eftirfarandi skilyrði fyrir samsvarandi:

* Hvort samstilla eigi eftir par-færslum.
* Hvort stofna eigi nýja færslu í dótturfélaginu ef hægt er að finna einstaka, óblandanlega samsvörun með því að nota skilyrðin. Ef virkja á þennan möguleika er kveikt á  **Create nýtt ef ekki næst að finna Samsvörandi**  aðgerð.
* Svæðin sem á að nota til að jafna færslur og hvort samsvörun sé Stafrétt.
* Forgangsraða í hvaða röð færslurnar eru leitar með því að tilgreina forgang sem samsvara. [!INCLUDE [prod_short](includes/prod_short.md)] mun leita að samsvörun í hækkandi röð sem byggist á forgangi forgangs. Autt gildi jafngildir forgangi 0, sem er mesti Forgangur. Reitir með 0 forgang eru fyrst teknir til greina.

## Samstilla í fyrsta sinn

Þegar það er tilbúið, á  **uppsetningarsíðu**  aðalstjórnunar, skal velja  **aðgerðina hefja upphaflega samstillingu** .  **Á síðunni upphaflegar samstillingarupplýsingar**  er valin gerð samstillingar sem nota á fyrir hverja töflu.

* Ef færslur eru bæði í uppruna-og dótturfyrirtækjunum og eiga að samsvara færslum sem fyrir eru skal velja Afsláttaraðgerðina  **sem**  byggir á notkun. [!INCLUDE [prod_short](includes/prod_short.md)] mun stemma við færslur í dótturfélaginu með færslum í upprunafélaginu á grundvelli samsvarandi skilyrða sem skilgreindar eru. Fyrir sevaral-sjálfgefnar töflur  [!INCLUDE [prod_short](includes/prod_short.md)]  hefur þegar jafnað fyrirliggjandi færslur með aðallykli þeirra en hægt er að breyta því ef þess er óskað. Einnig er hægt að láta samstillinguna stofna nýjar færslur í dótturfyrirtæki fyrir færslur í upprunafyrirtækinu sem dótturfyrirtækið er ekki með. Til að fræðast meira um samsvörun er farið í  [samsvörunarjöfnun samkvæmt](#use-match-based-coupling) notkun.
*  **Ef keyra á fulla samstillingu** stofnar Samstillingin nýjar færslur í upprunafélaginu sem eru ekki afsláttarsamt. Yfirleitt er þessi valkostur gagnlegur ef dótturfyrirtækið er ekki með nein gögn í töflunni eða vill bara bæta við færslum frá upprunafélaginu án þess að það sé samsvarandi.  

Þegar valið er að nota er byrjað á því  **að velja aðgerðina ræsa** .

Meðan samstilling er í  **gangi birtist dálkur vinnslustöðu**  á  **aðalgögnum upphafssamstillingarsíða**, staða hverrar færslu í vinnslu vinnslunnar. Ýttu  **á F5**  á lyklaborðinu til að uppfæra stöðuna.

> [!TIP]
> Samstilla töflur í ákveðinni röð. Ef samstilling er föst á töflu skal velja töfluna og velja  **síðan endurræsa**  aðgerð til að fá hana í gangi.

Til að fá aðgang að upplýsingum, s.s. fjölda færslna sem eru settar inn eða breytt, skaltu velja gildið í  **dálkinum staða**  vinnslu til að opna  **síðuna Skoða samstillingu** . Fyrir færslur sem settar voru inn er hægt að velja númerið í dálkinum innsettur  **·**  til að fá aðgang að frekari upplýsingum um nýju færslurnar.

## Bæta við eða eyða töflum úr listanum samstillingartöflur

### Bæta við töflu

> [!IMPORTANT]
> Þó að töflur sem innihalda Transactional Data séu tiltækar á listanum, til dæmis töflur sem innihalda færslur, ætti ekki að velja þær. Samstilling virkar aðeins fyrir töflur sem innihalda ekki Transactional gögn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **samstillingartöflur** og veljið síðan tengda tengilinn.
1. Velja  **skal nýtt** og velja síðan töfluna sem á að bæta við.
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### Eyða töflu

> [!NOTE]
> Ef færslu í upprunafyrirtæki er eytt er henni ekki einnig eytt í dótturfélaginu. Þetta hjálpar til við að fyrirbyggja óumbeðnum gagnatap. Dótturfyrirtækið getur ákveðið að eyða töflunni ef þau vilja.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **samstillingartöflur** og veljið síðan tengda tengilinn.
1. Velja skal aðgerðina **Eyða**.

## Nota útflutning og innflutning til að samnýta samstillingaruppsetningu

Ef verið er að setja upp mörg dótturfyrirtæki sem nota sömu, eða svipaðar Samstillingarstillingar, er hægt að spara tíma með því að setja upp eitt dótturfyrirtæki og flytja það síðan út og út úr uppsetningu á. XML-skrá. Í skránni er allt skipulag, þar á meðal Tafla og svæðvarpanir og síuskilyrði. Síðan er hægt að flytja skrána í næsta dótturfyrirtæki. Til að flytja inn eða út uppsetningu er uppsetningaraðgerðum á  **Aðalgagnatstjórnunum**  beitt til að nota  **innflutnings**  -eða  **útflutningsaðgerðir** .

## Sjá einnig

[Stjórna samstillingu aðalgagna](admin-sync-master-data.md)