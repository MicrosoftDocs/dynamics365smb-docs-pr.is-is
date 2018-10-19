---
title: "Setja upp pósthópa fyrir tengiliði| Microsoft Docs"
description: "Pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar, t.d. fyrir markaðsherferð eða kynningu."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a7b9c39b1f213bf2b09ee24e3e6172df027e042c
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Setja upp pósthópaa fyrir tengiliði.
pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar. Til dæmi er hægt að setja upp pósthóp með þeim tengiliðum sem eiga að fá tilkynningu um að skrifstofan hafi flutt, eða annan hóp til að senda gjafir á hátíðum.

Notkun pósthópar á tengiliði er tveggja þrepa ferli. Fyrst skilgreina pósthópskóða. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver pósthóp. Þegar kominn er pósthópskóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

## <a name="to-define-mailing-group-codes"></a>Skilgreina pósthópskóða
Pósthópskóði skilgreinir tegund eða flokk hóps, eins og Move fyrir flutning skrifstofu, GIFT fyrir hátíðsgjöf. Hægt er að hafa nokkrar starfsgreinarhópakóða. Til að skilgreina starfsgreinarhópar er að nota gluggann **pósthópar** .

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Pósthópar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="AssignMailGroupContact"></a> Pósthópum úthlutað á tengiliði
1. Tengiliðurinn er opnaður.
2. Valið er **Pósthópar** aðgerð. Glugginn **Pósthópar tengiliða** birtist.
3. Í reitnum **Pósthópskóði** veljið pósthópinn sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum pósthópum og óskað er. Einnig má nota sömu aðferð til að úthluta pósthópum úr Tengiliðalisti.

Fjöldi pósthópa sem þú hefur úthlutað tengiliðnum birtist í **Fjöldi pósthópa** í hlutanum **hlutaaðgerðin** á glugganum **Tengliður**.

Eftir að tengiliðum hefur verið úthlutað pósthópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Einstaklingstengiliðir stofnaðir](marketing-create-contact-persons.md)  
[Unnið með Business Central](ui-work-product.md)

