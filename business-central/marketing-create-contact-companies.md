---
title: Stofna viðskiptatengiliði | Microsoft Docs
description: Lýsir verkum til að stofna tengiliði og skilgreina viðskiptatengslin.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d5885ac3310e545c0a2550ca49d67f1f9ab6ca35
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922720"
---
# <a name="create-contacts"></a>Stofna tengiliði
Þegar viðskiptatengsl eru þróuð við einhvern í öðru fyrirtæki er hægt að stofna viðkomandi sem tengilið og færa inn upplýsingar um hann eða fyrirtæki hans sem geta komið sér vel í samskiptum í framtíðinni. Á síðunni **Tengiliðaspjald** er hægt að stofna eftirfarandi gerðir tengiliða:

* **Einstaklingur** - Yfirleitt er þetta þegar haft er bein samskipti við einhvern og tengiliðaupplýsingar fengnar frá viðkomandi.
* **Fyrirtæki** - Til dæmis ef tengiliðurinn er ekki einstaklingur heldur eining, t.d. verktaki eða banki. 

Upplýsingarnar sem eiga við um hverja gerð tengiliða eru mismunandi, þannig að reitirnir og aðgerðirnar sem eru í boði eru ólíkar. Til dæmis er aðeins hægt að úthluta starfsábyrgðir á einstakling og starfsgreinarhóp á fyrirtæki. 

Hægt er að breyta gildi reitsins **Gerð** seinna eða nota reitina í flýtiflipanum **Erfðir** á síðunni **Uppsetning markaðssetningar** til að tilgreina gögnin sem á að deila milli einstaklings og fyrirtækis hans. Nánari upplýsingar er að finna í [Uppsetning tengiliða](marketing-setup-contacts.md).

Þegar tengiliði er breytt í viðskiptamann, til dæmis, verður tengiliðurinn eða tengiliðarfyrirtækið að heiti viðskiptamannsins. Færslunni fyrir tengiliðinn er haldið eftir og hægt er að tengja tengiliðinn og viðskiptamanninn þannig að gögnin verði samstillt héðan í frá.

## <a name="to-create-a-contact-manually"></a>Að búa til tengilið handvirkt
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt** .
3. Í reitnum **númer** er fært inn númer fyrir tengiliðinn.

    Ef númeraröð fyrir tengiliði hefur verið sett upp á síðunni **Uppsetning markaðssetningar** er hægt að styðja á **Enter** til að setja inn tiltækt tengiliðanúmer.  
5. Önnur svæði eru fyllt út eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning:
Ef þú ert með viðskiptavini, lánardrottna og bankareikninga sem þú vilt búa tengiliðaspjöld fyrir, geturðu notað runuvinnsluna **Stofna tengiliði úr** til að stofna tengiliði á grunni fyrirliggjandi gagna. Þegar tengiliður er stofnaður á þennan hátt eru tengiliðaupplýsingarnar samstilltar eftir á við upplýsingar um viðeigandi viðskiptamann, lánadrottin eða bankareikning. Fyrir frekar upplýsingar, sjá [Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts)

> [!NOTE]  
> Áður en þú getur stofnað tengiliði á grunni fyrirliggjandi gagna, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í flýtiflipanum **Samskipti** á síðunni **Uppsetning markaðssetningar** . Frekari upplýsingar er að finna í [Setja upp tengiliði](marketing-setup-contacts.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn eitt af eftirfarandi, fer eftir úr hverju þú vilt búa til tengiliði, og veldu síðan viðeigandi tengil.
   * **Stofna tengiliði út frá viðskiptamönnum**
   * **Stofna tengiliði út frá lánardrottnum**
   * **Stofna tengiliði út frá bankareikningum**
2. Á beiðnisíðunni sem opnast í hlutanum **Viðskiptamaður** , **Lánadrottin** eða **Bankareikningur** skal setja upp afmarkanir ef stofna á tengiliði úr ákveðnum viðskiptamönnum, lánadrottnum eða bankareikningum.
3. Veldu hnappinn **Í lagi** til að hefja stofnun tengiliða.

Kerfið úthlutar nýju tengiliðunum næstu tengiliðanúmerunum í númeraröðinni. Viðskiptatengsl sem eru tilgreind á síðunni **Uppsetning markaðssetningar** er úthlutað á nýlega stofnuðu tengiliðina.

> [!TIP]  
> Einnig er hægt að gera þetta á hinn veginn, með því að stofna viðskiptavin, lánardrottin eða bankareikning úr tengilið. Frekari upplýsingar er að finna í [Tengiliðir stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið
Ef þú ert með viðskiptamann, lánardrottin, starfsmann eða bankareikning fyrir fyrirtækið sem þú vilt stofna tengilið fyrir, er hægt að nota virknina **Stofna sem** . Þegar tengiliður er stofnaður á þennan hátt eru tengslaupplýsingar samstilltar í framhaldinu við viðeigandi viðskiptamann, lánardrottin eða bankareikningsupplýsingar. Fyrir frekar upplýsingar, sjá [Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts)

> [!NOTE]  
> Áður en þú getur stofnað viðskiptamenn, starfsmenn eða bankareikninga úr tengiliðum, þarft að tilgreina kóða viðskiptatengsla á síðunni **Uppsetning markaðssetningar** í flýtiflipanum **Samskipti** . Nánari upplýsingar er að finna í [Uppsetning tengiliða](marketing-setup-contacts.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Velja skal tengiliðinn sem stofna á sem viðskiptamann, starfsmann, lánadrottin eða bankareikning.
3. Veljið aðgerðina **Stofna sem** og veljið síðan annaðhvort **Viðskiptamaður** , **Lánardrottinn** , **Banki** eða **Starfsmaður** .
4. Velja hnappinn **Í lagi** .

Tengslaupplýsingarnar eru fluttar úr tengiliðaspjaldinu yfir í nýtt spjald viðskiptamanns, lánardrottins, starfsmanns eða bankareiknings. Hugsanlega þarf að bæta við tilteknum upplýsingum við hvert spjald, svo sem um reikningsfærslu og greiðsluupplýsingar. Nánari upplýsingar má til dæmis finna í [Skrá nýja viðskiptavini](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Til að tengja tengilið við viðskiptamann, lánardrottin, starfsmann eða bankareikning sem þegar er til
Hafir þú tengilið og annaðhvort viðskiptamann, lánardrottin, starfsmann eða bankareikning fyrir sama fyrirtækið er hægt að tengja einingarnar tvær til að samstilla gögn.

1. Tengiliðurinn sem þú vilt tengja er opnaður.
2. Veljið aðgerðina **Tengja við fyrirliggjandi** og veljið síðan aðgerðina **Viðskiptamaður** , **Lánardrottinn** , eða **Banki** eða **Starfsmaður** .
3. Á síðunni sem opnast skal velja viðskiptamann, lánardrottin, starfsmann eða bankareikning sem tengja á við.
4. Í reitnum **Gildandi aðalreitir** er tilgreint hvaða reitum eigi að forgangsraða ef misræmi er upplýsingum í reitum sem eru sameiginlegir tengiliðnum annars vegar og viðskiptamanni, lánardrottni, starfsmanni eða bankareikningi hins vegar. Til dæmis ef kóði sölumanns er annar fyrir tengiliðinn og viðskiptamanninn, er hægt að velja að halda þeim sem er í tengiliðaspjaldinu með því að velja **Tengiliður** .
5. Velja hnappinn **Í lagi** .

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Samstilla tengiliði við viðskiptamenn, lánardrottna, starfsmenn og bankareikninga
Ef einhverjir tengiliðir eru einnig viðskiptamenn, lánardrottnar eða bankareikningar er hægt að samstilla þá við gögn úr tengiliðnum með eftirfarandi ávinningi:

* Aðeins þarf að uppfæra upplýsingar á einum stað. Ef símanúmeri, til dæmis, er breytt fyrir tengilið, er símanúmerið uppfært sjálfkrafa fyrir viðskiptamann, lánardrottin, starfsmann eða bankareikning.
* Hafi númeraröð verið tilgreind fyrir tengiliði, þegar starfsmaður, lánardrottin, starfsmaður eða bankareikningur er stofnaður, er tengiliður sjálfkrafa stofnaður.
* Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.
* Hægt er að láta skrá samskipti eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis.
* Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni, starfsmanni eða bankareikningi, er tengiliður eingöngu fjarlægður. Viðskiptamaður, lánardrottinn eða bankareikningur verður áfram eftir.
* Ef viðskiptamaður, lánardrottinn, starfsmaður eða bankareikningur er tengdur við tengilið, helst tengiliðurinn áfram.

> [!NOTE]  
> Sumar upplýsingar, t.d. upplýsingar um reikningsfærslu og bókun, eru ekki í boði fyrir tengiliði. Þegar stofnaðir eru tengiliðir sem viðskiptamenn, lánardrottnar, starfsmenn eða bankareikningar, viltu hugsanlega bæta þeim við handvirkt.

Þrjár leiðir eru til að virkja samstillingu gagna á milli tengiliða og viðskiptamanna, lánardrottna, starfsmanna eða bankareikninga:

* Þegar tengiliðir eru stofnaðir úr viðskiptamönnum, lánadrottnum, starfsmönnum eða bankareikningum. Sjá [Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning:](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Þegar stofnaðir eru viðskiptamenn, lánardrottnar, starfsmenn eða bankareikningar úr tengiliðum. Sjá [Stofna viðskiptamann, lánardrottin eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Þegar þú tengir tengiliði við fyrirliggjandi viðskiptamenn, lánardrottna, starfsmenn og bankareikninga úr tengiliðaspjaldinu. Sjá [Til að tengja tengilið við viðskiptamann, lánardrottin eða bankareikning sem þegar er til](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Til að skoða hvaða viðskiptavin, lánardrottin, starfsmann eða bankareikning tengiliður er tengdur við
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Veljið línuna fyrir tengilið, veljið aðgerðina **Tengdar upplýsingar** og veljið síðan aðgerðina **Viðskiptamaður/Lánardrottinn/Bankareikningur/Starfsmaður** .

## <a name="see-also"></a>Sjá einnig
[Vinna með tengiliði](marketing-contacts.md)  
[Uppsetning tengiliða](marketing-setup-contacts.md)  
[Unnið með Business Central](ui-work-product.md)
