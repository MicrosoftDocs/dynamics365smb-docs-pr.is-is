---
title: Vinna með aðalgagnasamstillingu
description: Læra hvernig á að stjórna samstillingu aðalgagna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 04/05/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization"></a>Vinna með aðalgagnasamstillingu

Þegar aðalgagnasamstilling hefur verið sett upp og samstillt í fyrsta skipti eru færslur í völdu töflunum paraðar og ítrekunarfærsla verkraðar er stofnuð fyrir hverja töflu. Verkraðarfærslurnar samstilla sjálfkrafa gögn í dótturfyrirtækjunum þegar einhver breytir upprunafyrirtækinu. Annars þarftu ekki að gera neitt.

> [!NOTE]
> Sjálfgefið er að verkraðarfærslurnar séu áætlaðar keyrðar hverja mínútu og ekki er hægt að breyta tímasetningunni.

Stundum fara hlutirnir hins vegar úrskeiðis og það gætu verið aðstæður sem maður þarf að hafa umsjón með eða rannsaka. Ef fólk breytir til dæmis sömu færslu bæði í upprunafyrirtækinu og dótturfyrirtæki mistekst samstillingin þannig að hægt sé að tilgreina rétta breytingu. Einnig getur upprunafyrirtækið sett upp viðauka sem breytir skema einnar af töflunum sem samstilla á með því að bæta við reit eða tveimur. Ef samstilla á nýju reitina í dótturfyrirtækjunum þarf að setja upp sömu viðbætur og uppfæra töfluskírteinin í uppsetningu þeirra.

Þessi grein lýsir verkfærunum sem þú getur notað til að halda samstillingu keyrð vel.

## <a name="overwrite-local-changes"></a>Skrifa yfir staðbundnar breytingar

Hægt er að nota gátreitinn **Skrifa yfir staðbundna breytingu** á reitunum og töflurnar sem samstilltar eru til að leyfa gögnum frá upprunafyrirtækinu að skrifa yfir gögn í dótturfyrirtækinu.

> [!NOTE]
> Ekki er hægt að gera samstillingu reita virka og leyfa dótturfyrirtækinu að skrifa gildi í hann óháð upprunafyrirtækinu. Annaðhvort verður að gera samstillingu óvirka fyrir reitinn eða leyfa ot upprunafyrirtækisins að skrifa yfir staðbundnar breytingar.

## <a name="update-table-schemas"></a>Uppfæra töfluskkemu

Ef upprunafyrirtækið breytir til dæmis töflu með því að bæta við reit sem á að samstilla verða dótturfyrirtæki að uppfæra reitavörpun sína. Á síðunni **Samstillingarreitir** skal nota aðgerðina **Uppfæra reiti** .

## <a name="enable-or-disable-couplings-between-records"></a>Gera stillingar virkar eða óvirkar milli færslna

Til að hefja eða stöðva jöfnun ákveðinna færslna í töflu á síðunni **Samstillingarreitir** skal velja reitina og nota annaðhvort **aðgerðirnar Gera virkar** eða **óvirkar** .

> [!TIP]
> Fljótleg leið til að gera marga reiti virka eða óvirka samtímis er að velja þá á listanum og nota annaðhvort **aðgerðirnar Gera virka** eða **óvirka** .

## <a name="run-a-full-synchronization"></a>Keyra fulla samstillingu

Aðgerðin **Keyra fulla samstillingu** raðar samstillingu fyrir allar töflufærslur í upprunafyrirtækinu og endurstillir allar færslur afundur. Til dæmis er samstilling gagnleg ef aukareitur í samstillingartöflu er virkur eða viðbótarreit bætt við með aðgerðinni **Uppfæra reiti** . Aðgerðin samstillir afturvirkt gögnin í þessum reitum.

## <a name="synchronize-modified-records"></a>Samstilla breyttar færslur

Ef stillingum töflu eða reits í dótturfyrirtæki er breytt verður að uppfæra samstillinguna. Til að uppfæra samstillinguna skal nota aðgerðina **Samstilla breyttar færslur** á síðunni **Samstillingartöflur** .

Aðgerðin **Samstilla breyttar** færslur tímasetur samstillingu eftirfarandi töflufærslna:

* Færslur sem ekki tókst að samstilla í síðustu tilraun.
* Færslur sem var breytt í upprunafyrirtækinu eftir að samstillingin var síðast tímasett. Hægt er að fara yfir síðasta áætlaða samstillingartíma á síðunni **Samstillingartöflur** í reitnum **Samstilla breytingar síðan** .

Aðgerðin virkar á sama hátt og tímasett samstilling og hægt er að nota hana sem leið til að samstilla utan áætlunarinnar. Ef t.d. gátreiturinn **Skrifa yfir staðbundnar breytingar** er valinn í reit til að leyfa gögnum frá upprunafyrirtækinu að skrifa yfir staðbundnar breytingar uppfærir aðgerðin þessi gögn. Einnig er bara hægt að bíða þar til næsta áætluð samstilling gerist.

## <a name="investigate-the-status-of-synchronization"></a>Kanna stöðu samstillinga

Tvær aðgerðir eru á síðunni **Samstillingartöflur** sem hjálpa til við að fylgjast með samstillingunni:

* **Samþættingarverk**
* **Verkraðarfærslur**

Eftirfarandi tafla lýsir aðgerðunum.

|Síða  |Heimildasamstæða  |
|---------|---------|
|**Samþættingarverk**     | Opna síðuna **Samstillingarverk** til að rannsaka hvað gerðist í hvert sinn sem verkraðarfærsla var keyrð. Til að grafa dýpra í upplýsingar um nýjar færslur sem var bætt við eða kanna hvers vegna færsla samstilltist ekki skal velja tölurnar í dálkunum **Sett inn** eða **Mistókst** . Einnig er hægt að nota þessa síðu til að hreinsa eldri færslur sem hugsanlega eru óþarfar. Til að fræðast meira um tiltekt er farið í [Hreinsa gamlar](#clean-up-old-entries) færslur.        |
|**Verkraðarfærslur**     | Fá aðgang að upplýsingum um verkraðarfærslu sem samstilla gögn fyrir valda töflu. Til dæmis má nota þessa síðu til að stjórna stöðu verkraðarfærslunnar til að fræðast meira um verkraðarfærslur með því að fara í [Nota verkröð til að tímasetja verk](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Ef villa finnst á síðunni **Samstillingarverk** sem þú getur ekki leyst sjálf(ur) getur þú ekki leyst þig, ef þú hefur samband við samstarfsaðila eða Microsoft til stuðnings, er gagnlegt að veita villuboðin og símtalsupplýsingarnar.

## <a name="clean-up-old-entries"></a>Hreinsa gamlar færslur

Með tímanum verður fjöldi færslna í samstillingarkladdanum stór og því gæti þurft að gera smá þrif til að fjarlægja óþarfar færslur. Ef auðvelda á að hreinsa gamlar færslur **býður síðan Samstillingarverk** upp á eftirfarandi aðgerðir:

* **Eyða færslum eldri en 7 dögum**
* **Eyða öllum færslum**

## <a name="adding-extensions"></a>Viðbótum bætt við

Ef upprunafyrirtækið setur upp nýja viðbót verður dótturfyrirtækið einnig að setja það upp ef samstilla á gögn fyrir það. Dótturfyrirtækið getur notað aðgerðina **Uppfæra reiti** á síðunni **Samstillingarreitir** til að bæta töflunum úr nafnaukanum við listann.

> [!NOTE]
> Sumar töflur sækja gögn úr tengdum töflum. Ef bætt er við viðbót sem inniheldur ekki tengdar töflur verða reitirnir í þessum töflum ekki tiltækir. Ganga þarf úr skugga um að öllum tengdum töflum hafi verið bætt við.

<!--
## <a name="recreate-a-deleted-job-queue-entry"></a>Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also"></a>Sjá einnig

[Undirbúningur fyrir samstillingu aðalgagna](admin-set-up-data-sync.md)
