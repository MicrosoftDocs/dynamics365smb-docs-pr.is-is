---
title: Setja upp starfsgreinahópar fyrir tengiliðafyrirtæki| Microsoft Docs
description: Lýsir því hvernig skal skilgreina starfsgreinahóp og úthluta honum til tengiliðafyrirtækis, til dæmis smásöluaðilar eða bílgreinaiðnaðurinn.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 9d1f685dce54db493e830096ef5d4749f0fc221a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309029"
---
# <a name="set-up-industry-groups-for-contact-companies"></a>Setja upp Starfsgreinahópar á tengiliðafyrirtæki.
Starfsgreinahópar eru notaðir til að tilgreina tegund starfsgreinar sem tengiliðirnir tilheyra, til dæmis smásöluaðilar eða bílgreinaiðnaðurinn.

Notkun starfsgreinahópa á tengiliði er tveggja þrepa ferli. Fyrst skilgreina starfsgreinarhópakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver starfsgreinarhóp. Þegar kominn er starfsgreinarhópakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

> [!NOTE]  
>   Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.

## <a name="to-define-an-industry-group-code"></a>Til að skilgreina kóða starfsgreinarhóps
Kóði starfsgreinarhópsins skilgreinir tegund eða flokk hópsins, til dæmis ADVERT fyrir auglýsingar eða Press fyrir sjónvarp og útvarp. Hægt er að hafa nokkrar starfsgreinarhópakóða. Til að skilgreina starfsgreinarhópa skal nota síðuna **Starfsgreinarhópar**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsgreinahópar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="AssignIndustryGroupContact"></a> Starfsgreinahópum úthlutað á tengilið
Þú getur ekki Úthluta Starfsgreinahópar á tengilið - aðeins fyrirtæki.

1. Tengiliðurinn er opnaður.
2. Valið er **Fyrirtæki** aðgerð, og síðan **starfsgreinarhópar** aðgerð. Síðan **Starfsgreinahópar tengiliða** birtist.
3. Í reitnum **starfsgreinarhópakóði** veljið starfsgreinahópinn sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum starfsgreinahópum og óskað er. Einnig má nota sömu aðferð til að úthluta Starfsgreinahópar úr Tengiliðalista.

Fjöldi iðnaðarhópa sem þú hefur úthlutað tengiliðnum birtist á **Fjöldi starfsgreinahópa** reitnum í **Hlutunarviðmið** hlutanum á síðunni **Tengiliður**.

Þegar tengiliðum hefur verið úthlutað starfsgreinarhópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="see-also"></a>Sjá einnig
[Stofna tengiliði](marketing-create-contact-companies.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
