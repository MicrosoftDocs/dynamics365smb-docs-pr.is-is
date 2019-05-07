---
title: Setja upp veftengingar fyrir tengiliðafyrirtæki| Microsoft Docs
description: Hægt er að skilgreina internet eða veftengingar og úthluta þeim til tengiliðafyrirtækja til að auðvelda þér að ákveða hvernig þú vilt leita að upplýsingum um tengiliði þína.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: aa5998b989d8a3d37f3d7bfcdb348a2c09381168
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "934397"
---
# <a name="set-up-web-sources-for-contact-companies"></a>Setja upp veftengingar fyrir tengiliðafyrirtæki.
Hægt er að nota veftengingar með tengiliðafyrirtækjum til að þekkja t.d. leitarvélar og vefsvæði á netinu sem óskað er eftir að nota til að leita að upplýsingum um tengiliðina. Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

Notkun veftenginga á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina veftengingakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hverja veftengingu. Þegar kominn er veftengingakóði er hægt að byrja að úthluta kóðanum til tengiliða.

## <a name="to-define-a-web-source-code"></a>Skilgreina veftengingarkóða
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **veftengingar** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Nýtt**.
3. Fyllt er í reitina **Kóti**, **Lýsing** og **URL**.

    Sláið inn %1 í reitinn **URL** til að setja inn staðgengil fyrir leitarorð í slóðinni. Þegar veftengingin er ræst frá tengilið er %1 skipt út fyrir leitarorð, t.d. heiti fyrirtækisins sem fært var inn á síðuna **Veftenging tengiliðar**.

Skrefin eru endurtekin til að setja upp eins margar veftengingar og óskað er.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Úthluta veftengingum á tengiliðarfyrirtæki
Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

1. Tengiliðurinn er opnaður.
2. Veljið aðgerðina **Fyrirtæki** og veljið síðan aðgerðina **Veftenging**. Síðan **Veftenglar tengiliða** birtist.
3. Í reitnum **Veftengingarkóði** skal velja veftenginguna sem á að úthluta.
4. Í reitinn **Leitarorð** er fært inn leitarorðið sem á að nota til að finna upplýsingarnar.

Skrefin eru endurtekin til að úthluta eins mörgum veftengingum og óskað er.

Einnig má nota sömu aðferð til að úthluta veftengingum á síðunni **Tengiliðalisti**.

## <a name="see-also"></a>Sjá einnig
[Stofna tengiliði](marketing-create-contact-companies.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
