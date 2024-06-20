---
title: Dálkaskilgreiningar í fjárhagsskýrslugerð
description: Lýsir því hvernig dálkskilgreiningar í fjárhagsskýrslugerðarvinnu.
author: kennieNP
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 488, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Dálkaskilgreiningar í fjárhagsskýrslugerð

Nota dálkaskilgreiningar til að tilgreina dálkana sem á að hafa með í skýrslu. Til dæmis er hægt að hanna skýrsluuppsetningu til að bera saman breytingu og stöðu fyrir sama tímabil á þessu ári og síðasta ári. Hægt er að hafa allt að 15 dálka í dálkskilgreiningu. Til dæmis eru margir dálkar gagnlegir til að birta áætlanir í 12 mánuði með dálki sem sýnir samtöluna.

## Stofna eða breyta dálkaskilgreiningu

Til að stofna eða breyta dálkaskilgreiningu skal fylgja þessum skrefum.

> [!NOTE]
> Prentaðar, forséðar og vistaðar útgáfur fjárhagsskýrslu sýna mest fimm dálka. Ef fjárhagsskýrsla er hins vegar aðeins ætluð til greiningar á síðunni **Fjárhagsskýrsla** er hægt að búa til eins marga dálka og óskað er.

1. Á síðunni **Fjárhagsskýrslur** skal velja viðeigandi fjárhagsskýrslu og velja svo aðgerðina **Breyta dálkaskilgreiningu** .
1. Á síðunni **Dálkskilgreining** skal búa til línu fyrir hvern dálk þar sem fjárhagsgögn eru sýnd í fjárhagsskýrslunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Velja **Í lagi**.
1. Opnaðu síðuna **Fjárhagsskýrsla** öðru hverju til að staðfesta að nýja dálkskilgreiningin virki eins og til er ætlast.

## Innbyggðar dálkaskilgreiningar

[!INCLUDE[prod_short](includes/prod_short.md)] veitir sýnidálksskilgreiningar sem geta hjálpað til við að byrja að setja upp fjárhagsskýrslur sem uppfylla þarfir notanda.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## Dæmi: Stofna dálkaskilgreiningu til að reikna prósentur

Hugsanlega þarf að vera dálkur í fjárhagsskýrslu til að reikna prósentur af samtölu. Ef til dæmis eru línur sem skipta sölu eftir víddum er hægt að dálkur vísa til prósentu heildarsölu í hverri línu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** skal velja Fjármálaskýrsla.  
1. Veljið aðgerðina **Breyta fjárhagsskýrslu** til að setja upp fjárhagsskýrslulínu til að reikna út samtöluna sem prósenturnar byggjast á.  
1. Línu er bætt við fyrir ofan fyrstu línuna sem á að birta prósentu fyrir.  
1. Reitirnir í línunni eru fylltir út sem hér segir: 
    1. Í reitinn **Tegund** samantektar er valinn **Stofn fyrir prósentur**. 
    1. Í reitinn **Samantekt** er færð inn reikniregla fyrir samtöluna sem prósentan er byggð á. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
1. Veljið aðgerðina **Breyta dálkskilgreiningu** til að setja upp dálk.  
1. Reitirnir í línunni eru fylltir út sem hér segir. 
    1. Í reitnum **Dálktegund** er valin **Reikniregla**. 
    1. Í reitnum **Formúla** er færð inn formúla fyrir upphæðina sem reikna á prósentuhlutfall fyrir, með prósentutákni (%) þar fyrir aftan. Til dæmis ef dálkur N inniheldur nettóbreytinguna, er fært inn **N%**.  
1. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## Samanburður á reikningstímabilum með reiknireglum tímabils

Fjárhagsskýrslan þín getur borið saman niðurstöður mismunandi reikningstímabila, svo sem síðastliðins mánaðar samanborið við sama mánuð á síðasta ári. Til að gera þetta skal opna síðuna **Dálkaskilgreining** og sérstilla hana með því að bæta reitnum **Formúla samanburðartímabils** við sem dálki. Frekari upplýsingar er að finna á [Sérstilling verksvæðis](ui-personalization-user.md). Hægt er að stilla þennan reit á reiknireglu tímabils.  

Bókhaldstímabil þarf ekki að vera í samræmi við dagatalið. Þó verður að vera sami fjöldi reikningstímabila á hverju reikningsári þótt tímabilin geti verið mismunandi að lengd.  

[!INCLUDE[prod_short](includes/prod_short.md)] nýtir formúluna fyrir tímabil til að reikna út lengd samanburðartímabils miðað við tímabilið sem fæst við dagsetningasíu á skýrslunni. Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar. Eftirfarandi tafla sýnir skammstafanirnar fyrir tímabilslýsingar.

| Skammstöfun | Heimildasamstæða                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| T            | Tímabil.                                                                                |
| ST           | Síðasta tímabil reikningsárs, hálfsárs eða ársfjórðungs.                                   |
| CP           | GT (gildandi tímabil) reikningsárs, hálfsárs eða ársfjórðungs. Notið GT í reiknireglum til að stilla tímabilið sem byrjar eða endar reikniregluna. Til dæmis RÁ\[1..GT\] sýnir tímann frá upphafi gildandi reikningsárs til gildandi tímabils.|
| FÁ           | Reikningsár. Til dæmis á RÁ\[1..3\] á við um fyrsta fjórðung yfirstandandi fjárhagsárs. |

Dæmi um reiknireglur:

| Formúla | Lýsing |
|-----|-----|
| \<Blank\>       | Gildandi tímabil. |
| \-1T            | Fyrra tímabil.            |
| \-1RÁ\[1..ST\]  | Allt fyrra reikningsár.                  |
| \-1RÁ           | Yfirstandandi tímabil á fyrra reikningsári.       |
| \-1RÁ\[1..3\]   | Fyrsti fjórðung fyrra reikningsárs.        |
| \-1RÁ\[1..GT\]  | Frá upphafi fyrra fjárhagsárs til núverandi tímabils í fyrra reikningsári, bæði tímabilin tekin með |
| \-1RÁ\[GT..ST\] | Frá núverandi fjárhagsári til núverandi tímabils í fyrra reikningsári, bæði tímabilin tekin með   |

Reikniregla er færð inn í reitinn **Reikniregla samanb.dagsetningar** í staðinn til að reikna út eftir venjulegum tímabilum. Ef reiturinn er t.d. stilltur á -1Y ber [!INCLUDE [prod_short](includes/prod_short.md)]  saman við sama tímabil fyrr.

> [!NOTE]
> Ekki er alltaf augljóst hvaða tímabil er verið að bera saman vegna þess að hægt er að setja dagsetningarafmörkun á skýrslu sem nær yfir dagsetningar sem eru aðrar en reikningstímabilin í bókhaldslyklinum. Ef stofnuð er fjárhagsskýrsla þar sem á að bera þetta tímabil saman við sama tímabil í fyrra er reiturinn Reikniregla samanburðardagsetningar **stilltur** á **1FY**. Síðan er skýrslan keyrð 28 **. febrúar og dagsetningarafmörkun** stillt á **janúar og febrúar**. Fyrir vikið ber fjárhagsskýrsluna saman janúar og febrúar á þessu ári við janúar á síðasta ári, sem er eina bókhaldstímabilið af tveimur sem var lokið á síðasta ári.  

Frekari upplýsingar í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## Skilgreiningar fjárhagsskýrsludálks í inn- eða útflutningi

Ef byrjað er á útgáfubylgju 1 2024 (útgáfa 24.1) er hægt að flytja inn og út fjárhagsskýrsludálksskilgreiningar sem RapidStart grunnstillingarpakka. Til dæmis eru grunnstillingarpakkar gagnlegir til að deila upplýsingum með öðrum fyrirtækjum. Pakkinn er búinn til í .rapidstart-skrá, sem þjappar innihaldinu saman.

> [!NOTE]
> Þegar skilgreiningar fjárhagsskýrsludálks eru fluttar inn er nýju skilgreiningunum skipt út fyrir færslur með sömu heitum og þær sem verið er að flytja inn. Skilgreiningarpakkinn fyrir skýrsluskilgreiningu skrifar ekki yfir fyrirliggjandi línu- eða dálkskilgreiningar sem eru notaðar í skýrsluskilgreiningunni.

Til að flytja inn eða flytja út skilgreiningar fjárhagsskýrsludálka skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Dálkaskilgreiningar** og velja síðan viðeigandi tengil.
1. Velja skal línuskilgreininguna og velja svo aðgerðina **Flytja inn dálkaskilgreiningu** eða **Flytja út dálkaskilgreiningu** eftir því hvað á að gera.

## Sjá einnig .

[Línuskilgreiningar í fjárhagsskýrslugerð](bi-row-definitions.md)  
[Undirbúa fjárhagsskýrslur](bi-how-work-account-schedule.md)  
[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
