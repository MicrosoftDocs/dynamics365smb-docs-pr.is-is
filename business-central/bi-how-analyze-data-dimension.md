---
title: Greina gögn eftir víddum
description: Þessi grein lýsir því hvernig hægt er að greina viðskiptagögn eftir víddum til að fá betri innsýn í reksturinn.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="analyze-data-by-dimensions" />Greina gögn eftir víddum

Í fjárhagsgreiningu er vídd tiltekin gögn sem má bæta við færslu sem einskonar merki. Þessi gögn eru notuð til að flokka saman færslur með svipuð einkenni, eins og viðskiptamenn, svæði, vörur og sölumenn og sækja þessa hópa á auðveldan hátt til greiningar. Víddir má nota fyrir færslur í færslubókum, skjölum og fjárhagsáætlunum. 

Hver „vídd“ lýsir áherslu greiningar. Tvívíð greining gæti því til dæmis verið sala eftir svæðum. Hægt er að framkvæma flóknari greiningar með því að nota fleiri en tvær víddir þegar færsla er stofnuð, til dæmis sölu á hverja söluherferð, hvern viðskiptamann á hverju svæði. Þetta gefur þér betri innsýn í viðskiptin, t.d. hversu vel fyrirtækið starfar, hvar því gengur vel eða illa og hvar ætti að ráðstafa meiri forða, svo þú getir tekið upplýstari ákvarðanir í framhaldinu. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

> [!TIP]
> Hægt er að greina færslugögn út frá víddum á skjótan hátt með því að afmarka samtölur á bókhaldslyklum (COA) og færslum á öllum **Færslur** síður út frá víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.

> [!NOTE]
> Ef kemur í ljós að rangt víddargildi hafi verið notuð í bókuðum fjárhagsfærslum er hægt að leiðrétta þau og uppfæra greiningaryfirlitin. Fáðu frekari upplýsingar í hlutanum [Úrræðaleit og víddarleiðréttingar](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view" />Setja upp greiningaryfirlit

Greining eftir víddum notar valda samsetningu af víddum. Þú geymir, sækir og uppfærir þessa vídd með því að búa til **Greiningaryfirlitsspjald**. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiningaryfirlit**, velja síðan viðkomandi tengil.  
2. Á síðunni **Listi yfir greiningaryfirlit** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að bæta öðrum víddarkóðum við þá fjóra sem fyrir eru á flýtiflipanum **Víddir** er aðgerðin **Afmörkun** valin, reitirnir fylltir út og síðan er smellt á **Í lagi** hnappinn.  
5. Til að uppfæra yfirlitið er valin aðgerðin **Uppfæra**.

## <a name="analyze-by-dimensions" />Greina eftir víddum

Notaðu greiningaryfirlit sem þegar hafa verið sett upp með fylkinu **Greining eftir víddum** til að skoða upphæðirnar í fjárhagnum.   

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiningaryfirlit**, velja síðan viðkomandi tengil.  
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Greining eftir víddum**.
3. Efst á síðunni **Greining eftir víddum** skal fylla inn í reitina til að skilgreina hvað birtist.
4. Veljið aðgerðina **Sýna fylki** til að opna viðeigandi fylkissíðu fyrir skilgreint greiningaryfirlit.
5. Til að sjá lýsingu á upphæð sem er sýnd á fylkissíðunni er upphæðin valin sem á að kafa niður í.  

- Í dálkunum til vinstri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem línur** í hausnum.  
- Í dálkunum til hægri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem dálka** í hausnum.

> [!IMPORTANT]  
> Ekki er hægt að velja styttra tímabil en tímabil sem er skilgreint fyrir dagsetningarþjöppun á spjaldinu **Greiningaryfirlit**. Skipanirnar **Næsta safn** og **Fyrra safn** eru óvirkar ef valið var **Tímabil** í annaðhvort reitnum **Sýna sem línur** eða **Sýna sem dálka**.  

> [!NOTE]  
> Hægt er að nota skýrsluna **Víddir - Sundurliðun** til að sýna ítarlega flokkun á notkun vídda í færslum á tilteknu tímabili. Hægt er að nota skýrsluna **Víddir - Heild** til að sýna aðeins heildarupphæðirnar.  

> [!TIP]  
> Einnig er hægt að breyta útlitinu með því að breyta innihaldi reitanna **Sýna sem línur** og **Sýna sem dálka** . Til að snúa við yfirlitsstillingu, skal velja aðgerðina **Snúa við línum og dálkum**.

## <a name="update-an-analysis-view" />Uppfæra greiningaryfirlit

Upphæðirnar sem sýndar eru á síðunni **Greining eftir víddum** gefa mynd af stöðu fyrirtækisins við síðustu uppfærslu. Til að sjá mynd af núverandi stöðu verður að uppfæra greiningaryfirlitið með því að keyra uppfærsluaðgerðina.

Notaðu eftirfarandi aðferð til að uppfæra greiningaryfirlit af síðunni **Greining eftir víddum**. Skrefin eru svipuð þeim sem notuð eru við að uppfæra síðurnar **Spjald greiningaryfirlits** og **Listi greiningaryfirlits**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiningaryfirlit**, velja síðan viðkomandi tengil.
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Greining eftir víddum**.
3. Á síðunni **Greining eftir víddum** skal velja reitinn **Kóði greiningaryfirlits**.  
4. Línan með viðeigandi greiningaryfirliti er valin.  
5. Á síðunni **Greiningaryfirlit** skal velja greiningaryfirlitið, síðan velja aðgerðina **Uppfæra**.  

> [!TIP]  
> Ef gátreiturinn **Uppfæra við bókun** er valinn á greiningaryfirlitsspjaldi, uppfærist yfirlitið sjálfkrafa þegar tengd færsla er bókuð.

> [!NOTE]  
> Til að uppfæra sum eða öll greiningaryfirlit á sama tíma, þarf að nota runuvinnsluna **Uppfæra greiningaryfirlit**.  

## <a name="see-related-training-at-microsoft-learnlearnmodulesdimensions-financial-reports-dynamics--business-centralindex" />Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index).

## <a name="see-also" />Sjá einnig .

[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með víddir](finance-dimensions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
