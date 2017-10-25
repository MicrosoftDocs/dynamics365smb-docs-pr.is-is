---
title: "Setja upp veftengingar fyrir tengiliðafyrirtæki| Microsoft Docs"
description: "Hægt er að skilgreina internet eða veftengingar og úthluta þeim til tengiliðafyrirtækja til að auðvelda þér að ákveða hvernig þú vilt leita að upplýsingum um tengiliði þína."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b81deefcdf79a93cc988d216f80b08794efb8ab6
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a>Hvernig skal: Setja upp veftengingar fyrir tengiliðafyrirtæki.
Hægt er að nota veftengingar með tengiliðafyrirtækjum til að þekkja t.d. leitarvélar og vefsvæði á netinu sem óskað er eftir að nota til að leita að upplýsingum um tengiliðina. Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

Notkun veftenginga á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina veftengingakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hverja veftengingu. Þegar kominn er veftengingakóði er hægt að byrja að úthluta kóðanum til tengiliða.

## <a name="to-define-a-web-source-code"></a>Skilgreina veftengingarkóða
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **veftengingar** og velja svo viðeigandi tengil.
2. Veljið aðgerðina **Nýtt**.
3. Fyllt er í reitina **Kóti**, **Lýsing** og **URL**.

    Sláið inn %1 í reitinn **URL** til að setja inn staðgengil fyrir leitarorð í slóðinni. Þegar veftengingin er ræst frá tengilið er %1 skipt út fyrir leitarorð, t.d. heiti fyrirtækisins sem fært var inn í gluggann **Veftenging tengiliðar**.

Skrefin eru endurtekin til að setja upp eins margar veftengingar og óskað er.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Úthluta veftengingum á tengiliðarfyrirtæki
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

