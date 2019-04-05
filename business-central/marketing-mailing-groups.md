---
title: Setja upp pósthópa fyrir tengiliði| Microsoft Docs
description: Pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar, t.d. fyrir markaðsherferð eða kynningu.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6c089b772c139d0c0e9465f383ab39bd3c125dca
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799861"
---
# <a name="set-up-mailing-groups-for-contacts"></a>Setja upp pósthópaa fyrir tengiliði.
pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar. Til dæmi er hægt að setja upp pósthóp með þeim tengiliðum sem eiga að fá tilkynningu um að skrifstofan hafi flutt, eða annan hóp til að senda gjafir á hátíðum.

Notkun pósthópar á tengiliði er tveggja þrepa ferli. Fyrst skilgreina pósthópskóða. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver pósthóp. Þegar kominn er pósthópskóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

## <a name="to-define-mailing-group-codes"></a>Skilgreina pósthópskóða
Pósthópskóði skilgreinir tegund eða flokk hóps, eins og Move fyrir flutning skrifstofu, GIFT fyrir hátíðsgjöf. Hægt er að hafa nokkrar starfsgreinarhópakóða. Til að skilgreina starfsgreinarhópa skal nota síðuna **Pósthópar**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Pósthópar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="AssignMailGroupContact"></a> Pósthópum úthlutað á tengiliði
1. Tengiliðurinn er opnaður.
2. Valið er **Pósthópar** aðgerð. Síðan **Pósthópar tengiliða** birtist.
3. Í reitnum **Pósthópskóði** veljið pósthópinn sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum pósthópum og óskað er. Einnig má nota sömu aðferð til að úthluta pósthópum úr Tengiliðalisti.

Fjöldi pósthópa sem þú hefur úthlutað tengiliðnum birtist í **Fjöldi pósthópa** í hlutanum **hlutaaðgerðin** á síðunni **Tengliður**.

Eftir að tengiliðum hefur verið úthlutað pósthópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="see-also"></a>Sjá einnig
[Stofna tengiliði](marketing-create-contact-companies.md)  
[Unnið með Business Central](ui-work-product.md)
