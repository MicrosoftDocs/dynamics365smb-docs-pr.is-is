---
title: Breyta því hvernig skýrsla lítur út með því að velja annað útlit
description: 'Þú getur notað mismunandi útlit fyrir skýrslu, og skipt á milli útlits til að breyta því hvernig skýrsla lítur út.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
---
# <a name="legacy-set-the-layout-used-by-a-report"></a><a name="legacy-set-the-layout-used-by-a-report"></a>(Eldra) Velja útlit sem skýrslan notar

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Skýrsla getur verið sett upp með fleiri en eitt skýrsluútliti, sem þú getur svo skipt milli eins og þörf er á.

Með hliðsjón af útlitinu sem er í boði fyrir skýrslu er hægt að velja að nota innbyggt RDLC-skýrsluútlit, innbyggt Word-skýrsluútlit eða sérsniðið útlit. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).

Þegar sérsniðið skýrsluútlit er skilgreint er hægt að velja það af úr spjöldum viðskiptamanna og lánardrottna til að tilgreina að valið útlit á að nota fyrir skjöl sem þú býrð til fyrir viðskiptamanninn eða lánardrottinn. Frekari upplýsingar eru í [Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Skýrslur skjala (ekki lista) sem nota Word-skýrsluútlit eru venjulega hraðari en þær sem nota RDLC-skýrsluútlit. Ef þú hefur þess vegna kost á því að velja milli Word- eða RDLC-skýrsluútlits fyrir skýrslu skjals, skaltu nota Word-skýrsluútlit fyrir bestu afköstin.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a><a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Til að breyta því hvaða skýrsluútlit á að nota fyrir skýrslu eða skjal

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Val á skýrsluútliti** og velja síðan viðkomandi tengil.
  
   Síðan **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum **Fyrirtæki** efst á síðunni. **Lýsing á útliti** <!-- **Selected Layout** -->reiturinn tilgreinir útlitið sem er notað í skýrslunni.
2. Settu reitinn **Fyrirtæki** efst á fyrirtækið sem skýrslan tilheyrir.

   Þessi reitur gerir þér kleift að velja mismunandi útlit fyrir sömu skýrslu í mismunandi fyrirtækjum.

3. Til að breyta útliti sem er notað í skýrslu skal velja röðina fyrir skýrsluna og stilla svo **Valið útlit** reitinn á einn af eftirfarandi valkostum:
   * **RDLC (innbyggt)**, notar innbyggt RDLC skýrsluútlit í skýrslunni.
   * **Word (innbyggt)**, notar innbyggt Word skýrsluútlit í skýrslunni.
   * **Sérsniðið**, notar sérsniðið útlit í skýrslu.  

> [!NOTE]
> Ef þú velur skýrsluútlit af gerðinni **RDLC (innbyggt)** eða **Word (innbyggt)** og færð villuboð um að skýrslan vilji ekki útlit af sérstakri gerð, verðurðu að velja annað útlit eða búa til sérsniðin skýrsla af þeirri gerð sem þú vilt nota. Sjá næsta ferli..

Ef þú velur innbyggt RDLC skýrsluútlit, þá þarf ekkert að gera og útlitið er notað næst þegar skýrslan er keyrð.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a><a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Til að breyta sérsniðnu útliti fyrir útlit skýrslu

Einnig gæti þurft að breyta sérsniðnu útliti í notkun. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

Öll sérsniðin skýrsluútlit sem eru til fyrir skýrsluútlit í fyrirtæki eru talin upp á síðunni **Sérsniðin skýrsluútlit** . Á síðunni **Val á útliti skýrslu** er hægt að sjá hvaða sérsniðnu útlit eru í boði fyrir hverja skýrslu í gátreitnum **Sérstillt útlit** .

1. Á síðunni **Val á útliti skýrslu**, í línunni fyrir útlit skýrslunnar sem þú vilt breyta skaltu velja uppflettihnappinn í reitnum **Lýsing á sérstilltu útliti** .
2. Á síðunni **Sérsniðin skýrsluútlit** skal velja línuna yfir sérsniðna útlitið sem á að nota og veljið svo hnappinn **Í lagi**.

Heiti á völdu sérsniðnu útliti er nú sýnt í reitnum **Sérstillt útlit** og verður notað næst þegar skýrslan eða skjalið er forskoðað, prentað eða sent.

Nú er hægt að fara á spjöld viðskiptamanna og lánardrottna til að tilgreina hvaða útlit á að nota fyrir önnur skjöl sem eru búin til fyrir viðkomandi viðskiptamann eða lánardrottinn, eins og staðfestingu á pöntun eða greiðsluáminningar. Frekari upplýsingar eru í [Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
