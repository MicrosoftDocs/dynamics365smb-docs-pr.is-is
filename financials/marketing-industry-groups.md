---
title: "Uppsetning iðnaðarhópa fyrir tengiliðarfyrirtæki | Microsoft Docs"
description: "Lýsir með iðnaðarhópum með tengiliði í fjármálum"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Uppsetning iðnaðarhópa fyrir tengiliðafyrirtæki
Starfsgreinahópar eru notaðir til að tilgreina tegund starfsgreinar sem tengiliðirnir tilheyra, til dæmis smásöluaðilar eða bílgreinaiðnaðurinn.

Notkun starfsgreinahópa á tengiliði er tveggja þrepa ferli. Fyrst skilgreina starfsgreinarhópakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver starfsgreinarhóp. Þegar kominn er starfsgreinarhópakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

**Athugasemd:** Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.

## <a name="to-define-an-industry-group-code"></a>Til að skilgreina kóða starfsgreinarhóps
Kóði starfsgreinarhópsins skilgreinir tegund eða flokk hópsins, til dæmis ADVERT fyrir auglýsingar eða Press fyrir sjónvarp og útvarp. Hægt er að hafa nokkrar starfsgreinarhópakóða. Til að skilgreina starfsgreinarhópar er að nota gluggann **starfsgreinarhópar** .

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Starfsgreinahópar**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="AssignIndustryGroupContact"></a> Starfsgreinahópum úthlutað á tengilið
Þú getur ekki Úthluta Starfsgreinahópar á tengilið - aðeins fyrirtæki.

1. Tengiliðurinn er opnaður.
2. Valið er **Fyrirtæki** aðgerð, og síðan **starfsgreinarhópar** aðgerð. Glugginn **Starfsgreinahópar tengiliða** birtist.
3. Í reitnum **starfsgreinarhópakóði** veljið starfsgreinahópinn sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum starfsgreinahópum og óskað er. Einnig má nota sömu aðferð til að úthluta Starfsgreinahópar úr Tengiliðalista.

Fjöldi iðnaðarhópa sem þú hefur úthlutað tengiliðnum birtist á **Fjöldi starfsgreinahópa** reitnum í **Hlutunarviðmið** hlutanum í glugganum **Tengiliður**.

Þegar tengiliðum hefur verið úthlutað starfsgreinarhópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

