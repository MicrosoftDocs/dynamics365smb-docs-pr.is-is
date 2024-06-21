---
title: Fjárhagsáætlanir stofnaðar
description: Lýsir því hvernig á að stofna fjárhagsáætlanir til að spá fyrir um mismunandi fjármálaaðgerðir og úthluta víddum fyrir viðskiptaupplýsingar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Stofna fjárhagsáætlanir

Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum. Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn. Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.  

Þegar áætlun er stofnuð er hægt að úthluta áætlunarvíddum, sem kallast áætlanavíddir, fyrir hana. Hægt er að nota áætlanavíddir til að setja afmarkanir á áætlun og til að bæta víddaupplýsingum við áætlunarfærslur. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Fjárhagsáætlanir gegna mikilvægu hlutverki í viðskiptagreind. Sem dæmi má nefna fjárhagsyfirlit sem byggir á fjárhagsskýrslum sem innihalda færslur fjárhagsáætlunar eða þegar upphæðir fjárhagsáætlunar samanborið við raunverulegar upphæðir eru greindar í bókhaldslyklinum. Frekari upplýsingar er að finna í [Viðskiptagreind](bi.md).

Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt. Frekari upplýsingar má finna í [Stofna kostnaðaráætlanir](finance-create-cost-budgets.md).  

## Að búa til nýja fjárhagsáætlun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsáætlanir** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Breyta lista**, fylltu svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja skal aðgerðina **Breyta fjárhagsáætlun**.
4. Efst á síðunni **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.  

   Á síðunni birtast aðeins færslur með heiti áætlunar sem ritað var í reitinn **Heiti** áætlunar. Þar sem heiti áætlunar var stofnað eru engar færslur sem samsvara afmörkuninni. Síðan er þar af leiðandi tóm.  
5. Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu. Síðan **Fjárhagsáætl.færslur** opnast.  
6. Ný lína er búin til og reiturinn **Upphæð** fylltur út. Loka síðunni **Fjárhagsáætlunarfærslur**.  
7. Þrep 5 og 6 eru endurtekin fyrir allar upphæðir í áætluninni.  

> [!NOTE]  
> Á flýtiflipanum **Afmarkanir** geturðu afmarkað upplýsingar um fjárhagsáætlun með fjárhagsáætlunarvíddum, sem hafa verið settar upp undir heiti fjárhagsáætlunar.

## Útflutningur og innflutningur fjárhagsáætlana með Excel

Eins og fyrir nánast allar aðrar síður getur þú flutt út gögn á síðum fjárhagsáætlunar til Microsoft Excel til frekari vinnslu eða greiningu. Frekari upplýsingar eru í [Flutningur viðskiptagagna í Excel](about-export-data.md).

> [!NOTE]
> Bókhaldslykillinn sem fjárhagsáætlanir eru byggðar á, hefur línur af reikningstegundinni Fyrirsögn. Í þessum línum er samtala línanna fyrir neðan hana. Þegar fjárhagsáætlun er flutt út eru gögn flutt út í öllum línum án tillits til reikningstegundarinnar. Hins vegar er aðeins hægt að flytja inn gögn í línur af tegundinni Bókunarreikningur.

Á sama hátt er gildum í hauslínum eytt þegar fjárhagsáætlun er flutt inn. Þeim er eytt til að forðast rangar samtölur eftir að gögn sem voru flutt inn eða þeim breytt í Excel hafa verið flutt inn eða þeim breytt.

### Aðstæður

Þú veist að nýi áætlaði launakostnaðurinn kemur til með að vera 1.200.000 í staðbundnum gjaldmiðli (SGM). Þú vilt gera launadeildinni kleift að gera fjárhagsáætlun fyrir þessar þrjár tilteknu línur (af lyklagerðinni bókun) fyrir starfsmenn í fullu starfi, starfsmenn í hlutastarfi og tímabundna aðstoð. Línurnar þrjár eru flokkaðar undir fyrirsagnarlínu launa.

Fært er inn 1.200.000 í fyrirsögnina, áætlunin flutt út í Excel, hún síðan send í deild launa og sagt þeim að dreifa SGM 1.200.000.

Launadeildin úthlutar upphæðinni á bókunarlyklana þrjá. Þegar þú flytur aftur inn í fjárhagsáætlun er fyllt út í lyklana þrjá með nýju Excel-gögnunum, sem verður samanlagt 1.200.000 SGM og fyrirsagnarlínan er auð.

## Sjá einnig .

[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Fjármál](finance.md)  
[Viðskiptaupplýsingar](bi.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
