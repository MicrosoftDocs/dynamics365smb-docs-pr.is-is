---
title: Greina gögn eftir víddum| Microsoft Docs
description: Lýsir því hvernig skal greina ýmis viðskiptagögn eftir víddum.
services: project-madeira
documentationcenter: ''
author: edupont
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ea949363506e9bc0d9bb3a1a4d53937501e8a5bb
ms.sourcegitcommit: cbd00f24fb471381bbfd64670237eda176bd78e5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947389"
---
#  <a name="analyze-data-by-dimensions"></a>Greina gögn eftir víddum
Í fjárhagsgreiningu er vídd tiltekin gögn sem má bæta við færslu sem einskonar merki. Þessi gögn eru notuð til að flokka saman færslur með svipuð einkenni, eins og viðskiptamenn, svæði, vörur og sölumenn og sækja þessa hópa á auðveldan hátt til greiningar. Víddir má nota fyrir færslur í færslubókum, skjölum og fjárhagsáætlunum. Heitið vídd lýsir því hvernig greiningin fer fram. Tvívíð greining gæti til dæmis verið sala eftir svæðum. Hins vegar er hægt að framkvæma flóknari greiningar með því að nota fleiri en tvær víddir þegar færsla er stofnuð, til dæmis sölu á hverja söluherferð, hvern viðskiptamann á hverju svæði. Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).

Gagnagreining með víddum gefur meiri innsýn í viðskiptin fyrir mat á upplýsingum, t.d. hversu vel fyrirtækið starfar, hvar því gengur vel eða illa og hvar ætti að ráðstafa meiri forða.

> [!TIP]
> Hægt er að greina færslugögn út frá víddum á skjótan hátt með því að afmarka samtölur á bókhaldslyklum og færslum á öllum **Færslur** síður út frá víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.

> [!NOTE]
> Ef kemur í ljós að röng vídd hafi verið notuð í bókuðum fjárhagsfærslum er hægt að leiðrétta víddargildin og uppfæra greiningaryfirlitið. Frekari upplýsingar eru í [Úrræðaleit og víddarleiðrétting](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="to-set-up-an-analysis-view"></a>Að setja upp greiningaryfirlit  
Greining eftir víddum sýnir valda samsetningu vídda. Hægt er að geyma og sækja hverja greiningu sem sett hefur verið upp. Upplýsingar um uppsetningu greiningar eru geymdar í **greiningaryfirlit** spjaldi til að einfalda greiningu seinna.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiningaryfirlit** og veldu síðan tengda tengilinn.  
2. Á síðunni **Listi yfir greiningaryfirlit** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að bæta öðrum víddarkóðum við þá fjóra sem fyrir eru á flýtiflipanum **Víddir** er aðgerðin **Afmörkun** valin, reitirnir fylltir út og síðan er smellt á **Í lagi** hnappinn.  
5. Til að uppfæra yfirlitið er valin aðgerðin **Uppfæra**.

## <a name="to-analyze-by-dimensions"></a>Að greina eftir víddum
Hægt er að nota fylkið **Greining eftir víddum** til að skoða upphæðirnar í fjárhag með því að nota greiningaryfirlitin sem þegar eru uppsett. Fyllt er á síðunni **Greining eftir víddum** til að skilgreina hvað fylkið sýnir og síðan er valin aðgerðin **Sýna fylki** til að skoða fylkið.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiningaryfirlit** og veldu síðan tengda tengilinn.  
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Greining eftir víddum**.
3. Efst á síðunni **Greining eftir víddum** skal fylla inn í reitina til að skilgreina hvað birtist.
4. Veljið aðgerðina **Sýna fylki** til að opna viðeigandi fylkissíðu fyrir skilgreint greiningaryfirlit.
5. Til að sjá lýsingu á upphæð sem er sýnd á fylkissíðunni er upphæðin valin sem á að kafa niður í.  

- Í dálkunum til vinstri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem línur** í hausnum.  
- Í dálkunum lengst til hægri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem dálka** í hausnum.

> [!IMPORTANT]  
>   Ekki er hægt að velja styttra tímabil en tímabil sem er skilgreint fyrir dagsetningarþjöppun á spjaldinu **Greiningaryfirlit**. Skipanirnar **Næsta safn** og **Fyrra safn** eru óvirkar ef valið var **Tímabil** , annaðhvort í reitnum **Sýna sem línur** eða **Sýna sem dálkar**.  

> [!NOTE]  
>   Hægt er að nota skýrsluna **Víddir - Sundurliðun** til að sýna ítarlega flokkun á notkun vídda í færslum á tilteknu tímabili. Hægt er að nota skýrsluna **Víddir - Heild** til að sýna aðeins heildarupphæðirnar.  

> [!TIP]  
>   Einnig er hægt að breyta útlitinu með því að breyta innihaldi reitanna **Sýna sem línur** og **Sýna sem dálka** . Til að snúa við yfirlitsstillingu, skal velja aðgerðina **Snúa við línum og dálkum**.

## <a name="to-update-an-analysis-view"></a>Að uppfæra greiningaryfirlit  
Upphæðirnar sem sýndar eru á síðunni **Greining eftir víddum** gefa mynd af stöðu fyrirtækisins við síðustu uppfærslu. Til að sjá mynd af núverandi stöðu verður að uppfæra greiningaryfirlitið með því að keyra uppfærsluaðgerðina.

Eftirfarandi aðgerð er til að uppfæra greiningaryfirlit af síðunni **Greining eftir víddum** . Skrefin eru svipuð og á síðunum **Greiningaryfirlitsspjald** og **Greiningaryfirlitslisti**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiningaryfirlit** og veldu síðan tengda tengilinn.
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Greining eftir víddum**.
2. Á síðunni **Greining eftir víddum** skal velja reitinn **Kóði greiningaryfirlits**.  
3. Línan með viðeigandi greiningaryfirliti er valin.  
4. Á síðunni **Greiningaryfirlit** skal velja greiningaryfirlitið og síðan velja aðgerðina **Uppfæra**.  

> [!TIP]  
>   Ef gátreiturinn **Uppfæra við bókun** er valinn á greiningaryfirlitsspjaldi, uppfærist yfirlitið sjálfkrafa þegar tengd færsla er bókuð.

> [!NOTE]  
>   Til að uppfæra sum eða öll greiningaryfirlit á sama tíma, þarf að nota runuvinnsluna **Uppfæra greiningaryfirlit**.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með víddir](finance-dimensions.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]