---
title: "Uppfæra gengi gjaldmiðils| Microsoft Docs"
description: "Til að nota mismunandi gjaldmiðla í rekstri, er hægt að setja upp kóða fyrir hvern gjaldmiðil og nota utanaðkomandi gjaldeyrisgengisþjónustu, eins og t.d. FloatRates."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 23940bd1e5fd29dc92e8285c08679135889701e9
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="update-currency-exchange-rates"></a>Uppfæra gengi
Setja þarf upp kóða fyrir hvern gjaldmiðil sem notaður er ef keypt er eða selt í öðrum gjaldmiðlum en staðbundinn gjaldmiðill, ef eitthvað er útistandandi eða gjaldfallið í öðrum gjaldmiðlum, eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.  

Þar sem fyrirtæki starfa að auknum mæli í mörgum löndum/svæðum verður æ mikilvægara fyrir þau að geta skoðað eða skráð fjárhag sinn í fleiri en einum gjaldmiðli. Forritið styður notkun margra gjaldmiðla. Í því er fjárhagurinn settur upp með staðbundna gjaldmiðlinum (SGM) og annar gjaldmiðill er stilltur sem annar gjaldmiðill, með rétt gengi stillt.  

 Sé öðrum gjaldmiðli gefin skilgreiningin Viðbótarskýrslugjaldmiðill mun [!INCLUDE[d365fin](includes/d365fin_md.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK. Þegar kerfið reiknar upphæðir fjárhagsfærslna í öðrum skýrslugjaldmiðli notar það upplýsingarnar af síðunni **Gengi gjaldmiðils** til að finna viðeigandi gengi.  

> [!WARNING]  
>  Aðgerðina Annar skýrslugjaldmiðill ætti EKKI að nota sem grunn fyrir umreikning fjárhagslegra yfirlita. Hún er ekki verkfæri til að umreikna ársreikninga erlendra dótturfyrirtækja, sem hluti af samsteypufyrirtæki. Annar skýrslugjaldmiðill gefur einungis kost á að undirbúa skýrslur í öðrum gjaldmiðli, líkt og sá gjaldmiðill væri heimagjaldmiðill fyrirtækisins.

## <a name="adjusting-exchange-rates"></a>Gengi leiðrétt  
Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu. Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn. Keyrslan Stilla gengi er notuð til að lagfæra gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna. Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Skýrslur og upphæðir birtar í öðrum skýrslugjaldmiðli  
Með því að nota annan skýrslugjaldmiðil er hægt að auðvelda skýrsluferli fyrirtækisins í eftirfarandi tilvikum:  

- Fyrirtæki í löndum/svæðum utan ESB sem hafa þó stóran hluta færslna sinna milli fyrirtækja í ESB-löndum/svæðum. Í þessu tilviki gæti fyrirtækið sem er utan ESB skipt yfir í skráningu í evrum til að gera viðskiptaskýrslur sínar nytsamlegri fyrir viðskiptafélaga sína í ESB.  

- Fyrirtæki sem vilja einnig birta skýrslur sínar í gjaldmiðli sem er notaður meira á alþjóðavísu en þeirra eigin.  

Nokkrar skýrslur í kerfishlutanum fjárhagur byggja á fjárhagsfærslum. Til að birta fjármálagögnin í skýrslunni í öðrum skýrslugjaldmiðli er einfaldlega hakað í reitinn **Sýna í viðbótar gjaldmiðli** á viðeigandi Fjárhagsskýrslusíðu.  

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Setja upp þjónustu um gengi gjaldmiðils
Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum uppfærðum, t.d. FloatRates.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónusta um gengi gjaldmiðils** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Fylltu í reitina eftir því sem nauðsyn krefur á síðunni **Þjónusta fyrir gengi gjaldmiðils**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veldu reitinn **Virkt** til að virkja þjónustuna.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Til að uppfæra gengi í gegnum þjónustu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gjaldmiðlar** og veldu síðan tengda tengilinn.
2. Veldu aðgerðina **Uppfæra gengi**.

Gildið í **Gengi** reitnum á síðunni **Gjaldmiðlar** er uppfært með nýjustu gengi gjaldmiðilsins.

## <a name="see-also"></a>Sjá einnig
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

