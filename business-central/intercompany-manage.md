---
title: Vinna með millifyrirtækjafærslur
description: Með milli-fyrirtækjavirkninni getur einfaldað fyrirtækjaferli og færslur á milli dótturfyrirtækja innan sama fyrirtækis.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 08/11/2021
ms.author: edupont
ms.openlocfilehash: 19fa804213d4f0a66a92a9febb157f2b5da23ec2
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440564"
---
# <a name="managing-intercompany-transactions"></a>Vinna með millifyrirtækjafærslur

Eiginleikar færsla milli fyrirtækja eru hannaðar fyrir notendur sem stýra fleiri en einni löglegri viðskiptaeiningu og hafa stofnað mörg fyrirtæki til að aðskilja bókhald þessara eininga. Þessi lýsing á við um marga notendur, sérstaklega þá sem vinna á alþjóðlegum markaði eða svæðum sem hafa mörg ólík viðskipta- og reglugerðaumhverfi.

Fyrirtækið gæti verið samansett úr mörgum dótturfyrirtækum án þess að hafa sama fjölda bókahalds- og stjórnunarteyma. Færslur milli fyrirtækja einfalda ferli í rekstri og færslur milli eininga.

Þegar byrjað er að nota færslur milli fyrirtækja verða viðskipti við dótturfyrirtæki og innri fyrirtækjafélaga jafn einföld og samskipti við lánardrottna og viðskiptamenn. Færslur milli fyrirtækja eru aðeins færðar einu sinni í viðeigandi skjal. Notandinn getur notað þær aðgerðir sem hann er vanur, til dæmis stjórnun á útgjöldum og gjaldfærðum skuldum. Vörpunaraðgerðir fyrir bókhaldslykla og víddir tryggja að upplýsingarnar birtist á réttum stað.  

Fjórir helstu kostir milli fyrirtækjavirkninnar eru:  

- Tímasparnaður og einfaldari færslur auka afköst  
- Minni hætta á villum - færslur aðeins færðar inn í eitt skipti og sjálfvirkar uppfærslur á heildarkerfinu  
- Fullt eftirlit með ferli endurskoðana, viðskipta og færslna  
- Skilvirkar og hagkvæmar færslur í samskiptum við hlutdeildarfélög eða dótturfyrirtæki  

## <a name="streamlining-the-flow-of-business-activities"></a>Einfaldari viðskiptahættir  

Með færslum milli fyrirtækja er hægt að senda sölu- og innkaupaskjöl sem og fjárhagsfærslur á skrifstofur í öðrum löndum, söluskrifstofur eða dótturfyrirtæki, allt í gegnum forritið. Þar sem ekki þarf að færa gögn inn endurtekið og senda, taka á móti, prenta og skrá sölu og innkaup á pappír sparast tími og skilvirkni eykst.  

Færsluskjölum má stjórna algjörlega. Til dæmis er hægt að hafna fylgiskjali sem þú hefur fengið sent og því rangar bókanir Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar. Einnig er hægt að uppfæra innkaupapöntun þegar keypt er frá félaga eða hlutdeildarfyrirtæki, svo lengi sem sölufyrirtækið hefur ekki afhent vörur.  

Þegar færsla er færð inn þarf ekki að tilgreina reikningana fyrir stök söfn bóka, heldur þarf aðeins að gefa upp kenni samstarfsfyrirtækisins. Milli-fyrirtækjavirknin býr til færslubókarlínur sem leiða til réttrar stöðu reikninga beggja fyrirtækjanna sem eiga hlut að færslu. Í Útistandandi og viðskiptaskuldir er MF-félagakóta úthlutað á hvaða viðskiptamann eða lánardrottin sem er. Pantanir og reikningar sem eiga við færslur til eða frá þessum félögum stofna þaðan í frá samsvarandi skjöl hjá fyrirtækjafélögum svo að staða reikninganna verði rétt.  

Aðgerðir færslur milli fyrirtækja eru hannaðar til að auðvelda færslur milli fyrirtækja með sölu- og innkaupaskjölum og línum færslubókarinnar. Færslur milli fyrirtækja leyfa færslur milli fyrirtækja úr mörgum [!INCLUDE [prod_short](includes/prod_short.md)] gagnagrunnum, löndum/svæðum, bókhaldslyklum víddum og vörunúmerum.  

Í færslum milli fyrirtækja eru margar færslur og mörg skjöl notuð:  

- Færslur í færslubók
- Innkaupa- og sölupantanir
- Innkaupa- og sölureikningar
- Kreditreikningar
- Skilapantanir

Þegar færslur milli fyrirtækja eru stofnaðar er listi yfir MF-félaga búinn til sem kallast MF-félagar og bókhaldslykill fyrir þá. Því næst er hægt að búa til færslur milli fyrirtækja í færslubók. Víddir má setja upp aðskildar ef þess þarf.  

> [!NOTE]
> Almenna færslubókin inniheldur ekki aðgerðir fyrir gjaldmiðla heldur umreiknar allar upphæðir í SGM eða heimagjaldmiðilinn.

Eftir að samstarfsaðilar hafa verið settir upp sem viðskiptamenn og lánardrottnar í kerfinu og þeim úthlutað MF-félagakóta er hægt að deila innkaupa- og söluskjölum milli fyrirtækja, þar á meðal vörum og vörugjöldum. [!INCLUDE [prod_short](includes/prod_short.md)] styður færslur milli fyrirtækja úr mörgum gagnagrunnum, til dæmis í ólíkum löndum/svæðum, í ólíkum gjaldmiðlum, bókhaldslyklum, víddum og vörunúmerum.  

> [!NOTE]
> Ekki er hægt að skipta öllum tegundum gagna á milli fyrirtækja á þennan hátt. Innkaupreikningar eru ekki sendir til viðskiptafélaga í gegnum ferli milli fyrirtækja. En sölureikningar sem sendir eru inn í gegnum ferli milli fyrirtækja verða stofnaðir sem innkaupareikningar í móttökufyrirtækinu.

Að steypa saman fjárhagsgögnum getur einkum gagnast fyrir ferla innan samstæða. Frekari upplýsingar er að finna í [Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|Til að |Sjá|
|---|---|
|Stofna lánardrottna og viðskiptamenn millifyrirtækis sem svokallaða millifyrirtækjafélaga, og setja upp bókhaldslykil millifyrirtækis.|[Uppsetning milli fyrirtækja](intercompany-how-setup.md)|
|Milli-fyrirtækjaskjöl eða færslubækur eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga.|[Unnið með samstæðuskjöl og færslubækur](intercompany-how-work-documents-journals.md)|
|Skipuleggja og vinna færslur á inn- og útleið sem þú og millifyrirtækjafélagar þínir sendið ykkar á milli.|[Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur](intercompany-how-manage-intercompany-inbox.md)|
|Nota færslur milli fyrirtækja til að dreifa kostnaði á milli samstarfsfyrirtækja.|[Úthluta kostnaði til millifyrirtækjafélaga](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
