---
title: Nota upplýsingareikninga til að greina gögn sem ekki eru viðskipti
description: Lýsir því hvernig tölfræðilegir reikningar eru notaðir sem annar uppruni gagna fyrir greiningar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
ms.service: dynamics-365-business-central
---
# <a name="analyze-data-with-statistical-accounts"></a>Greina gögn með tölfræðilegum reikningum

Nota tölfræðilega reikninga til viðbótarupplýsinga í fjárhagsskýrslum. Með tölfræðilegum reikningum er hægt að bæta við mælieiningum sem byggðar eru á gögnum sem ekki tengjast viðskiptum. Gögnum sem ekki eru í færslum er bætt við eins og einingum sem byggja á tölum, svo sem:

* Höfuðstaður starfsmanns
* Ferningslaga
* Fjöldi viðskiptamanna með gjaldfallna reikninga

Til dæmis er hægt að mæla tekjur eða kostnað eftir fjölda fólks í deild. Yfirskrift deildarinnar er eining upplýsingareikningsins. Eftirfarandi mynd sýnir dæmi um skýrslu sem notar tölfræðilegan reikning til að sýna tekjur á hvern starfsmann.

:::image type="content" source="media/statistical account report example.png" alt-text="Dæmi um skýrslu sem inniheldur gögn úr upplýsingareikningi.":::

Með tilliti til þess hvernig þeir vinna eru tölfræðilegir reikningar líkir bókunarreikningum. Þær geyma færslur sem bókaðar eru með því að nota tölfræðilegar lykilbækur svo að hægt sé að nota færslurnar sem gögn fyrir fjárhagsskýrslur. Nánari upplýsingar um fjárhagsskýrslur fást [í Undirbúning fjárhagsskýrslna með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md). 

Nokkur lykilmunur er á milli tölfræðireikninga og bókunarreikninga. Tölfræðilegir reikningar eru aðskildar einingar og eru ekki taldar með í prófjöfnunarskýrslum. Einnig þarf ekki að jafna debet- og kreditupphæðir þegar upplýsingareikningsbækur eru notaðar til að bóka færslur á upplýsingareikning. Upphæðin er bókuð.

## <a name="set-up-a-statistical-account"></a>Setja upp tölfræðilegan reikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **upplýsingareikninga** og velja síðan viðeigandi tengil.
1. Í flýtiflipanum **Almennt** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account"></a>Bóka upphæðir á tölfræðilegan reikning

1. Til að bóka upphæðirnar sem á að rekja er aðgerðin Upplýsingareikningabók valin á **síðunni Upplýsingareikningar**  **.** 
1. Í reitinn **Bókunardagsetning** er færð inn lokadagsetning bókunartímabilsins sem bóka á upphæðir fyrir.
1. Valfrjálst: Ef rekja á upphæðir fyrir tiltekið fylgiskjal í reitnum **Númer fylgiskjals.** er kenni fylgiskjalsins fært inn.
1. Í reitnum **Upplýsingareikningur nr.** skal velja upplýsingareikninginn sem bóka á upphæðir á.
1. Í reitinn **Lýsing** er færð inn stutt lýsing á því sem verið er að mæla.  
1. Í reitinn **Upphæð** er upphæðin sem á að bóka færð inn. 
1. Valfrjálst: Eigi að taka upplýsingareikninginn með í ítarlegri greiningum þarf að tilgreina víddir í reitunum **Deildarkóti og** Kóti **viðskiptamannahóps**. Til að fræðast meira um víddir er farið í [Greining gagna eftir víddum](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts"></a>Sannprófa upphæðir talnagagnalykla

Á síðunni **Upplýsingareikningar** er aðgerðin **Staða** upplýsingareikninga notuð til að sannreyna að skráðar upphæðir séu réttar fyrir hvert tímabil.  

## <a name="include-the-statistical-account-in-a-financial-report"></a>Taka talnagagnareikning með í fjárhagsskýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Stofna nýja fjárhagsskýrslu á einn af eftirfarandi háttum:
    1. Til að byrja frá grunni skal velja **Nýtt**. Nánari upplýsingar um stofnun fjárhagsskýrslna eru í [Stofna nýja fjárhagsskýrslu](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Til að nota stillingar úr svipaðri skýrslu sem þegar er til er skýrslan valin til að afrita og svo aðgerðin **Afrita fjárhagsskýrslu** valin. Hægt er að breyta stillingunum sem afritaðar eru í nýju skýrslunni.
1. Bæta við upplýsingareikningi:
    1. Ef byrjað er frá grunni skal velja aðgerðina **Breyta línuskilgreiningu** .
    1. Til að nota línuskilgreiningu úr skýrslu sem þegar er til skal velja skýrsluna til að afrita úr og velja svo aðgerðina **Afrita línuskilgreiningu** .
1.  **Á línuskilgreiningarsíðunni**, í reitnum **Línunr.** Er tilgreint hvar línan birtist í röð lína í skýrslunni.
1. Í reitinn **Lýsing** er færður inn texti sem gefur til kynna hvað er verið að mæla.
1. Í reitnum **Tegund** samantektar skal velja **Upplýsingareikningar**.
1. Í reitnum **Samantekt** skal velja upplýsingareikning.
1. Í reitnum **Tegund** línu er valið hvort skoða eigi stöðuna á bókunardagsetningunni eða byrjun bókunartímabilsins eða sýna breytingu á upphæðinni á tímabilinu.
1. Eftirstandandi reitir eru fylltir út. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Sjá einnig

[Viðskiptagreind fjármála](bi.md)  
[Fjárhagsskýrslur og greiningar í Business Central](finance-reports.md)
