---
title: Greina gögn eftir víddum
description: Í þessari grein er lýst hvernig hægt er að greina viðskipagögn eftir víddum til að öðlast meiri innsýn í fyrirtæki.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 545, 555, 556, 557, 558, 9372, 9370, 9371
ms.date: 09/22/2022
ms.author: edupont
ms.openlocfilehash: 62c0cdbb3641ab55c58d5ce944591b2aeef7f059
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606252"
---
# <a name="analyze-data-by-dimensions"></a>Greina gögn eftir víddum

Í fjármálagreiningu er vídd gagna sem bætt er við færslu sem nokkurs konar merki. Þessi gögn eru notuð til að flokka saman færslur með svipuð einkenni, eins og viðskiptamenn, svæði, vörur og sölumenn og sækja þessa hópa á auðveldan hátt til greiningar. Víddir má nota fyrir færslur í færslubókum, skjölum og fjárhagsáætlunum. 

Hver "vídd" lýsir áherslum í greiningu. Svo myndi Tvívíð greining t.d. vera Sala á svæði. Með því að nota fleiri en tvær víddir við stofnun færslu er hægt að framkvæma flóknari greiningar, svo sem sölu á söluherferð fyrir hvern viðskiptavinaflokk fyrir hvert svæði. Sem gefur þér meiri innsýn í reksturinn, eins og hversu vel fyrirtæki þitt starfa, hvar það þrífst og hvar það er ekki, og hvar meira fjármagn á að úthluta, þannig að þú getir tekið upplýstar ákvarðanir um leið og þú hreyfir þig áfram. Lærðu meira í [vinnunni með víddum](finance-dimensions.md).

> [!TIP]
> Flýtileiðin til að greina færslugögn eftir víddum er að afmarka samtölur í bókhaldslyklum (COA) og færslum á öllum **færslum** síðum eftir víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.

> [!NOTE]
> Ef rangt víddargildi hefur verið notað í bókuðum fjárhagsfærslum er hægt að leiðrétta það og uppfæra greiningaryfirlit. Frekari upplýsingar eru [í hlutanum úrræðaleit og leiðrétting vídda](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view"></a>Setja upp greiningaryfirlit

Greining eftir víddum notar valda samsetningu vídda. Þú geymir, sækir og uppfærir Víddasamstæður **með því að stofna greiningaryfirlitskort**. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Greiningaryfirlit** og velja síðan tengda tengilinn.  
2. Á síðunni **Listi yfir greiningaryfirlit** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að bæta við öðrum víddarkóðum til viðbótar við fjórar á **fastflipanum víddir** er hægt að **Velja síuaðgerðina**, fylla út reitina og velja **síðan OK** hnappinn.  
5. Til að uppfæra yfirlitið er valin aðgerðin **Uppfæra**.

## <a name="analyze-by-dimensions"></a>Greina eftir víddum

Notið greiningaryfirlit sem þegar hafa verið sett upp með **víddunum Greining eftir víddum** til að skoða upphæðirnar í fjárhag.   

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Greiningaryfirlit** og velja síðan tengda tengilinn.  
2. Velja viðeigandi greiningaryfirlit og velja **síðan aðgerðina Greining eftir víddum**.
3. Efst á síðunni **Greining eftir víddum** skal fylla inn í reitina til að skilgreina hvað birtist.
4. Veljið aðgerðina **Sýna fylki** til að opna viðeigandi fylkissíðu fyrir skilgreint greiningaryfirlit.
5. Til að sjá lýsingu á upphæð sem er sýnd á fylkissíðunni er upphæðin valin sem á að kafa niður í.  

- Í dálkunum til að geyma upplýsingar eftir því hvað var valið í **reitnum Sýna sem línur** í hausnum.  
- Í hægridálkunum eru upplýsingar byggðar á því sem valið var í **reitnum Sýna sem dálka** í hausnum.

> [!IMPORTANT]  
> Ekki er hægt að velja styttra tímabil en tímabil sem er skilgreint fyrir dagsetningarþjöppun á spjaldinu **Greiningaryfirlit**. **Næstu mengi** og **fyrri stilltar** skipanir eru óvirkar ef þú hefur valið **tímabil** annaðhvort **í reitnum Sýna sem línur** eða **Sýna sem dálka**.  

> [!NOTE]  
> Hægt er að nota skýrsluna **Víddir - Sundurliðun** til að sýna ítarlega flokkun á notkun vídda í færslum á tilteknu tímabili. Hægt er að nota skýrsluna **Víddir - Heild** til að sýna aðeins heildarupphæðirnar.  

> [!TIP]  
> Einnig er hægt að breyta yfirliti með því að breyta innihaldi **Sýna sem lína** og **Sýna sem dálka**. Til að snúa við yfirlitsstillingu, skal velja aðgerðina **Snúa við línum og dálkum**.

## <a name="update-an-analysis-view"></a>Uppfæra greiningaryfirlit

Upphæðirnar sem birtast á **síðunni Greining eftir víddum** gefa mynd af ríki fyrirtækisins við síðustu uppfærslu. Til að sjá mynd af núverandi stöðu verður að uppfæra greiningaryfirlitið með því að keyra uppfærsluaðgerðina.

Notið eftirfarandi ferli til að uppfæra greiningaryfirlit frá **síðunni Greining eftir víddum**. Skrefin eru svipuð og þau sem eru til uppfærslu á **listasíðum** greiningaryfirlitsins **og** greiningaryfirliti.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Greiningaryfirlit** og velja síðan tengda tengilinn.
2. Velja viðeigandi greiningaryfirlit og velja **síðan aðgerðina Greining eftir víddum**.
3. Á síðunni **Greining eftir víddum** skal velja reitinn **Kóði greiningaryfirlits**.  
4. Línan með viðeigandi greiningaryfirliti er valin.  
5. **Á síðunni greiningaryfirlit** skal velja greiningaryfirlitið og velja **síðan uppfærsluaðgerðina**.  

> [!TIP]  
> Ef valið er að **Uppfæra í gátreitnum bókun** á spjaldi greiningaryfirlit uppfærist yfirlitið sjálfkrafa þegar tengd færsla er bókuð.

> [!NOTE]  
> Til að uppfæra sum eða öll greiningaryfirlit á sama tíma, þarf að nota runuvinnsluna **Uppfæra greiningaryfirlit**.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Upplýsingarit um Fjármál fyrirtækja](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með víddir](finance-dimensions.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
