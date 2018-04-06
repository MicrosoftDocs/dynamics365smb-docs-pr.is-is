---
title: "Stofna fyrirtækjatengiliði| Microsoft Docs"
description: "Lýsir því hvernig skal stofna tengilið fyrir hvert nýtt fyrirtæki eða tilvonandi fyrirtæki sem þú átt samskipti við eða ert í sambandi við."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-contact-companies"></a>Stofna fyrirtækjatengilið
Hægt er að stofna tengilið fyrir hvert nýtt fyrirtæki sem notandinn á í samskiptum við, til dæmis viðskiptamann, lánardrottinn, tilvonandi viðskiptamann, banka, lögfræðistofu, ráðgjafa og svo framvegis.

Tvær leiðir eru til að stofna tengilið: frá upphafi eða úr fyrirliggjandi viðskiptamanni, lánadrottni bankareikningi..

Áður en tengiliður er stofnaður er ráðlegt að athuga stillingarnar í glugganum  **Tengslastjórnunargrunnur**. Nánari upplýsingar er að finna í [Uppsetning tengslastjórnunar](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Stofna nýtt tengiliðarfyrirtæki frá upphafi
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Tengiliðir** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Í **reitinn Nr.** er fært inn númer fyrir tengiliðinn.

    Hafi númeraröð fyrir tengiliði verið sett upp í glugganum **Tengslastjórnunargrunnur** er hægt að styðja á Færslulykilinn til að velja næsta lausa tengiliðanúmer.  
4. Setja **Tegund** á **Fyrirtæki**.
5. Hinir reitirnir eru fylltir út eins krafist er.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Stofna fyrirtækistengilið úr viðskiptamanni, lánadrottni eða bankareikning
Hafi þegar verið settur upp fjöldi viðskiptamanna, lánardrottna og bankareikninga er hægt að stofna tengiliði á grunni gagna sem til eru. Þegar tengilið er stofnað á þennan hátt er tengiliðaupplýsingarnar samstillt við upplýsingar um  viðskiptamann, lánadrottinn eða bankareikning.

> [!NOTE]  
>   Áður en þú getur stofnað tengiliðafyrirtæki á þennan hátt, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í glugganum **uppsetning markaðssetningar** Ef þú munt stofna tengiliði úr bankareikningi verður einnig að tilgreina númeraraðir fyrir bankareikninga í glugganum **Fjárhagsgrunnur**.

1. Veljið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, færa inn eitt af eftirtöldu, allt eftir því hvaðan stofna á tengiliði og veljið svo viðkomandi tengil.
   * **Stofna tengiliði útfrá viðskiptamönnum**
   * **Stofna tengiliði útfrá lánardottnum**
   * **Stofna tengiliði útfrá bankareikningum**
2. Á glugganum runuvinnsla sem opnast í hlutanum **Viðskiptamaður**, **Lánadrottin** eða **Bankareikningur** skal setja upp afmarkanir ef stofna á tengiliði úr ákveðnum viðskiptamönnum, lánadrottnum eða bankareikningum.
3. Veldu hnappinn **Í lagi** til að hefja stofnun tengiliða.

    Kerfið úthlutar nýju tengiliðunum næstu tengiliðanúmerunum í númeraröðinni. Viðskiptatengsl fyrir lánardrottna sem er tilgreint í **uppsetning markaðssetningar** glugganum er úthlutað á nýlega stofnuðu tengiliðina..

> [!TIP]  
>   Þú getur einnig stofnað viðskiptamann, lánadrottinn eða bankareikning út frá tengilið. Fyrir frekar upplýsingar, sjá sjá [stofna Viðskiptamann, Lánadrottinn eða Bankareikning út frá tengilið](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Sjá einnig
[Samstilla tengiliði við viðskiptavini, seljendur og bankareikninga](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Úthluta viðskiptatengslum á tengilið](marketing-business-relations.md#AssignBusRelContact)  
[Úthluta Starfsgreinahópum á tengilið](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Pósthópum úthlutað á tengiliði](marketing-mailing-groups.md#AssignMailGroupContact)  
[Stofna einstaklingstengilið](marketing-create-contact-persons.md)  
[Unnið með Finance and Operations, Business Edition](ui-work-product.md)

