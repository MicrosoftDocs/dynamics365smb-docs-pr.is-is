---
title: "Uppsetning viðskiptatengsla fyrir tengiliði | Microsoft Docs"
description: "Lýsir viðskiptatengslum fyrir tengiliði í Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6719ac45f298d6c952427c871eaf818cb7480c3
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-business-relations-on-contact-companies"></a>Uppsetning viðskiptatengsla í tengiliðafyrirtækjum
Þú getur notað Viðskiptatengsl til að tilgreina þau viðskiptatengsl sem eru við tengiliðina, til dæmis viðföng, banka, ráðgjafa eða þjónustuaðila, og svo framvegis.

Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli. Fyrst skilgreinirðu kóða viðskiptatengsla. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl. Þegar kominn er viðskiptatengslakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

**Athugasemd:** Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.

## <a name="to-define-a-business-relation-code"></a>Til að skilgreina viðskiptatengslakóða
Viðskiptatengslarkóðinn skilgreinir flokk eða tegund viðskiptasambandsins, svo sem banka eða lög. Hægt er að hafa nokkrar viðskiptatengslakóða. Til að skilgreina viðskiptatengslin er að nota gluggann **Viðskiptatengsl** .

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Viðskiptasambönd**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="AssignBusRelContact"></a> Til að úthluta viðskiptatengslum á tengilið
Þú getur ekki Úthluta viðskiptatengslum á tengilið - aðeins fyrirtæki.

1. Tengiliðurinn er opnaður.
2. Valið er **Fyrirtæki** aðgerð, og síðan **Viðskiptatengsl** aðgerð.

    Glugginn **Viðskiptatengsl tengiliðar** birtist.
3. Í reitnum **Viðskiptatengslakóti** eru valin þau viðskiptatengsl sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum viðskiptatengslum og óskað er. Einnig má nota sömu aðferð til að úthluta viðskiptatengslum í Tengiliðalisti.

Fjöldi viðskiptatengsla sem tengiliðnum hefur verið úthlutað er birtur í reitnum **Fjöldi viðskiptatengsla ** á hlutanum **Hlutun** í glugganum **tengiliður**.

Þegar tengiliðum hefur verið úthlutað viðskiptatengslum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

