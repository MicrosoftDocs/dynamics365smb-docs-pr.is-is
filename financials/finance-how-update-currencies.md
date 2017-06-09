---
title: "Hvernig á að: Uppfæra gengi | Microsoft Docs"
description: "Vinna með marga gjaldmiðla"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Hvernig á að: Uppfæra gengi
Setja þarf upp kóða fyrir hvern gjaldmiðil sem notaður er ef keypt er eða selt í öðrum gjaldmiðlum en staðbundinn gjaldmiðill, ef eitthvað er útistandandi eða gjaldfallið í öðrum gjaldmiðlum, eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.  

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).

Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum upp til dags. Yahoo gjaldeyrisgengi er fyrirfram og tilbúinn til að virkja.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Setja upp þjónustu um gengi gjaldmiðils
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Þjónusta um gengi gjaldmiðils**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fylltu inn **Þjónusta um gengi gjaldmiðils** eftir því sem nauðsyn krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veldu reitinn **Virkt** til að virkja þjónustuna.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Til að uppfæra gengi í gegnum þjónustu
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Gjaldmiðlar**, og velja síðan viðeigandi tengil.
2. Veldu aðgerðina **Uppfæra gengi**.

Gildið í **Gengi** reitnum í **Gjaldmiðlar** er uppfærður með nýjustu gengi gjaldmiðilsins.

## <a name="see-also"></a>Sjá einnig
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

