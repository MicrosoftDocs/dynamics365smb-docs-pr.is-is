---
title: "Greina gögn eftir víddum| Microsoft Docs"
description: "Lýsir því hvernig skal greina ýmis viðskiptagögn eftir víddum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 94d783a806b56e972f16ebe1e0d383582cd72126
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
#  <a name="analyze-data-by-dimensions"></a>Greina gögn eftir víddum
Í fjárhagsgreiningu er vídd tiltekin gögn sem má bæta við færslu sem einskonar merki. Þessi gögn eru notuð til að flokka saman færslur með svipuð einkenni, eins og viðskiptamenn, svæði, vörur og sölumenn og sækja þessa hópa á auðveldan hátt til greiningar. Víddir má nota fyrir færslur í færslubókum, skjölum og fjárhagsáætlunum. Heitið vídd lýsir því hvernig greiningin fer fram. Tvívíð greining gæti til dæmis verið sala eftir svæðum. Hins vegar er hægt að framkvæma flóknari greiningar með því að nota fleiri en tvær víddir þegar færsla er stofnuð, til dæmis sölu á hverja söluherferð, hvern viðskiptamann á hverju svæði. Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).

Gagnagreining með víddum gefur meiri innsýn í viðskiptin fyrir mat á upplýsingum, t.d. hversu vel fyrirtækið starfar, hvar því gengur vel eða illa og hvar ætti að ráðstafa meiri forða.

> [!TIP]
> Hægt er að greina færslugögn út frá víddum á skjótan hátt með því að afmarka samtölur á bókhaldslyklum og færslum í öllum **Færslur** gluggum út frá víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.

## <a name="to-set-up-an-analysis-view"></a>Að setja upp greiningaryfirlit  
Greining eftir víddum sýnir valda samsetningu vídda. Hægt er að geyma og sækja hverja greiningu sem sett hefur verið upp. Upplýsingar um uppsetningu greiningar eru geymdar í **greiningaryfirlit** spjaldi til að einfalda greiningu seinna.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiningaryfirlit** og velja svo viðeigandi tengil.  
2. Í glugganum **Listi yfir greiningaryfirlit** skal velja aðgerðina **Nýtt**.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að bæta öðrum víddarkóðum við þá fjóra sem fyrir eru á flýtiflipanum **Víddir** er aðgerðin **Afmörkun** valin, reitirnir fylltir út og síðan er smellt á **Í lagi** hnappinn.  
5. Til að uppfæra yfirlitið er valin aðgerðin **Uppfæra**.

## <a name="to-analyze-by-dimensions"></a>Að greina eftir víddum
Hægt er að nota fylkið **Greining eftir víddum** til að skoða upphæðirnar í fjárhag með því að nota greiningaryfirlitin sem þegar eru uppsett. Fyllt er í gluggann **Greining eftir víddum** til að skilgreina hvað fylkið sýnir og síðan er valin aðgerðin **Sýna fylki** til að skoða fylkið.  

- Í dálkunum til vinstri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem línur** í hausnum.  
- Í dálkunum lengst til hægri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem dálka** í hausnum.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Greining eftir víddum** og velja svo viðeigandi tengil.  
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Breyta greiningaryfirliti**.
3. Efst í glugganum **Greining eftir víddum** skal fylla inn í reitina til að skilgreina hvað birtist.
4. 5. Til að sjá lýsingu á upphæð sem er sýnd í fylkisglugganum er smellt á upphæðina .  

> [!IMPORTANT]  
>   Ekki er hægt að velja styttra tímabil en tímabil sem er skilgreint fyrir dagsetningarþjöppun á spjaldinu **Greiningaryfirlit**. Skipanirnar **Næsta safn** og **Fyrra safn** eru óvirkar ef valið var **Tímabil** , annaðhvort í reitnum **Sýna sem línur** eða **Sýna sem dálkar**.  

> [!NOTE]  
>   Hægt er að nota skýrsluna **Víddir - Sundurliðun** til að sýna ítarlega flokkun á notkun vídda í færslum á tilteknu tímabili. Hægt er að nota skýrsluna **Víddir - Heild** til að sýna aðeins heildarupphæðirnar.  

> [!TIP]  
>   Einnig er hægt að breyta útlitinu með því að breyta innihaldi reitanna **Sýna sem línur** og **Sýna sem dálka** . Til að snúa við yfirlitsstillingu, skal velja aðgerðina **Snúa við línum og dálkum**.

## <a name="to-update-an-analysis-view"></a>Að uppfæra greiningaryfirlit  
Upphæðirnar sem sýndar eru í glugganum **Greining eftir víddum** gefa mynd af stöðu fyrirtækisins við síðustu uppfærslu. Til að sjá mynd af núverandi stöðu verður að uppfæra greiningaryfirlitið með því að keyra uppfærsluaðgerðina.

Eftirfarandi aðgerð er til að uppfæra greiningaryfirlit úr glugganum **Greining eftir víddum** . Skrefin eru svipuð og í gluggunum **Greiningaryfirlitsspjald** og **Greiningaryfirlitslisti**.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Greining eftir víddum** og velja svo viðeigandi tengil.  
2. Í glugganum **Greining eftir víddum** skal velja reitinn **Kóði greiningaryfirlits**.  
3. Línan með viðeigandi greiningaryfirliti er valin.  
4. Velja skal aðgerðina **Uppfæra**.  

> [!TIP]  
>   Ef gátreiturinn **Uppfæra við bókun** er valinn á greiningaryfirlitsspjaldi, uppfærist yfirlitið sjálfkrafa þegar tengd færsla er bókuð.

> [!NOTE]  
>   Til að uppfæra sum eða öll greiningaryfirlit á sama tíma, þarf að nota runuvinnsluna **Uppfæra greiningaryfirlit**.  

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með víddir](finance-dimensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

