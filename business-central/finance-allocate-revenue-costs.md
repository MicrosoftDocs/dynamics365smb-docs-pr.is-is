---
title: Úthluta tekjum og kostnaði á marga fjárhagslykla
description: Læra hvernig á að úthluta kostnaði á einn eða fleiri lykla í fjárhag.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Úthluta tekjum og kostnaði á marga fjárhagslykla

Í þessari grein er lýst hvernig á að nota úthlutunarlykla til að dreifa upphæðum á sölu-og innkaupaskjölum og færslubókarlínum í mismunandi fjárhagsreikninga. Hægt er að úthluta upphæðum með fastri eða breytilegri dreifingu.  

Úthlutunin skiptir færslubókarlínu í línur sem skilgreindar eru á  **reikningssíðu úthlutunarlykils** . Ef t.d. er skipt á leigu á þremur leiðum með víddum, þá eru þrjár línur bókaðar fyrir úthlutunina. Þess vegna færðu sex fjárhagsfærslur (eða hugsanlega meira ef þú ert að nota VSK eða virðisaukaskatt). Þótt þetta innlegg fleiri fjárhagsfærslur en þörf krefur er hægt að bakfæra stakar línur í stað þess að bakfæra alla úthlutunina.

Úthlutunarlyklar virka einnig með deferrals. Til að fræðast meira um deferrals er farið í  [tekjur og útgjöld](finance-how-defer-revenue-expenses.md).

Eftirfarandi tafla kynnir úthlutunaraðferðirnar sem hægt er að nota.

|Úthlutunaraðferð  |Heimildasamstæða  |
|---------|---------|
|Lagað     | Þegar skipta á útgjöldum á þann hátt sem endurtekið er yfir lengri tíma er hægt að nýta sér fasta úthlutun. Föst úthlutun við skulum skilgreina úthlutunarskiptinguna. Þessi skiptiskipti breytist aðeins þegar uppsetningu er breytt á  **síðunni úthlutunarlykil**  úthlutunar.        |
|Breytilegt     | Til að dreifa tekjum eða útgjöldum út frá gildum sem breytast með tímanum er notuð Breytileg úthlutunaraðferð. Breytileg úthlutun láta tilgreindar heimildir til að nota við útreikning úthlutunarprósentu. Þessi aðferð hentar vel t.d. fyrir skerta starfsmannakostnað sem samkvæmt misháum fjölda í deild eða deildum er. Annað dæmi er úthlutun kostnaðar við Leigu samkvæmt myndefni í framleiðsluhæð sem gæti verið breytilegt eftir framleiðslulínu. Breytilegar úthlutanir nota samsetningu vídda og talnagykla til að ákvarða hvernig upphæðir dreifast á tímabil. Til að fræðast nánar um tölfræðireikninga er farið í að  [greina gögn með tölfræðilegum reikningum](bi-use-statistical-accounts.md). Til að fræðast meira um víddir er farið að  [vinna með víddir](finance-dimensions.md).        |

## Nota fasta hluti eða prósentu til að úthluta upphæðum

1.  ![Veldu þá ljósaperu sem opnar teiknið segja mér eiginleika](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") , Sláðu inn  **úthlutunarlykil** og veldu síðan tengda tengilinn.  
1.  **Veldu**  nýtt  **fyrir á síðunni Úthlutunarlyklar**.
1. Fylla þarf út reitinn **Nr.**. Og  **Heiti**  reita.
1.  **Valið**  er fast  **í reitnum Tegund** reiknings.
1.  **Í reitinn Tegund**  viðtökustaðar reiknings er valinn  **fjárhagsreikningur**  eða  **Bankareikningur**.
1.  **Í reitnum viðtökunúmer**  áfangastaðar er valinn lykillinn sem á að bóka gildið á.
1. Valfrjálst: Velja  **víddaraðgerðina**  og tilgreina síðan víddirnar sem á að bóka fyrir línuna.
1.  **Í reitunum hluti**  og  **Prósenta**  er tilgreint hvernig eigi að dreifa upphæðum á áfangareikninginn.
  
   > [!TIP]
   > Ef Raunupphæðin sem úthluta á fyrir fasta úthlutun er færð inn í  **samhlutunarsvæðið**  **sýnir reiturinn prósenta**  heildarupphæðina.
1. Endurtaka þetta ferli fyrir hvern lykil sem á að hafa með í úthlutuninni.

## Nota breytilega aðferð til að ráðstafa upphæðum

1.  ![Veldu þá ljósaperu sem opnar teiknið segja mér eiginleika](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") , Sláðu inn  **úthlutunarlykil** og veldu síðan tengda tengilinn.  
1.  **Veldu**  nýtt  **fyrir á síðunni Úthlutunarlyklar**.
1. Fylla þarf út reitinn **Nr.**. Og  **Heiti**  reita.
1.  **Í reitnum Tegund**  reiknings skal velja  **breytu**.
1.  **Í reitnum Tegund**  viðtökureiknings er valinn  **fjárhagsreikningur**.
1.  **Í reitnum viðtökunúmer**  áfangastaðar er valinn lykillinn sem á að bóka gildið á.
1.  **Í reitinn gerð**  sundurliðunarlykils er valinn  **talnagas**.
1.  **Í reitnum útreikningstímabil**  er valið það tímabil sem á að dreifa upphæðum á.
1. Valfrjálst: til að afmarka á Sérstök Altæk víddargildi skal velja afmörkun á  **stöðu**  sundurliðunar lykils og tilgreina síðan síunargildin.
1. Valfrjálst: Velja  **víddaraðgerðina**  og tilgreina síðan víddirnar sem á að bóka fyrir línuna.

## Ráðstafa upphæðum á Flúðum

Úthlutunarlyklar eru stofnaðir til að skipta tekjum og kostnaði fyrir fjárhagsreikninga og bankareikninga. Ef úthlutun er sjálfvalar getur það sparað mikinn tíma. Hins vegar, ef nota á úthlutunarlykla, en ekki á að stofna þá fyrir hvern fjárhagsreikning, er hægt að vista enn lengri tíma.

Með valkostinum afrita úr yfirvalkosts er hægt að nota úthlutunarlykilinn til að skipta upphæðum á fjárhagsreikning í línu í fylgiskjali eða færslubók.  **Í reitnum Tegund**  reiknings í fylgiskjali eða bókarlínu er Fjárhagsreikningur valinn og síðan er úthlutunarlykillinn í reitnum  **úthlutunarreikningur nr.** sviði. Upphæðinni í línunni er skipt fyrir fjárhagsreikninginn samkvæmt uppsetningunni í úthlutunarreikningnum. Það er tæpast gagnsæ leið til úthlutunar en ekki þarf að stofna úthlutunarlykil sérstaklega fyrir fjárhagsreikninginn.

Auðvelt er að setja upp tilfallandi úthlutanir úr tilfallandi. Í stað þess að tilgreina bankareikning eða fjárhagsreikning í  **reitnum Tegund**  endareiknings á  **úthlutunarlykli**  er hægt að  **Velja erfð frá yfirvalkostinum** . Skilja skal  **reitinn Númer**  viðtökureiknings eftir auðan. Þegar fjárhagsreikningurinn er valinn í skjalinu eða færslubókarlínunni er lykillinn notaður til að úthluta upphæðum.

## Staðfestið að upphæðir dreifist rétt áður en þær eru bókaðar

Það eru nokkrar leiðir til að sannreyna að upphæðir dreifist rétt:

*  **Á síðunni úthlutunarlykil**  skal velja  **aðgerðina prófun úthlutunar** .  **Notið upphæðina til að úthluta**  svæði til að prófa mismunandi upphæðir.
*  **Á síðunni fjárhagsfærslubækur**  er færslubókin valin og aðgerðin Forskoðun  **bókunar notuð** .

## Leiðrétta dreifinguna

Ef þú finnur eitthvað í úthlutun sem þú vilt breyta getur þú aðlagað úthlutunina áður en þú bókar hana.  

1. Opnið skjalið eða færslubókina sem hefur úthlutunina sem á að breyta.
1. Línan er valin og síðan er  **aðgerðin endurdreifa Reikningsúthlutun**  valin.
1.  **Gerið leiðréttinguna á síðunni Breyta úthlutun** .

## Bóka úthlutunarfærslu

Eftirfarandi skref lýsa því hvernig úthlutunarfærslu er bókuð úr færslubók. Þrepin eru þau sömu fyrir sölu-og innkaupaskjöl.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.  
1. Stofnið nýja línu. Fyllt er í reitina á sama hátt og óskað er eftir öðrum færslugerð færslubókar.
1. Ef notuð er föst eða breytileg úthlutun skal fylla út eftirfarandi reiti:
    1.  **Í reitnum Tegund**  reiknings skal velja  **úthlutunarlykil**.
    1. Í reitnum  **Reikningur nr.** er úthlutunarlykillinn valinn.
1. Ef úthlutun sem notar erfði frá yfirvalkostinum er notuð skal gera eftirfarandi:
    1.  **Fjárhagsreikningur**  er valinn  **í reitnum Tegund** reiknings.
    1. Í reitnum  **Reikningur nr.** er valinn Fjárhagsreikningur.
    1.  **Í úthlutunarlykli nr.** skal velja úthlutunarlykilinn sem er settur upp til að nota valkostinn erfa frá yfirvalkostinum. 
1. Velja **Bóka**.

## Sjá einnig

[Vinna í færslubókum](ui-work-general-journals.md)  