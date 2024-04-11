---
title: Stjórna samstillingu aðalgagna
description: Fræðast um hvernig samstilling aðalgagna er stjórnað.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# Stjórna samstillingu aðalgagna

Eftir að samstilling aðalgagna hefur verið sett upp og samstillt í fyrsta sinn eru færslur í völdum töflum settar saman og færsla endurtekinna verkraðarstofna fyrir hverja töflu. Runufærslur eru sjálfkrafa samstilltar gögn í dótturfyrirtækjunum þegar einhver gerir breytingu á upprunafélaginu. Annars þarf maður ekki að gera neitt.

> [!NOTE]
> Runufærslurnar eru áætlaðar keyrðar á hverri stundu og ekki er hægt að breyta áætluninni.

Stundum fara hlutirnir þó úrskeiðis og það gætu verið aðstæður sem þarf að stjórna eða rannsaka. Til dæmis, ef fólk breytir sömu færslu bæði í upprunafélaginu og í dótturfyrirtæki, mistekst samstilling svo hægt sé að tilgreina breytinguna sem er rétt. Eða gæti Upprunafyrirtækið sett upp framlengingu sem breytir skema einnar af töflunum samstilla með því að bæta við reit eða tveimur. Ef samstilla á nýja reiti dótturfyrirtækjanna þarf að setja upp sömu viðaukanna og uppfæra Töfluskemu í uppsetningu þeirra.

Þessi grein lýsir verkfærunum sem nota má til að halda samstillingu í gangi vel.

## Rannsaka stöðu samstillingar

Tvær aðgerðir eru á síðunni Samstillingartöflur  **sem geta hjálpað til við**  að fylgjast með samstillingunni:

* **Samstillingarvinnslur samþættingar**
* **Færslur vinnsluraðar**

Eftirfarandi tafla lýsir aðgerðunum.

|Síða  |Description  |
|---------|---------|
|**Samstillingarvinnslur samþættingar**     |  **Opna síðuna störf**  Samstillingarsamstillingar til að kanna hvað gerðist í hvert sinn sem færsla í vinnslu var gerð í verkraðarafærslu. Til að grafa dýpra inn í upplýsingar um nýjar færslur sem var bætt við, eða kanna af hverju færsla tókst ekki samstillt, skal velja númerin í  **·**  dálkunum eða  **misheppnuðu** . Einnig er hægt að nota þessa síðu til að taka upp eldri færslur sem ekki er víst að þurfi. Til að fá frekari upplýsingar um tiltekt er farið í að  [taka upp gamlar færslur](#clean-up-old-entries).        |
|**Færslur vinnsluraðar**     | Nálgast upplýsingar um færsluna í vinnsluraðarafærslu sem samstilla gögn fyrir valda töflu. Til dæmis, þessi síða er notuð til að stjórna stöðu færslu í verkraðarafærslu, til að fá meiri upplýsingar um vinnsluraðarafærslur, farið í að  [nota Starfaraðir til að áætla verk](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Ef villa kemur upp á  **síðunni Samþættingarsamstillingarvinnslur**  sem ekki er hægt að leysa handvirkt ef haft er samband við samstarfsaðila eða Microsoft fyrir stuðning er gagnlegt að útvega villuboðin og upplýsingar um kallbunka.

## Samstilla breyttar færslur

Ef stillingum fyrir töflu eða svæði er breytt í dótturfyrirtæki þarf að uppfæra samstillinguna. Ef ákveðið er til dæmis að velja  **gátreitinn skrifa yfir staðbundna breytingu**  á reit til að leyfa gögnum frá upprunafélaginu að skrifa yfir staðbundnar breytingar. Til að uppfæra samstillinguna skal nota  **aðgerðina samstilla breytt færslur**  á  **síðunni samstillingartöflur** .

## Uppfæra Töfluskemu

Ef veitufyrirtækið breytir töflu, til dæmis með því að bæta við reit sem á að samstilla, verða dótturfyrirtækin að uppfæra svæðvarpana.  **Á síðunni samstillingarsvæði**  skal nota  **aðgerðina uppfærslusvæði** . 

## Gera þrýstingsstillirinn virka eða óvirka milli færslna

Til að ræsa eða stöðva festingu á tilteknum færslum í töflu, á  **síðunni samstillingarsvæði**, skal velja svæðin og nota síðan annað hvort aðgerðir til  **að virkja**  eða  **slökkva**  á þeim. 

> [!TIP]
> Fljótleg leið til að gera mörg svæði virk eða óvirk á sama tíma er að velja þau í listanum og nota síðan annað hvort  **Aðgerðir til að virkja**  eða  **slökkva**  á þeim.

## Bæta við viðaukum

Ef upprunafélagið setur upp nýja framlengingu þarf dótturfyrirtæki einnig að setja það upp ef það vill samstilla gögn fyrir það. Dótturfyrirtækið getur notað  **aðgerðina uppfæra svæði**  á  **síðunni samstillingarsvæði**  til að bæta töflunum úr viðaukanum við listann.

> [!NOTE]
> Sumar töflur fá gögn úr tengdum töflum. Ef viðbótartöflu er bætt við sem inniheldur ekki tengdar töflur eru svæðin í þessum töflum ekki tiltæk. Staðfestið að þú hafir bætt við öllum tengdum töflum.

## Tiltekt í gömlum færslum

Með tímanum verður Fjöldi færslna í samstillingarkladdanum orðinn stór, þannig að þú gætir viljað gera smá húsgæftir til að fjarlægja óþarfa færslur. Til að auðvelda Hreinsun á gömlum færslum,  **þá býður síða Samþættingarsamstillingarvinnslu**  eftirfarandi aðgerðir:

* **Eyða færslum eldri en 7 daga**
* **Eyða öllum færslum**

<!--
## Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## Sjá einnig

[Fá tilbúinn til að samstilla aðalgögn](admin-set-up-data-sync.md)
