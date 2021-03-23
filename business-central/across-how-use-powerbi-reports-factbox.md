---
title: Birta sérstillta Power BI-skýrslur fyrir Business Central Data| Microsoft docs
description: Hægt er að nota Power BI skýrslur til að öðlast frekari innsýn í gögnum í listum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6c818940357ed21a994e7553517989a0c16accec
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379274"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Býr til Power BI skýrslur til að birta listagögn í [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] inniheldur stjórneiningu fyrir upplýsingakassa á mörgum veigamiklum listasíðum sem veita frekari innsýn í gögnin í listanum. Þegar farið er milli lína í listanum er skýrslan uppfærð og síuð fyrir valda færslu. Hægt er að búa til sérsniðnar skýrslur til að birta í þessari stjórnun. Hins vegar eru fáar reglur til staðar til að tryggja að skýrslur virki eins og til er ætlast.  

## <a name="prerequisites"></a>Frumskilyrði

- Power BI-Reikningur.
- Power BI Desktop.

Frekari upplýsingar um það hvernig þú hefst handa má finna í [Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Skilgreining gagnasamstæðu skýrslu

Tilgreina gagnagjafann sem inniheldur gögnin sem tengjast listanum. Ef þú vilt t.d. stofna skýrslu fyrir sölulista skal tryggja að gagnamengið innihaldi upplýsingar sem tengjast sölu.  

## <a name="defining-the-report-filter"></a>Skilgreining á afmörkun skýrslu

Til að gera gagnauppfærslu í valinni færslu á listanum er síu bætt við skýrslu. Sían verður að innihalda reit gagnagjafans sem er notaður sem *aðallykill*. Í flestum tilvikum er aðallykill fyrir lista reiturinn **Nr.** .

Til að skilgreina afmörkun í skýrslunni er aðallykill af listanum yfir tiltæki reitir valinn og síðan er sá reitur dregill og sleppt yfir í hlutann **Afmörkun skýrslu**. Sían verður að vera grunnskýrslusía sem er skilgreind fyrir allar síður. Það getur ekki verið síða, sjónrænt eða ítarleg sía.

![Afmörkun skýslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Stærð og litur skýrslu valin

Stærð skýrslu verður að stilla á 325 sinnum 310 pixla. Þessi stærð býður upp á rétta kvörðun á skýrslu í tiltæku bili í Power BI stjórnun upplýsingareits í [!INCLUDE[prod_short](includes/prod_short.md)]. Til að skilgreina stærð skýrslu skal staðsetja fókus utan svæðis fyrir útlit skýrslu og velja svo tákn fyrir málningarrúllu.

![Breidd og hæð skýrslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Hægt er að breyta breidd og hæð skýrslunnar með því að velja **Sérsníða** í reitnum **Tegund**.

Ef bakgrunnur skýringarinnar á að vera með bakgrunnslit Power BI upplýsingareitsins skal stilla bakgrunnslit skýrslu á *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Notkun á skýrslum með mörgum síðum

Með Power BI er hægt að stofna eina skýrslu með mörgum síðum. Fyrir skýrslur sem birtast með listasíðum mælum við hins vegar ekki með því að þær séu með fleiri en eina síðu. Power BI upplýsingareiturinn sýnir aðeins fyrstu síðu skýrslunnar.

## <a name="naming-the-report"></a>Gefa skýrslunni heiti

Gefa skal skýrslunni heiti sem inniheldur heiti listasíðunnar sem tengist skýrslunni. Ef skýrsla er t.d. fyrir listasíðuna **Lánardrottinn** skal innihalda orðið *lánardrottinn* einhvers staðar í heitinu.  

Þessi nafnavenja er ekki skilyrði. Hins vegar gerir það val á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)] fljótlegri. Þegar skýrsluvalssíða opnast af listasíðu er hún síuð sjálfkrafa út frá síðuheitinu. Þessi sía er búin til að takmarka skýrslurnar sem eru birtar. Einnig er hægt að fjarlægja afmörkunina til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.  

## <a name="fixing-problems"></a>Vandamál lagfærð

Þessi hluti veitir hjáleið fyrir flest dæmigerð vandamál sem komið geta upp þegar Power BI-skýrsla er búin til.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Ekki er hægt að sjá skýrslur á síðunni „Velja skýrslur“

Það er líklega vegna þess að heiti skýrslunnar inniheldur ekki heiti listasíðunnar. Hreinsaðu síuna til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Verið er að hlaða skrá en hún er tóm, ekki síuð eða síuð á rangan hátt

Sannprófa verður að skýrsluafmörkunin innihaldi réttan aðallykil. Yfirleitt er þessi reitur **Nr.** reitur, en í töflunni **Fjárhagsfærsla**, til dæmis, verður að nota **Færslunr.** reitinn.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Skýrslu er hlaðið inn, en hún sýnir síðu sem þú bjóst ekki við

Sannprófa verður að skýrslan sem notandi vill að birtist sé fyrsta síðan í skýrslunni.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Skýrsla birtist með óæskilegum gráum ramma eða hún er of lítill eða of stór

Staðfestið að stærð skýrslu sé stillt á 325 x 310 pixla. Vista skal skýrsluna og síðan endurnýja listasíðuna.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Gera viðskiptagögn þín virk fyrir Power BI](admin-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Hafist handa](product-get-started.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]