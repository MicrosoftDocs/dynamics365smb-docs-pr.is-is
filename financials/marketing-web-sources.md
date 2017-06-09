---
title: "Uppsetning veftengingar fyrir tengiliðafyrirtæki | Microsoft Docs"
description: "Lýsir hvernig á að nota vefur heimildir fyrir tengiliði í fjármálum"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8a452619aeeee907cf61fd5d1a8fce409ad2e42d
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-web-sources-for-contact-companies"></a>Uppsetning veftenginga fyrir tengiliðafyrirtæki
Hægt er að nota veftengingar með tengiliðafyrirtækjum til að þekkja t.d. leitarvélar og vefsvæði á netinu sem óskað er eftir að nota til að leita að upplýsingum um tengiliðina. Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

Notkun veftenginga á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina veftengingakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hverja veftengingu. Þegar kominn er veftengingakóði er hægt að byrja að úthluta kóðanum til tengiliða.

## <a name="to-define-a-web-source-code"></a>til að skilgreina vefkóðann
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Veftenglar**, og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Nýtt**.
3. Fyllt er í reitina **Kóti**, **Lýsing** og **URL**.

    Sláið inn %1 í reitinn **URL** til að setja inn staðgengil fyrir leitarorð í slóðinni. Þegar veftengingin er ræst frá tengilið er %1 skipt út fyrir leitarorð, t.d. heiti fyrirtækisins sem fært var inn í gluggann **Veftenging tengiliðar**.

Skrefin eru endurtekin til að setja upp eins margar veftengingar og óskað er.

## <a name="to-assign-web-sources-to-a-contact-company"></a>til að úthluta veftengingum á tengiliðarfyrirtæki
Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

1. Tengiliðurinn er opnaður.
2. Veljið aðgerðina **Fyrirtæki** og veljið síðan aðgerðina **Veftenging**. Glugginn **Veftenglar tengiliða** birtist.
3. Í reitnum **Veftengingarkóði** skal velja veftenginguna sem á að úthluta.
4. Í reitinn **Leitarorð** er fært inn leitarorðið sem á að nota til að finna upplýsingarnar.

Skrefin eru endurtekin til að úthluta eins mörgum veftengingum og óskað er.

Einnig má nota sömu aðferð til að úthluta veftengingum í glugganum **Tengiliðalisti**.

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

