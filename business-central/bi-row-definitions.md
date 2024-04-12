---
title: Línuskilgreiningar í fjárhagsskýrslugerð
description: Lýsir því hvernig línuskilgreiningar í fjárhagsskýrslugerð.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Línuskilgreiningar í fjárhagsskýrslugerð

Línuskilgreiningar í fjárhagsskýrslum eru staður fyrir útreikninga sem ekki er hægt að gera beint í bókhaldslyklinum. Til dæmis er hægt að búa til millisamtölur fyrir reikningsflokka og setja þær inn í aðrar samtölur Einnig er hægt að reikna milliskref sem ekki eru sýnd í lokaskýrslunni.

## Stofna eða breyta línuskilgreiningu

Til að stofna eða breyta línuskilgreiningu skal fylgja eftirfarandi skrefum:

1. Á síðunni **Fjárhagsskýrslur** skal velja viðeigandi fjárhagsskýrslu og velja svo aðgerðina **Breyta línuskilgreiningu** .
1. Veldu aðgerðirnar **Setja inn fjárhagsreikninga**, **Setja inn sjóðstreymisreikninga** og **Setja inn kostnaðartegundir** til að búa til línu fyrir hverja fjárhagslega einingu sem á að greina. Til dæmis gæti ein lína verið fyrir núverandi eignir og önnur röð fyrir eignir. Skoðaðu fjármálaskýrslurnar í CRONUS sýnifyrirtækinu til að fá innblástur.

    > [!NOTE]
    > **Línan nr.** reiturinn sýnir fyrstu 10 stafina í kennimerki, eins og reikningsnúmer. Ef einingum með kennum sem byrja á sömu 10 stöfum er bætt við eru tvítekningar í reitnum **Línunr.** . Ef þörf er á er hægt að breyta kennimerkjum handvirkt eftir að þú hefur sett inn einingarnar. Öll kennimerkin eru birt í reitnum **Samantekt**.

> [!NOTE]
> Dálkarnir sem eru skilgreindir í hverri línu í línuskilgreiningunni tákna dálka þrjá og upp á síðunni **Fjárhagsskýrsla** . Fyrstu tveir dálkarnir, **Dálkanr.** og **Lýsing**, eru fastar.  

## Innbyggðar línuskilgreiningar

[!INCLUDE[prod_short](includes/prod_short.md)] veitir sýnidæmisskilgreiningar sem geta hjálpað til við að byrja að setja upp fjárhagsskýrslur sem uppfylla þarfir notanda.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> Sýnishornaskýrslurnar í [!INCLUDE[prod_short](includes/prod_short.md)] eru ekki tilbúnar til notkunar úr kassanum. Eftir því hvernig fjárhagsreikningar, víddir, fjárhagsreikningaflokkar og áætlanir eru settar upp skal leiðrétta sýnilínu- og dálkskilgreiningar og fjárhagsskýrslur sem nota þær til samræmis við uppsetninguna.

## Nota flokka fjárhagsreikninga til að breyta útliti ársreikninga

Hægt er að nota lykiltegundir fjárhagsreikninga til að breyta sniði fjárhagsskýrslna. T.d. þegar reikningaflokkar hafa verið settir upp á síðunni **Flokkar** fjárhagsreikninga, er hægt að velja aðgerðina **Mynda fjárhagsskýrslu** og uppfæra undirliggjandi fjárhagsskýrslur fyrir almennar fjárhagsskýrslur. Næst þegar keyrð er önnur þessara skýrslna, svo sem **Stöðuyfirlitsskýrsla**, nýjar samtölur og undirfærslur er bætt við.

Annar ávinningur af því að nota fjárhagsreikningaflokka yfir hráa fjárhagsreikninga í línuskilgreiningum er að breyting á uppbyggingu bókhaldslykils hefur engin áhrif á fjárhagsskýrslur.

> [!NOTE]
> Efsta stigs reikningsflokkarnir, svo sem **Skuldahnútur**, eru fastir og ekki er hægt að bæta við eigin. Hins vegar er hægt að eyða og bæta við reikningsflokkum á neðri stigum til að skilgreina hvernig tengt fjárhagsskýrsla birtist í skýrslum.
>
> Þú ættir að stofna og skipuleggja eigin lægri flokka fjárhagsreikninga frá grunni, í stigveldi ef þörf er á, frekar en að reyna að endurraða þeim sem fyrir eru. Til dæmis er hægt að endurhanna **Skuldir** til að innihalda nýtt **Eigið fé** og síðan **Skammtímaskuldir** og **Langtímaskuldir**. Nánari upplýsingar um [vörpun fjárhagsreikninga í lykilflokka](finance-general-ledger.md#account-categories).

## Bestu venjur til að vinna með línuskilgreiningar

Línuskilgreiningar eru ekki útgáfaðar. Þegar línuskilgreiningu er breytt er gömlu útgáfunni skipt út þegar breytingin er vistuð í gagnagrunninum. Eftirfarandi listi inniheldur nokkrar bestu venjur til að vinna með línuskilgreiningar:

- Ef línuskilgreiningum er bætt við skal velja góðan kóta og fylla út lýsingarreitinn með mikilvægum texta á meðan notandi veit enn hvað línuskilgreiningin er notuð fyrir. Þessar upplýsingar auðvelda samstarfsfólki þínu (og framtíðar sjálfum þér) að vinna við fjármálaskýrslugerð og breyta kannski línuskilgreiningunni.
- Áður en línuskilgreiningu er breytt skal íhuga að taka afrit af henni sem öryggisafrit, ef breytingin virkar ekki eins og búist er við. Annaðhvort er hægt að afrita skilgreininguna (gefa henni gott heiti) eða flytja hana út. Nánari upplýsingar eru í [Flytja inn eða út línuskilgreiningar](#import-or-export-financial-reporting-row-definitions).
- Ef þörf er á fersku eintaki af skilgreiningu sem [!INCLUDE[prod_short](includes/prod_short.md)] útvegar er auðvelt að fá það til að stofna nýtt fyrirtæki sem inniheldur aðeins uppsetningargögn. Síðan skal flytja skilgreininguna út og flytja hana inn í fyrirtækinu þar sem skilgreiningin þarfnast endurnýjunar.

## Línuskilgreiningar fyrir inn- eða útflutning fjárhagsskýrslugerðar

Hægt er að flytja inn og út fjárhagslínuskilgreiningar sem RapidStart skilgreiningarpakka. Til dæmis eru grunnstillingarpakkar gagnlegir til að deila upplýsingum með öðrum fyrirtækjum. Pakkinn er búinn til í .rapidstart-skrá, sem þjappar innihaldinu saman.

> [!NOTE]
> Þegar línuskilgreiningar fjárhagsskýrslugerðar eru fluttar inn koma fyrirliggjandi færslur með sömu heitum og þær sem verið er að flytja inn með nýju skilgreiningunum. Skilgreiningarpakkinn fyrir skýrsluskilgreiningu skrifar ekki yfir fyrirliggjandi línu- eða dálkskilgreiningar sem eru notaðar í skýrsluskilgreiningunni.

Til að flytja inn og út línuskilgreiningar fjárhagsskýrslu skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **línuskilgreiningar** og velja síðan viðeigandi tengil.
1. Veljið línuskilgreininguna og veljið svo aðgerðina **Flytja inn** línuskilgreiningu eða **Útflutningslínuskilgreiningu** eftir því hvað á að gera.

## Sjá einnig .

[Dálkaskilgreiningar í fjárhagsskýrslugerð](bi-column-definitions.md)  
[Undirbúa fjárhagsskýrslur](bi-how-work-account-schedule.md)  
[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
