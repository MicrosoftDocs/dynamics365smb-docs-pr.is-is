---
title: "Uppfæra gengi gjaldmiðils| Microsoft Docs"
description: "Til að nota mismunandi gjaldmiðla í rekstri, er hægt að setja upp kóða fyrir hvern gjaldmiðil og nota utanaðkomandi gjaldeyrisgengisþjónustu, eins og t.d. Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 07/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eecb1c7b7bcb62e8dc7def488f66338855dad030
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-update-currency-exchange-rates"></a>Hvernig á að: Uppfæra gengi
Setja þarf upp kóða fyrir hvern gjaldmiðil sem notaður er ef keypt er eða selt í öðrum gjaldmiðlum en staðbundinn gjaldmiðill, ef eitthvað er útistandandi eða gjaldfallið í öðrum gjaldmiðlum, eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.  

Þar sem fyrirtæki starfa að auknum mæli í mörgum löndum/svæðum verður æ mikilvægara fyrir þau að geta skoðað eða skráð fjárhag sinn í fleiri en einum gjaldmiðli. Forritið styður notkun margra gjaldmiðla. Í því er fjárhagurinn settur upp með staðbundna gjaldmiðlinum (SGM) og annar gjaldmiðill er stilltur sem annar gjaldmiðill, með rétt gengi stillt.  

 Sé öðrum gjaldmiðli gefin skilgreiningin Viðbótarskýrslugjaldmiðill mun [!INCLUDE[d365fin](includes/d365fin_md.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK. Þegar kerfið reiknar upphæðir fjárhagsfærslna í öðrum skýrslugjaldmiðli notar það upplýsingarnar úr glugganum  **Gengi gjaldmiðils** til að finna viðeigandi gengi.  

> [!WARNING]  
>  Aðgerðina Annar skýrslugjaldmiðill ætti EKKI að nota sem grunn fyrir umreikning fjárhagslegra yfirlita. Hún er ekki verkfæri til að umreikna ársreikninga erlendra dótturfyrirtækja, sem hluti af samsteypufyrirtæki. Annar skýrslugjaldmiðill gefur einungis kost á að undirbúa skýrslur í öðrum gjaldmiðli, líkt og sá gjaldmiðill væri heimagjaldmiðill fyrirtækisins.

## <a name="adjusting-exchange-rates"></a>Gengi leiðrétt  
Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu. Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn. Keyrslan Stilla gengi er notuð til að lagfæra gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna. Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Skýrslur og upphæðir birtar í öðrum skýrslugjaldmiðli  
Með því að nota annan skýrslugjaldmiðil er hægt að auðvelda skýrsluferli fyrirtækisins í eftirfarandi tilvikum:  

- Fyrirtæki í löndum/svæðum utan ESB sem hafa þó stóran hluta færslna sinna milli fyrirtækja í ESB-löndum/svæðum. Í þessu tilviki gæti fyrirtækið sem er utan ESB skipt yfir í skráningu í evrum til að gera viðskiptaskýrslur sínar nytsamlegri fyrir viðskiptafélaga sína í ESB.  

- Fyrirtæki sem vilja einnig birta skýrslur sínar í gjaldmiðli sem er notaður meira á alþjóðavísu en þeirra eigin.  

Nokkrar skýrslur í kerfishlutanum fjárhagur byggja á fjárhagsfærslum. Til að birta fjármálagögnin í skýrslunni í öðrum skýrslugjaldmiðli er einfaldlega hakað í reitinn **Sýna í viðbótar gjaldmiðli** á viðeigandi Fjárhagsskýrsluglugga.  

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Setja upp þjónustu um gengi gjaldmiðils
Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum upp til dags. Yahoo gjaldeyrisgengi er fyrirfram og tilbúinn til að virkja.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónusta um gengi gjaldmiðla** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fylltu inn **Þjónusta um gengi gjaldmiðils** eftir því sem nauðsyn krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veldu reitinn **Virkt** til að virkja þjónustuna.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Til að uppfæra gengi í gegnum þjónustu
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gjaldmiðlar** og velja svo viðeigandi tengil.
2. Veldu aðgerðina **Uppfæra gengi**.

Gildið í **Gengi** reitnum í **Gjaldmiðlar** er uppfærður með nýjustu gengi gjaldmiðilsins.

## <a name="see-also"></a>Sjá einnig
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

