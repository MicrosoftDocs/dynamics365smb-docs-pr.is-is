---
title: Nota Talnagagnakykla til að greina gögn sem ekki eru Transactional
description: Lýsir hvernig nota á talnagögnum lykla sem annan gagnagjafa fyrir greiningu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
ms.service: dynamics-365-business-central
---
# Greina gögn með tölfræðilegum reikningum

Nota talnagykla í upplýsingar um viðbót í ársskýrslur. Með tölfræðireikningum er hægt að bæta við mæliupplýsingum sem eru byggðar á ótransactional gögnum. Ótransviðbótargögnunum er bætt við eins og einingar sem byggðar eru á eftirfarandi:

* Starfsmannafundir
* Ferfætum
* Fjöldi viðskiptamanna með gjaldfallna reikninga

Til dæmis er hægt að mæla tekjur eða kostnað út frá fólksfjölda í deild. Höfuðstóll fyrir deildina er eining fyrir talnageikninginn. Eftirfarandi mynd sýnir dæmi um skýrslu sem notar tölfræðilykil til að sýna tekjur á hvern starfsmann.

:::image type="content" source="media/statistical account report example.png" alt-text="Dæmi um skýrslu sem inniheldur gögn úr tölfræðireikningi.":::

Með hliðsjón af því hvernig þær virka eru hagstæðir lyklar Svipaðir að bókunarreikningum. Þær geyma færslur sem bókaðar eru með tölfræðilegum reikningabókum, þannig að hægt sé að nota færslurnar sem gögn fyrir ársskýrslur. Til að fá frekari upplýsingar um ársskýrslur er farið í að  [undirbúa fjárhagsskýrslur með fjárhagslegum gögnum og lykilflokkum](bi-how-work-account-schedule.md). 

Nokkur lykilmismunur er á talnagtakröfum og bókunarreikningum. Tölfræðireikningar eru aðskildir aðilar og eru ekki teknir með í skýrslum um prufustöðu. Einnig þarf ekki að jafna debet-og kreditupphæðir þegar tölfræðilegar reikningabækur eru notaðar til að bóka færslur á Tölfræðilegt lykil. Þú bókar upphæðina bara.

## Setja upp talnageikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **talnagengdra lykla** og velja síðan tengdan tengil.
1. Í flýtiflipanum **Almennt** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Bóka upphæðir á talnageikning

1. Til að bóka upphæðirnar sem óskað er eftir að rekja, á  **síðunni hagstjórnarreikningar**, skal velja  **aðgerð Talnagarabókar** .
1.  **Í reitinn Bókunardags**  ., er færð inn Síðasti dagur bókunartímabilsins sem bóka á upphæðir fyrir.
1. Valfrjálst: Ef rekja á upphæðir fyrir tiltekið skjal í reitnum  **Fylgiskjal nr.**  er fært inn í reitinn KENNI skjalsins.
1.  **Í hagstjórnarlegu Reikningnr.**  skal velja þann lykil sem á að bóka upphæðir á.
1.  **Í reitinn Lýsing**  er rituð stutt lýsing á því sem verið er að mæla.  
1.  **Í reitinn Upphæð**  er rituð upphæðin sem á að bóka. 
1. Valfrjálst: Ef notandi vill hafa Talnagótslykta með Ítarlegri greiningu skal tilgreina víddir í  **reitunum Deildarkóti**  og  **Customergroup kóti** . Til að fræðast meira um víddir er farið í að  [greina gögn eftir víddum](bi-how-analyze-data-dimension.md).

## Sannreyna upphæðir talnageiknings

 **Á síðunni hagstjórnarreikningar**  skal nota  **aðgerðina upplýsingar um stöðu**  reikninga til að sannprófa að skráðar upphæðir séu réttar fyrir hvert tímabil.  

## Taka talnageikninginn með í ársskýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Stofnið nýja ársskýrslu með annarri af eftirfarandi hætti:
    1. Til að byrja frá grunni velur  **þú nýtt**. Til að fræðast meira um stofnun fjárhagsskýrslna er farið í að  [Stofna nýja ársskýrslu](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Ef nota á stillingar úr svipaðri skýrslu er skýrslan valin og hún síðan valin  **aðgerðin afrita fjárhagsskýrsla** . Hægt er að breyta þeim stillingum sem afritaðar eru í nýju skýrslunni.
1. Bættu við tölfræðilegum lykli:
    1. Ef þú ert að  **byrja frá grunni skaltu velja aðgerðina Breyta línuskilgreiningu** .
    1. Til að nota línuskilgreiningu úr fyrirliggjandi skýrslu skal velja skýrsluna sem afrita á úr og velja  **síðan aðgerðina afritaklínuskilgreining** .
1.  **Á Línuskilgreiningsíðunni**  í reitnum  **Línunr.** Er skilgreint hvar röðin birtist í röð línanna í skýrslunni.
1.  **Í reitinn Lýsing**  er ritaður texti sem gefur til kynna hvað verið er að mæla.
1.  **Í reitnum Tegund**  samantektar skal velja  **talnagykla**.
1.  **Í reitnum Samantekt**  er valinn tölfræðilykill.
1.  **Í reitnum Tegund**  línu er valið hvort skoða eigi stöðuna á bókunardagsetningunni eða í upphafi bókunartímabilsins eða sýna breytinguna á upphæðinni á tímabilinu.
1. Eftirstandandi reitir eru fylltir út. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Sjá einnig

[Viðskiptagreind fjármála](bi.md)  
[Fjárhagsskýrslur og greiningar í Business Central](finance-reports.md)