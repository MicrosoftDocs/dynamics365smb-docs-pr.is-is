---
title: Stilling skýrsluútlitsins
description: Kynntu þér hvernig á að stilla útlitið sem notað er í skýrslu við forskoðun og prentun.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 08/12/2022
ms.author: jswymer
---
# <a name="setting-the-layout-used-by-a-report"></a>Stilling útlits sem skýrsla notar

> **Á VIÐ UM:** Business Central Online, Business Central á staðnum 2022 útgáfutímabil 1 og nýrra. Fyrir eldri útgáfur skaltu fara [hingað](ui-how-change-layout-currently-used-report.md).

Skýrsluútlit ákveður útlit skýrslunnar. Það stýrir því hvaða gagnareitir í gagnasafni skýrslu eru sýndir, hvernig þeim er raðað upp, stílsnið og fleira. Skýrsla getur verið með fleiri en eitt útlit sem hægt er að skipta á milli eftir þörfum.

Þegar mörg fyrirtæki eru í forritinu eru útlitin stillt fyrir hvert fyrirtæki fyrir sig. Þannig að sama skýrslan í einu fyrirtæki getur verið með annað útlit en í öðru fyrirtæki.

## <a name="get-started"></a>Hafist handa

Til eru nokkrar leiðir til að stilla hvaða útlit skýrsla notar. Hver leið hefur sína kosti, eftir því hvað leitast er við að gera: 

- Á síðu skýrslubeiðni

  Þegar skýrsla er sett upp til að keyra, inniheldur skýrslubeiðnisíðan reitinn **Skýrsluútlit** sem sýnir núverandi sjálfgefið útlit sem skýrslan notar. Hægt er að nota þennan reit til að skipta tímabundið yfir í annað tiltækt útlit fyrir skýrsluna sem þú ert að keyra. Þegar skýrslan hefur verið keyrð fer útlitið aftur yfir í sjálfgefna útlitið. Nánari upplýsingar eru í [Keyra og prenta skýrslur](ui-work-report.md#switching-the-report-layout)þ

- Á síðunni **Val á útliti skýrslu**

  Síðan **Val á útliti skýrslu** sýnir lista yfir allar skýrslur. Þessi síða gefur til kynna hvernig sjálfgefið útlit skýrslu er. Hún gerir þér kleift að stilla útlit í mismunandi fyrirtækjum án þess að þurfa að skipta úr fyrirtækinu sem unnið er í.

- Frá síðunni **Skýrsluútlit** sýnir síðan **Skýrsluútlit** öll tiltæk útlit fyrir hverja skýrslu í núverandi fyrirtæki. Hún er einnig notuð til að tilgreina sjálfgefið útlit fyrir skýrslur. Auðvelt er að finna ákveðið útlit með því að raða eða sía listann. Þegar þú finnur útlitið geturðu stillt það fyrir skýrsluna með einu vali.

  > [!NOTE]
  > Þú getur ekki notað síðuna **Skýrsluútlit** fyrir Word- og RDLC-útlit sem var búið til með því að nota eldri eiginleikann af **Sérsniðnum útlitum**. Í raun sérðu ekki einu sinni þessi sérsniðnu útlit sem gefin eru upp á síðunni **Skýrsluútlit**. Fyrir þessi útlit er aðeins hægt að stilla þau með því að nota síðuna **Val á útliti skýrslu**.

## <a name="set-the-layout-from-the-report-layouts-page"></a>Stilla útlit á síðu skýrsluútlits

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Finndu útlitið í listanum, veldu það og veldu svo aðgerðina **Stilla sjálfgefið** efst á síðunni.

## <a name="set-the-layout-from-report-layout-selection-page"></a>Stilla útlitið á valsíðu skýrsluútlits

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Val á skýrsluútliti** og velja síðan viðkomandi tengil.
  
   Síðan sýnir allar skýrslur sem eru tiltækar fyrir fyrirtækið sem tilgreint er í reitnum **Fyrirtæki** efst á síðunni. Reiturinn **Lýsing á útliti** tilgreinir útlitið sem skýrslan notar sem stendur.
2. Stilltu reitinn **Fyrirtæki** efst á fyrirtækið með skýrsluna.
3. Finndu og veldu skýrsluna í listanum og gerðu síðan eitt af eftirfarandi skrefum:

   - Ef útlitið sem þú vilt skipta yfir í er af annarri gerð en núverandi útlit skaltu velja reitinn **Útlit**, síðan velja gerð útlitsins sem þú vilt stilla í skýrslunni. 
   - Ef útlitið sem þú vilt skipta yfir í er af sömu gerð og núverandi útlit skaltu velja aðgerðina **Velja útlit** efst.

4. Á síðunni **Skýrsluútlit** velur þú útlitið og velur síðan **Í lagi**.

## <a name="revert-to-the-original-default-layout"></a>Fara aftur í upprunalegt sjálfgefið útlit

Skýrslur eru hannaðar til að nota sjálfgefið útlit. Þú getur skipt aftur yfir í upprunalegt sjálfgefið útlit á síðunni **Val á útliti skýrslu**. Veldu bara skýrsluna og veldu svo aðgerðina **Endurheimta sjálfgefið val** efst á síðunni.

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
