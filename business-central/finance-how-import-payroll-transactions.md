---
title: Flytja inn launafærslur
description: 'Þegar launum er stjórnað, eru fjárhagsfærslur fluttar inn og bókaðar frá launaveitu til fjárhags, með því að nota launaviðbætur eins og Ceridian.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 08/09/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="import-payroll-transactions"></a>Flytja inn launafærslur

Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag. Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir á síðuna **Færslubók**. Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga. Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.

> [!NOTE]  
> Til að nota þessa aðgerð þarf viðbót fyrir innflutning launa að vera uppsett og virkjuð. The Ceridian Payroll og Quickbooks Payroll File Import eftirnafn eru fyrirfram uppsett í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[prod_short](includes/prod_short.md)] Nota viðbætur](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Til að flytja inn launaskrá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Í viðkomandi færslubókarkeyrslu skal velja **Flytja inn launafærslur**. Uppsetning með hjálp opnast.
3. Fylgdu skrefunum á síðunni **Flytja inn launafærslur**.

    > [!TIP]  
    >   Í liðnum þar sem ytri launaskrám er varpað í fjárhagsreikningana þína man kerfið þá vörpun næst þegar sömu skýrslur eru fluttar inn. Þetta sparar tíma því ekki þarf að fylla handvirkt inn svæðið **Reikningnúmer** í færslubókinni í hvert skipti sem þú hefur flutt inn ítrekaða launafærslu.   

    Þegar hnappurinn **Í lagi** er valinn í uppsetningu með leiðsögn er síðan **Almenn færslubók** fullur af línum sem tákna færslurnar sem launaskráin innheldur og búið er að fylla út tilheyrandi lykla í reitunum **Fjárhagsreikningur** í samræmi við þá vörpun sem gerð var í leiðsögninni.
4. Breyta skal eða bóka færslubókarlínur líkt og fyrir allar aðrar færslur í fjárhag. Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)    
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)    
[Vinna í færslubókum](ui-work-general-journals.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
