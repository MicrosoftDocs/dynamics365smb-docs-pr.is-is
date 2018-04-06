---
title: "Tengiliðir samstilltir við viðskiptamenn og lánardrottnar| Microsoft Docs"
description: "Hægt er að tengja eða samstilla tengiliðaupplýsingar frá tengiliðum sem líka eru viðskiptamenn, lánardrottnar eða bankareikningar, þannig að þú uppfærir upplýsingarnar aðeins á einum stað."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2b85c52378a351dbc1a0809ec540b1f53c8074ef
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga
Ef einhverjir tengiliðir eru einnig viðskiptamenn, lánardrottnar eða bankareikningar er hægt að samstilla tengiliðaupplýsingarnar við viðvomandi viðskiptavin, lánardrottinn, eða bankareikning. Samstilling gerir upplýsingarnar sem eru sameiginleg tengiliði og viðskiptamenn, lánardrottna eða bankareikninga þær sömu.  

Áður en tengiliðir eru samstilltir við viðskiptamenn, lánardrottna eða bankareikninga þarf að tilgreina viðskiptatengslakóða fyrir viðskiptamenn, lánardrottna og bankareikninga í glugganum **uppsetning markaðssetningar** Nánari upplýsingar er að finna í [Uppsetning tengslastjórnunar](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Mismunandi leiðir fyrir tengiliðir til að vera samstilltir við viðskiptamenn, lánardrottna og bankareikninga
Hægt er að samstilla tengiliðina við viðskiptamenn, lánardrottna eða bankareikninga á þrenna vegu:

* Tengja tengiliði við viðskiptamenn sem fyrir eru, lánardrottna, eða bankareikninga á tengiliðaspjaldinu. Frekari upplýsingar eru í [Tengja tengiliði við viðskiptamenn, lánardrottna og bankareikninga.](marketing-how-link-contact.md)
* Stofna viðskiptamenn , lánardrottna, eða bankareikninga úr tengilið. Fyrir frekar upplýsingar, sjá sjá [stofna Viðskiptamann, Lánadrottinn eða Bankareikning út frá tengilið](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Stofna tengiliði úr viðskiptamönnum, lánadrottnum eða bankareikningum. Nánari upplýsingar er að finna í [Búa til tengilið frá viðskiptavini, seljanda eða bankareikningi](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Afleiðingar samstillingar
Meðan tengiliður er samstillt viðskiptavini, lánardrottni eða bankareikningi:

* Aðeins þarf að uppfæra upplýsingar á einum stað. Ef símanúmeri, til dæmis, er breytt fyrir tengilið, er símanúmerið uppfært sjálfkrafa með sömu breytingum á viðskiptavini, lánardrottni eða bankareikningi.
* Hafi númeraröð verið tilgreind fyrir tengilið stofnar kerfið sjálfkrafa tengiliðaspjald fyrir viðskiptamenn, lánardrottna eða bankareikninga í hvert sinn sem stofnað er viðskiptamannaspjald, lánardrottna spjald eða bankareikningsspjald.
* Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.
* Hægt er að láta skrá samskipti þegar aðgerðir eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis, eru framkvæmdar.
* Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni eða bankareikningi, er tengiliður eingöngu fjarlægðu. viðskiptamann, lánardrottin eða bankareikning verður áfram eftir.
* Ef eytt er viðskiptamanni, lánardrottni eða bankareikningi sem tengist tengilið er eingöngu tengiliður eftir.

> [!NOTE]  
>   Sumar upplýsingar, s.s. um reikningsfærslur og bókunarupplýsingar, koma ekki fram á tengiliðarspjaldinu. Því gæti verið ráðlegt að bæta þeim handvirkt í viðskiptamannaspjaldið, lánardrottnaspjaldið eða bankareikningsspjaldið þegar tengiliðir eru stofnaðir sem viðskiptamenn, lánardrottnar eða bankareikningar.

## <a name="see-also"></a>Sjá einnig
[Vinna með tengiliði](marketing-contacts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

