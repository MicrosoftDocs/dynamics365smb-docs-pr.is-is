---
title: Úthluta tekjum og kostnaði á marga fjárhagsreikninga
description: Fræðast um hvernig á að úthluta kostnaði á einn eða fleiri reikninga í fjárhag.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Úthluta tekjum og kostnaði á marga fjárhagsreikninga

Í þessari grein er því lýst hvernig úthlutunarreikningar eru notaðir til að dreifa upphæðum í sölu- og innkaupaskjölum og færslubókarlínum í mismunandi fjárhagsreikninga. Hægt er að úthluta upphæðum með fastri eða breytilegri dreifingu.  

Úthlutun skiptir færslubókarlínu í línurnar sem skilgreindar eru á síðunni **Úthlutunarreikningur** . Ef til dæmis leigukostnaði er skipt upp með þremur leiðum með víddum verður til þrjár línur til að bóka úthlutunina. Því eru sex fjárhagslínur (eða hugsanlega fleiri ef notaður er VSK eða söluskattur). Þó svo að þetta bóki fleiri fjárhagsfærslur en þörf krefur gerir það kleift að bakfæra einstakar línur í stað þess að bakfæra alla úthlutunina.

Úthlutunarreikningar vinna einnig með frestun. Hægt er að fá nánari upplýsingar um frestun með því að [fara í Frestaðar tekjur og útgjöld](finance-how-defer-revenue-expenses.md).

Eftirfarandi tafla kynnir úthlutunaraðferðirnar sem hægt er að nota.

|Úthlutunaraðferð  |Heimildasamstæða  |
|---------|---------|
|Lagað     | Þegar skipta á upp kostnaði á þann hátt sem er endurtekinn á lengri tíma er hægt að nota fasta úthlutun. Með fastri úthlutun er hægt að skilgreina skiptingu úthlutunar. Þessi skipting breytist aðeins þegar uppsetningunni er breytt á síðunni **Úthlutunarreikningur** .        |
|Breytilegt     | Nota breytilega úthlutunaraðferð til að dreifa tekjum eða kostnaði á grundvelli virðis sem breytast með tímanum. Í breytilegum úthlutunum er hægt að tilgreina uppruna sem á að nota til að reikna úthlutunarprósentur. Þessi aðferð er til dæmis gagnleg til að skipta kostnaði starfsmanna sem lýsir mismiklum höfuðstól í deildum eða deildum. Annað dæmi er að dreifa kostnaði við leigu á grundvelli myndefnis framleiðslugólfs sem gæti verið breytilegt á hverja framleiðslulínu með tímanum. Breytilegar úthlutanir nota samsetningu vídda og talnagagnalykla til að ákvarða hvernig upphæðir skiptast á tímabil. Til að fræðast meira um tölfræðilega reikninga er farið í [Greina gögn með tölfræðilegum reikningum](bi-use-statistical-accounts.md). Hægt er að fræðast meira um víddir með því að fara í [Vinna með víddir](finance-dimensions.md).        |

## Nota aðferð fyrir fasta samnýtingu eða prósentu til að úthluta upphæðum

1.  ![Veldu Lightbulb sem opnar táknið Segja mér,](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") sláðu inn **Úthlutunarreikning** og veldu svo viðeigandi tengil.  
1. Á síðunni **Úthlutunarreikningar** skal velja **Nýtt**.
1. Fylla þarf út reitinn **Nr.**. Reitunum Heiti **.** 
1. Í reitnum **Tegund** reiknings er Valið **Fast**.
1. Í reitnum **Tegund** viðtökureiknings skal velja **Fjárhagsreikningur** eða **Bankareikningur**.
1. Í reitnum **Númer** viðtökureiknings skal velja reikninginn sem bóka á gildið á.
1. Valfrjálst: Veljið **víddirnar** og tilgreinið síðan víddirnar sem á að bóka fyrir línuna.
1. Í reitunum **Samnýting** og **Prósenta** skal tilgreina hvernig á að dreifa upphæðum á áfangareikninginn.
  
   > [!TIP]
   > Ef raunveruleg upphæð er færð inn til að úthluta fastri úthlutun í reitinn **Samnýta** sýnir reiturinn **Prósenta prósentu** heildarupphæðarinnar.
1. Þetta ferli er endurtekið fyrir hvern reikning sem á að taka með í úthlutun.

## Nota breytilega aðferð til að úthluta upphæðum

1.  ![Veldu Lightbulb sem opnar táknið Segja mér,](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") sláðu inn **Úthlutunarreikning** og veldu svo viðeigandi tengil.  
1. Á síðunni **Úthlutunarreikningar** skal velja **Nýtt**.
1. Fylla þarf út reitinn **Nr.**. Reitunum Heiti **.** 
1. Í reitnum **Tegund** reiknings er valið **Breytilegt**.
1. Í reitnum **Tegund** viðtökureiknings skal velja **Fjárhagsreikningur**.
1. Í reitnum **Númer** viðtökureiknings skal velja reikninginn sem bóka á gildið á.
1. Í reitnum **Tegund** sundurliðunarreiknings skal velja **Upplýsingareikningur**.
1. Í reitnum **Útreikningstímabil** er valið tímabilið sem á að dreifa upphæðum á.
1. Valfrjálst: Til að afmarka eftir tilteknum gildum altækra vídda skal velja **afmarkanir á stöðu sundurliðunarreiknings** og tilgreina síðan afmörkunargildin.
1. Valfrjálst: Veljið **víddirnar** og tilgreinið síðan víddirnar sem á að bóka fyrir línuna.

## Úthluta upphæðum á fljúgandi

Úthlutunarreikningar eru stofnaðir til að skipta tekjum og kostnaði fyrir fjárhagsreikninga og bankareikninga. Sjálfvirk úthlutun getur sparað tíma. Eigi hinsvegar að nota úthlutunarreikninga en ekki að stofna þá fyrir hvern fjárhagsreikning er hægt að spara enn meiri tíma.

Valkosturinn Afrita frá yfirvalkostum gerir kleift að nota úthlutunarreikninginn til að skipta upphæðum fyrir fjárhagsreikning í línu í fylgiskjali eða færslubók. Í reitnum **Tegund** reiknings í fylgiskjals- eða færslubókarlínu er valinn fjárhagsreikningur og úthlutunarreikningurinn síðan valinn í reitnum **Úthlutunarreikningur nr.** Ef reiturinn er auður er Upphæðinni í línunni er skipt upp fyrir fjárhagsreikninginn samkvæmt uppsetningunni í úthlutunarreikningnum. Minna gegnsæ leið til úthlutunar en ekki þarf að stofna úthlutunarreikning sérstaklega fyrir fjárhagsreikninginn.

Auðvelt er að setja upp tilfalkkaúthlutanir. Í stað þess að tilgreina banka eða fjárhagsreikning í reitnum **Tegund** viðtökureiknings á síðunni **Úthlutunarreikningur** er valkosturinn Afrita frá yfirvalkostinum **valinn**. Reiturinn **Númer** viðtökureiknings er hafður auður. Þegar fjárhagsreikningurinn er valinn í fylgiskjals- eða færslubókarlínunni er sá reikningur notaður til að úthluta upphæðum.

## Staðfesta að upphæðir dreifist rétt áður en þær eru bókaðar

Nokkrar leiðir eru til að sannprófa að upphæðir dreifist rétt:

* Á síðunni **Úthlutunarreikningur** skal velja aðgerðina Prófun **úthlutunar** . Reiturinn **Upphæð til úthlutunar er notaður til að prófa** aðrar upphæðir.
* Á síðunni **Fjárhagsbækur** skal velja færslubókina og nota svo aðgerðina **Bókunarforskoðun** .

## Stilla dreifinguna

Ef eitthvað finnst í úthlutun sem á að breyta er hægt að leiðrétta úthlutunina áður en hún er bókuð.  

1. Skjalið eða færslubókin með úthlutuninni sem á að breyta er opnuð.
1. Veljið línuna og veljið svo aðgerðina **Endurdreifa úthlutun** reiknings.
1. Á síðunni **Breyta úthlutunum** þarf að leiðrétta.

## Bóka úthlutunarfærslu

Eftirfarandi skref útskýra hvernig á að bóka úthlutunarfærslu úr færslubók. Skrefin eru eins fyrir sölu- og innkaupaskjöl.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.  
1. Stofnið nýja línu. Reitirnir eru fylltir út eins og hver vill fyrir aðrar tegundir færslubóka.
1. Ef föst eða breytileg úthlutun er notuð er fyllt út í eftirfarandi reiti:
    1. Í reitnum **Tegund** reiknings er Úthlutunarreikningur **valinn**.
    1. Í reitnum **Reikningur nr.** skal velja úthlutunarreikning.
1. Ef úthlutun sem notar Erfa frá yfirvalkostinum er eftirfarandi gert:
    1. Fjárhagsreikningur **er valinn** í reitnum **Tegund** reiknings.
    1. Í reitnum **Reikningur nr.** skal velja fjárhagsreikninginn.
    1. Í reitnum **Úthlutunarreikningur nr.** skal velja úthlutunarreikninginn sem er settur upp til að nota valkostinn Afrita frá yfirvalkostinum. 
1. Velja **Bóka**.

## Sjá einnig

[Vinna í færslubókum](ui-work-general-journals.md)  