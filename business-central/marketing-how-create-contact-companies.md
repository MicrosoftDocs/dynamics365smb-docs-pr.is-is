---
title: Stofna fyrirtækjatengiliði| Microsoft Docs
description: Lýsir því hvernig skal stofna tengilið fyrir hvert nýtt fyrirtæki eða tilvonandi fyrirtæki sem þú átt samskipti við eða ert í sambandi við.
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
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: fcd964cc1cea9fb256b58f3a73b061b241d92fe4
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309245"
---
# <a name="create-contacts"></a>Stofna tengiliði
Hægt er að stofna tengilið fyrir hvert nýtt fyrirtæki sem notandinn á í samskiptum við, til dæmis viðskiptamann, lánardrottinn, tilvonandi viðskiptamann, banka, lögfræðistofu, ráðgjafa og svo framvegis.

Tvær leiðir eru til að stofna tengilið: frá upphafi eða úr fyrirliggjandi viðskiptamanni, lánadrottni bankareikningi..

## <a name="create-a-company-contact-from-scratch"></a>Stofna nýtt tengiliðarfyrirtæki frá upphafi
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Í **reitinn Nr.** er fært inn númer fyrir tengiliðinn.

    Hafi númeraröð fyrir tengiliði verið sett upp á síðunni **Tengslastjórnunargrunnur** er hægt að styðja á Færslulykilinn til að velja næsta lausa tengiliðanúmer.  
4. Setja **Tegund** á **Fyrirtæki**.
5. Hinir reitirnir eru fylltir út eins krafist er.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Stofna fyrirtækistengilið úr viðskiptamanni, lánadrottni eða bankareikning
Hafi þegar verið settur upp fjöldi viðskiptamanna, lánardrottna og bankareikninga er hægt að stofna tengiliði á grunni gagna sem til eru. Þegar tengilið er stofnað á þennan hátt er tengiliðaupplýsingarnar samstillt við upplýsingar um  viðskiptamann, lánadrottinn eða bankareikning.

> [!NOTE]  
>   Áður en þú getur stofnað tengiliðafyrirtæki á þennan hátt, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í síðunni **uppsetning markaðssetningar**. Ef þú munt stofna tengiliði úr bankareikningi verður einnig að tilgreina númeraraðir fyrir bankareikninga á síðunni **Fjárhagsgrunnur**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn eitt af eftirfarandi, eftir því hvaðan á að búa til tengiliði, og veldu síðan tengda tengilinn.
   * **Stofna tengiliði útfrá viðskiptamönnum**
   * **Stofna tengiliði út frá lánardrottnum**
   * **Stofna tengiliði út frá bankareikningum**
2. Á síðunni runuvinnsla sem opnast í hlutanum **Viðskiptamaður**, **Lánadrottin** eða **Bankareikningur** skal setja upp afmarkanir ef stofna á tengiliði úr ákveðnum viðskiptamönnum, lánadrottnum eða bankareikningum.
3. Veldu hnappinn **Í lagi** til að hefja stofnun tengiliða.

    Kerfið úthlutar nýju tengiliðunum næstu tengiliðanúmerunum í númeraröðinni. Viðskiptatengsl fyrir lánardrottna sem er tilgreint á síðunni **uppsetning markaðssetningar** er úthlutað á nýlega stofnuðu tengiliðina.

> [!TIP]  
>   Þú getur einnig stofnað viðskiptamann, lánadrottinn eða bankareikning út frá tengilið. Fyrir frekar upplýsingar, sjá sjá [stofna Viðskiptamann, Lánadrottinn eða Bankareikning út frá tengilið](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Sjá einnig
[Samstilla tengiliði við viðskiptavini, seljendur og bankareikninga](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Úthluta viðskiptatengslum á tengilið](marketing-business-relations.md#AssignBusRelContact)  
[Úthluta Starfsgreinahópum á tengilið](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Pósthópum úthlutað á tengiliði](marketing-mailing-groups.md#AssignMailGroupContact)  
[Stofna einstaklingstengilið](marketing-create-contact-persons.md)  
[Vinna með Business Central](ui-work-product.md)
