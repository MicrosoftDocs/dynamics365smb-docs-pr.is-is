---
title: "Skilgreina kóða viðskiptatengsla á tengiliði| Microsoft Docs"
description: "Notaðu viðskiptatengsl í Business Central til að hjálpa til við markaðssetningu og tilgreina þau viðskiptatengsl sem þú hefur við viðföng, biðlara og viðskiptavini, t.d. banka eða þjónustuaðila."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-marketing
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 33743655f682aae9e02393aa68d04dffd334357b
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Uppsetning viðskiptatengsla í tengiliðafyrirtækjum
Þú getur notað Viðskiptatengsl til að tilgreina þau viðskiptatengsl sem eru við tengiliðina, til dæmis viðföng, banka, ráðgjafa eða þjónustuaðila, og svo framvegis.

Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli. Fyrst skilgreinirðu kóða viðskiptatengsla. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl. Þegar kominn er viðskiptatengslakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

> [!NOTE]  
>   Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.

## <a name="to-define-a-business-relation-code"></a>Til að skilgreina viðskiptatengslakóða
Viðskiptatengslarkóðinn skilgreinir flokk eða tegund viðskiptasambandsins, svo sem banka eða lög. Hægt er að hafa nokkrar viðskiptatengslakóða. Til að skilgreina viðskiptatengslin skal nota síðuna **Viðskiptatengsl**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðskiptatengsl** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="AssignBusRelContact"></a> Til að úthluta viðskiptatengslum á tengilið
Þú getur ekki Úthluta viðskiptatengslum á tengilið - aðeins fyrirtæki.

1. Tengiliðurinn er opnaður.
2. Valið er **Fyrirtæki** aðgerð, og síðan **Viðskiptatengsl** aðgerð.

    Síðan **Viðskiptatengsl tengiliðar** birtist.
3. Í reitnum **Viðskiptatengslakóti** eru valin þau viðskiptatengsl sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum viðskiptatengslum og óskað er. Einnig má nota sömu aðferð til að úthluta viðskiptatengslum í Tengiliðalisti.

Fjöldi viðskiptatengsla sem tengiliðnum hefur verið úthlutað er birtur í reitnum **Fjöldi viðskiptatengsla** á hlutanum **Hlutun** á síðunni **tengiliður**.

Þegar tengiliðum hefur verið úthlutað viðskiptatengslum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

