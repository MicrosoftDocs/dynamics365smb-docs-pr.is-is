---
title: "Stofna fyrirtækjatengiliði| Microsoft Docs"
description: "Lýsir því hvernig skal stofna tengilið fyrir hvert nýtt fyrirtæki eða tilvonandi fyrirtæki sem þú átt samskipti við eða ert í sambandi við."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 64bef8820ec10bb293ccda88e7384d5d9e868e1f
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="create-contact-companies"></a>Stofna fyrirtækjatengilið
Hægt er að stofna tengilið fyrir hvert nýtt fyrirtæki sem notandinn á í samskiptum við, til dæmis viðskiptamann, lánardrottinn, tilvonandi viðskiptamann, banka, lögfræðistofu, ráðgjafa og svo framvegis.

Tvær leiðir eru til að stofna tengilið: frá upphafi eða úr fyrirliggjandi viðskiptamanni, lánadrottni bankareikningi..

Áður en tengiliður er stofnaður er ráðlegt að athuga stillingarnar í glugganum  **Tengslastjórnunargrunnur**. Nánari upplýsingar er að finna í [Uppsetning tengslastjórnunar](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Stofna nýtt tengiliðarfyrirtæki frá upphafi
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Í **reitinn Nr.** er fært inn númer fyrir tengiliðinn.

    Hafi númeraröð fyrir tengiliði verið sett upp í glugganum **Tengslastjórnunargrunnur** er hægt að styðja á Færslulykilinn til að velja næsta lausa tengiliðanúmer.  
4. Setja **Tegund** á **Fyrirtæki**.
5. Hinir reitirnir eru fylltir út eins krafist er.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Stofna fyrirtækistengilið úr viðskiptamanni, lánadrottni eða bankareikning
Hafi þegar verið settur upp fjöldi viðskiptamanna, lánardrottna og bankareikninga er hægt að stofna tengiliði á grunni gagna sem til eru. Þegar tengilið er stofnað á þennan hátt er tengiliðaupplýsingarnar samstillt við upplýsingar um  viðskiptamann, lánadrottinn eða bankareikning.

> [!NOTE]  
>   Áður en þú getur stofnað tengiliðafyrirtæki á þennan hátt, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í glugganum **uppsetning markaðssetningar** Ef þú munt stofna tengiliði úr bankareikningi verður einnig að tilgreina númeraraðir fyrir bankareikninga í glugganum **Fjárhagsgrunnur**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn eitt af eftirfarandi, eftir því hvaðan á að búa til tengiliði, og veldu síðan tengda tengilinn.
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
[Vinna með Business Central](ui-work-product.md)

