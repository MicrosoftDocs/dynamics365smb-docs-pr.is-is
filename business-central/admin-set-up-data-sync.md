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

# <a name="get-ready-to-synchronize-master-data" />Fá tilbúinn til að samstilla aðalgögn

Þegar tvö eða fleiri fyrirtæki nota einhver sömu aðalgögnin er hægt að samstilla gögnin frekar en bæta því handvirkt við í hverju fyrirtæki. Til dæmis er gagnlegt að samstilla gögn þegar ný dótturfyrirtæki eru sett upp.

Aðalgögn eru með stillingar og ótransactional upplýsingar um rekstrareiningar. Til dæmis viðskiptamenn, lánardrottna, vöru og starfsmenn. Gögnin veita samhengi fyrir viðskiptafærslur. Eftirfarandi eru örfá dæmi um aðalgögn fyrir viðskiptavin:

* Nafn
* Auðkennisnúmer
* Heimilisfang
* Greiðsluskilmálar
* Lánamark

Samstilling er sett upp í dótturfyrirtækjunum. Með því að nota togalíkan draga dótturfélög þau gögn frá upprunafélaginu sem þau þurfa að gera í viðskiptum við þau. Þegar búið er að setja upp samstillingu og samstilla gögn í fyrsta sinn eru öll sett. Færslur í vinnslubiðröð uppfæra afsláttarfærslur í dótturfélögum þegar einhver breytir gögnum í upprunafélaginu.

## <a name="uni-directional-synchronization-only" />Uni-stefnumiðuð samstilling aðeins

Aðeins er hægt að samstilla gögn frá upprunafélaginu til dótturfyrirtækja í togtísku. Dótturfélag má ekki ýta gögnum til upprunafélagsins.

> [!NOTE]
> Þó að það sé hægt þá mælum við ekki með því að sett sé upp samtalen bi-stefnumarkandi samstilling. Þ.e. samstillingu gagna frá upprunafélaginu til dótturfélags og frá dótturfélagi til frumfyrirtækis. Samstilling gagna í báðar áttir getur leitt til árekstra eða óæskilegra skrifla.

## <a name="before-you-start" />Verður að byrja fyrir

Eftirfarandi eru kröfur um uppsetningu samstillingar.

* Öll fyrirtæki þurfa að vera í sama umhverfi.
* Notandinn sem setur upp dótturfyrirtækið verður að hafa nauðsynleg leyfi fyrir  **,** Premium  **eða** Basic  **.** 

> [!NOTE]
> Teymismeðlimurinn og innri kerfisstjóri leyfa aðgang en ekki breyta færslum svo ekki sé hægt að nota þær til að setja upp samstillinguna. Úthlutað admin leyfi gerir þér ekki kleift að raða bakgrunnsverkum þannig að þú munt ekki geta lokið uppsetningunni.

## <a name="specify-the-source-company" />Tilgreinið upprunafélagið

Fyrstu skrefin eru að tilgreina fyrirtæki sem verður gagnagjafi og virkjar samstillingu. Dótturfyrirtæki með draga gögn úr upprunafélaginu.

1. Í dótturfyrirtæki skal velja þá  ![ljósaperu sem opnar aðgerðina segja mér upp.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **uppsetningu** á aðalgagnateikni og velja síðan tengda tengilinn.
1.  **Í reitnum Upprunafélagið**  skal tilgreina fyrirtækið sem á að draga breytingar úr.
1. Kveikja á Virkja skipta á  **samstillingu** .
1. Veldu  **í lagi** í staðfestingarglugganum. [!INCLUDE [prod_short](includes/prod_short.md)] finnur töflurnar og svæðin sem eru tiltæk frá upprunafélaginu.

Næsta skref er að gera töflur og svæði virk fyrir samstillingu.

## <a name="enable-or-disable-tables-and-fields" />Gera töflur og svæði virk eða óvirk

Til að spara tíma,  [!INCLUDE [prod_short](includes/prod_short.md)]  gefur upp lista yfir töflur sem fyrirtæki samstilla oft. Sjálfgefið er að þessar töflur séu virkjaðar fyrir samstillingu. Hægt er að breyta, gera óvirka eða eyða þeim eins og sjá má Fit. Sem aukatíma-Saver eru sum svæði á töflunum þegar óvirk vegna þess að þau eiga líklega ekki við um dótturfyrirtæki.

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

### <a name="use-match-based-coupling" />Nota sambyggða festingu

Hægt er að tilgreina gögnin sem á að samstilla fyrir töflu með samsvarandi færslum sem byggðar eru á skilyrðum. Á uppsetningarsíðu  **Aðalgagnabanka er valin aðgerð sem**  byggir  **á samsvörun til að opna**  síðuna velja afsláttarskilyrði  **.**  Hægt er að tilgreina eftirfarandi skilyrði fyrir samsvarandi:

* Hvort samstilla eigi eftir par-færslum.
* Hvort stofna eigi nýja færslu í dótturfélaginu ef hægt er að finna einstaka, óblandanlega samsvörun með því að nota skilyrðin. Ef virkja á þennan möguleika er kveikt á  **Create nýtt ef ekki næst að finna Samsvörandi**  aðgerð.
* Svæðin sem á að nota til að jafna færslur og hvort samsvörun sé Stafrétt.
* Forgangsraða í hvaða röð færslurnar eru leitar með því að tilgreina forgang sem samsvara. [!INCLUDE [prod_short](includes/prod_short.md)] mun leita að samsvörun í hækkandi röð sem byggist á forgangi forgangs. Autt gildi jafngildir forgangi 0, sem er mesti Forgangur. Reitir með 0 forgang eru fyrst teknir til greina.

## <a name="synchronize-for-the-first-time" />Samstilla í fyrsta sinn

Þegar það er tilbúið, á  **uppsetningarsíðu**  aðalstjórnunar, skal velja  **aðgerðina hefja upphaflega samstillingu** .  **Á síðunni upphaflegar samstillingarupplýsingar**  er valin gerð samstillingar sem nota á fyrir hverja töflu.

* Ef færslur eru bæði í uppruna-og dótturfyrirtækjunum og eiga að samsvara færslum sem fyrir eru skal velja Afsláttaraðgerðina  **sem**  byggir á notkun. [!INCLUDE [prod_short](includes/prod_short.md)] stemmir færslur í dótturfyrirtækið með færslum í upprunafélaginu. Samstæður eru byggðar á jöfnunarskilyrðum sem notandi skilgreinir. Fyrir margar sjálfgefnar töflur  [!INCLUDE [prod_short](includes/prod_short.md)]  hefur þegar jafnað fyrirliggjandi færslur með aðallykli þeirra en því má breyta ef þess er óskað. Einnig er hægt að láta samstillinguna stofna nýjar færslur í dótturfyrirtæki fyrir færslur í upprunafyrirtækinu sem dótturfyrirtækið er ekki með. Til að fræðast meira um samsvörun er farið í  [samsvörunarjöfnun samkvæmt](#use-match-based-coupling) notkun.
*  **Ef keyra á fulla samstillingu** stofnar samstilling nýjar færslur fyrir allar færslur í upprunafélaginu sem ekki eru enn í gangi. Þessi valkostur er til dæmis gagnlegur við eftirfarandi aðstæður:

    * Dótturfyrirtækið er ekki með gögn í töflunni.
    * Þú vilt bæta við færslum úr upprunafélaginu án þess að samsvara.  

Þegar valið er að nota er byrjað á því  **að velja aðgerðina ræsa** .

Meðan samstilling er í  **gangi birtist dálkur vinnslustöðu**  á  **aðalgögnum upphafssamstillingarsíða**, staða hverrar færslu í vinnslu vinnslunnar. Ýttu  **á F5**  á lyklaborðinu til að uppfæra stöðuna.

> [!TIP]
> Samstilla töflur í ákveðinni röð. Ef samstilling er föst á töflu skal velja töfluna og velja  **síðan endurræsa**  aðgerð til að fá hana í gangi.

Til að fá aðgang að upplýsingum, s.s. fjölda færslna sem eru settar inn eða breytt, skaltu velja gildið í  **dálkinum staða**  vinnslu til að opna  **síðuna Skoða samstillingu** . Fyrir færslur sem settar voru inn er hægt að velja númerið í dálkinum innsettur  **·**  til að fá aðgang að frekari upplýsingum um nýju færslurnar.

## <a name="add-or-delete-tables-from-the-synchronization-tables-list" />Bæta við eða eyða töflum úr listanum samstillingartöflur

### <a name="add-a-table" />Bæta við töflu

> [!IMPORTANT]
> Þó að töflur sem innihalda Transactional Data séu tiltækar á listanum, til dæmis töflur sem innihalda færslur, ætti ekki að velja þær. Samstilling virkar aðeins fyrir töflur sem innihalda ekki Transactional gögn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **samstillingartöflur** og veljið síðan tengda tengilinn.
1. Velja  **skal nýtt** og velja síðan töfluna sem á að bæta við.
1. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### <a name="delete-a-table" />Eyða töflu

> [!NOTE]
> Ef færslu í upprunafyrirtæki er eytt er henni ekki einnig eytt í dótturfélaginu. Þetta hjálpar til við að fyrirbyggja óumbeðnum gagnatap. Dótturfyrirtækið getur ákveðið að eyða töflunni ef þau vilja.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **samstillingartöflur** og veljið síðan tengda tengilinn.
1. Velja skal aðgerðina **Eyða**.

## <a name="use-export-and-import-to-share-a-synchronization-setup" />Nota útflutning og innflutning til að samnýta samstillingaruppsetningu

Ef þú ert að setja upp nokkur dótturfyrirtæki sem nota sömu eða svipaðar Samstillingarstillingar, þá er tími Bjarkar. Setja upp eitt dótturfyrirtæki og flytja það síðan út í XML-skrá. Í skránni er allt skipulag, þar á meðal Tafla og svæðvarpanir og síuskilyrði. Síðan er hægt að flytja skrána í næsta dótturfyrirtæki. Til að flytja inn eða út uppsetningu er uppsetningaraðgerðum á  **Aðalgagnatstjórnunum**  beitt til að nota  **innflutnings**  -eða  **útflutningsaðgerðir** .

## <a name="see-also" />Sjá einnig

[Stjórna samstillingu aðalgagna](admin-sync-master-data.md)
