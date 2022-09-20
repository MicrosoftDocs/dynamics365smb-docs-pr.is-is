---
title: Stofna viðskiptatengiliði
description: Lýsir þeim verkefnum sem þarf til að stofna tengiliði og skilgreina viðskiptatengslum á tengiliðaspjaldinu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 08/30/2022
ms.author: edupont
ms.openlocfilehash: deeec3e41ab172c62607b03bd3486edbde83b3e6
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460632"
---
# <a name="create-contacts"></a>Stofna tengiliði

Þegar þú myndast viðskiptasambönd við einhvern í öðru fyrirtæki, Bættu þeim við sem tengiliður í [!INCLUDE[prod_short](includes/prod_short.md)]. Bættu síðan við upplýsingum um þá, eða fyrirtæki þeirra, sem gætu hentað í framtíðinni fjarskipti. Hægt er að stofna eftirfarandi gerðir tengiliða á **síðunni tengiliðaspjald**:

* **Manneskja** – Notaðu þetta þegar þú hefur haft bein samskipti við einhvern og haft samband þeirra við upplýsingar.
* **Fyrirtæki** – Notið þetta fyrir tengilið sem ekki er einstakur heldur fremur eining á borð við verktaka eða banka.

Upplýsingarnar sem skipta máli fyrir hverja tegund tengiliðar eru mismunandi, þannig að tiltæk svæði og aðgerðir eru ólík. Til dæmis er aðeins hægt að úthluta starfsábyrgðir á einstakling og starfsgreinarhóp á fyrirtæki.

Hægt er að breyta gildinu seinna í reitnum **Gerð**. Að öðrum kosti skal nota reitina í flýtiflipanum **Erfðir** á síðunni **Uppsetning markaðssetningar** til að tilgreina gögnin sem á að deila milli einstaklings og fyrirtækis hans. Frekari upplýsingar um [uppsetningu tengiliða](marketing-setup-contacts.md).

Þegar tengiliði er breytt í viðskiptamann, til dæmis, verður tengiliðurinn eða tengiliðarfyrirtækið að heiti viðskiptamannsins. Færslunni fyrir tengiliðinn er haldið við og hægt er að tengja tengiliðinn við viðskiptavininn svo að gögnum þeirra sé samstillt áfram.

> [!NOTE]
> Ef skipt er á [eiginleikann fyrir umbreytingarsniðmát](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees), þá er einnig hægt að stofna lánardrottna eða starfsmenn úr viðskiptatengingum.
>
> Ef hins vegar þegar verið er að nota innbyggða virkni til að stofna viðskiptavini eða vörur sjálfkrafa, styður þessi uppfærsluaðgerð ekki sérsniðin svæði og nýlega stofnaða viðskiptamenn eða vörur innihalda slík gögn ekki.

## <a name="to-create-a-contact-manually"></a>Að búa til tengilið handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **tengiliði** og veljið síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.
3. Í reitnum **númer** er fært inn númer fyrir tengiliðinn.

   Ef númeraröð fyrir tengiliði hefur verið sett upp á síðunni **Uppsetning markaðssetningar** er hægt að styðja á **Enter** til að setja inn tiltækt tengiliðanúmer.
4. Önnur svæði eru fyllt út eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning:

Ef stofnaðir hafa verið viðskiptamenn, Lánardrottnar og Bankareikningar sem stofna á tengiliðaspjöld fyrir er hægt að nota **keyrsluna stofna tengiliði úr** keyrslum. Þegar tengiliður er stofnaður með þessum hætti er tengiliðaupplýsingarnar síðar samstilltar við tengda viðskiptamann, lánardrottinn eða upplýsingar um bankareikning. [Frekari upplýsingar eru samstilltar við tengiliði við viðskiptamenn, lánardrottna, starfsmenn og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Áður en þú getur stofnað tengiliði á grunni fyrirliggjandi gagna, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í flýtiflipanum **Samskipti** á síðunni **Uppsetning markaðssetningar**. Frekari upplýsingar um [uppsetningu tengiliða](marketing-setup-contacts.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn eitt af eftirfarandi sem samsvarar einingunni sem á að stofna tengiliði úr og velja síðan tengda tengilinn.
   * **Stofna tengiliði útfrá viðskiptamönnum**
   * **Stofna tengiliði út frá lánardrottnum**
   * **Stofna tengiliði út frá bankareikningum**
2. Á beiðnisíðunni sem opnast í hlutanum **Viðskiptamaður**, **Lánadrottin** eða **Bankareikningur** skal setja upp afmarkanir ef stofna á tengiliði úr ákveðnum viðskiptamönnum, lánadrottnum eða bankareikningum.
3. Valið **er í lagi** til að byrja að stofna tengiliði.

Kerfið úthlutar nýju tengiliðunum næstu tengiliðanúmerunum í númeraröðinni. Viðskiptatengslakótanum sem tilgreindur er á **síðu Markaðsuppsetningarinnar** er úthlutað til nýstofnaðs tengiliða.

> [!TIP]  
> Einnig er hægt að gera þetta öðrum veginn í kring, þ.e. með því að stofna viðskiptavin, lánardrottinn, starfsmann eða bankareikning frá tengilið. Frekari upplýsingar eru [í til að stofna viðskiptavin, lánardrottinn, starfsmann eða bankareikning í Tengiliðahluta](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið

Ef um er að ræða viðskiptavin, lánardrottinn, starfsmann eða bankareikning fyrir fyrirtækið sem stofna á tengilið fyrir skal nota **aðgerðina stofna sem** aðgerð. Þegar tengiliður er stofnaður með þessum hætti er tengiliðaupplýsingarnar síðar samstilltar við tengda viðskiptamenn, lánardrottinn, starfsmann eða bankareikninginn upplýsingar. [Frekari upplýsingar eru samstilltar við tengiliði við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Áður en þú getur stofnað viðskiptamenn, starfsmenn eða bankareikninga úr tengiliðum, þarft að tilgreina kóða viðskiptatengsla á síðunni **Uppsetning markaðssetningar** í flýtiflipanum **Samskipti**. Frekari upplýsingar um [uppsetningu tengiliða](marketing-setup-contacts.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **tengiliði** og veljið síðan tengda tengilinn.
2. Velja skal tengiliðinn sem stofna á sem viðskiptamann, starfsmann, lánadrottin eða bankareikning.
3. **Veljið aðgerðina Create**, veljið síðan annað hvort **Viðskiptamaður**, **Lánardrottinn**, **Banki** eða **Starfsmaður**.
4. Velja **Í lagi**.

Tengslaupplýsingarnar eru fluttar úr tengiliðaspjaldinu yfir í nýtt spjald viðskiptamanns, lánardrottins, starfsmanns eða bankareiknings. Hugsanlega þarf að bæta við tilteknum upplýsingum við hvert spjald, svo sem um reikningsfærslu og greiðsluupplýsingar. Sem dæmi má sjá [skrá yfir nýja viðskiptamenn](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Til að tengja tengilið við viðskiptamann, lánardrottin, starfsmann eða bankareikning sem þegar er til

Hafir þú tengilið og annaðhvort viðskiptamann, lánardrottin, starfsmann eða bankareikning fyrir sama fyrirtækið er hægt að tengja einingarnar tvær til að samstilla gögn.

1. Tengiliðurinn sem tengja á við er opnaður.
2. Velja skal **tengilinn með fyrirliggjandi** aðgerð, velja **síðan viðskiptavin**, **Lánardrottinn**, **bankann** eða **aðgerð starfsmanns**.
3. Á síðunni sem opnast skal velja viðskiptamann, lánardrottin, starfsmann eða bankareikning sem tengja á við.
4. **Í reitnum Gildandi aðalreitir** eru reitirnir tilgreindir til að forgangsraða ef misræmi er í svæðum sem eru sameiginleg bæði tengiliðarins og viðskiptamannsins, lánardrottinsins, starfsmannsins eða bankareikninginn. Ef kóti sölumanns er mismunandi milli tengiliðar og viðskiptamanns er hægt að velja að halda einu á tengiliðaspjaldinu með því að velja **Tengiliður**.
5. Velja **Í lagi**.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Að fjarlægja tengil milli tengiliðar og fyrirliggjandi viðskiptamanns, lánardrottins, starfsmanns eða bankareiknings

Ef tengiliður viðskiptamanns, lánardrottinn, starfsmaður eða Bankareikningur sem ekki var ætlunin að fjarlægja var hlekkurinn fjarlægður milli eininga svo gögnin verði ekki lengur samstillir.

1. Opna skal tengiliðinn sem er með rangan tengil.  
2. Veljið aðgerðina **Viðskiptatengsl**.  
3. Á síðunni sem opnast skal velja viðskiptamann, lánardrottin, starfsmann eða bankareikning þar sem fjarlægja á tengilinn.  
4. Velja skal aðgerðina **Eyða**.  

> [!NOTE]  
> Ekki skal nota gluggann **Viðskiptatengsl** til að breyta tengslum sem fyrir eru. Þess í stað skal fjarlægja tengslin og nota aðgerðina **Tengja v. fyrirliggjandi**. Frekari upplýsingar er [að fá í til að tengja tengilið við kaflann Viðskiptamaður, lánardrottinn, starfsmaður eða bankareiknings](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Samstilla tengiliði við viðskiptamenn, lánardrottna, starfsmenn og bankareikninga

Ef einhverjir tengiliðanna eru einnig viðskiptamenn, Lánardrottnar, starfsmenn eða Bankareikningar er hægt að samstilla þá við gögn úr tengiliðunum og fá eftirfarandi fríðindi:

* Aðeins þarf að uppfæra upplýsingar á einum stað. Ef símanúmeri tengiliðar er breytt í tengiliðinn er númer viðskiptamanns, lánardrottins, starfsmanns eða bankareiknings uppfært sjálfkrafa.
* Hafi númeraröð verið tilgreind fyrir tengiliði, þegar starfsmaður, lánardrottin, starfsmaður eða bankareikningur er stofnaður, er tengiliður sjálfkrafa stofnaður.
* Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.
* Hægt er að láta skrá samskipti eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis.
* Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni, starfsmanni eða bankareikningi, er tengiliður eingöngu fjarlægður. Viðskiptamaður, lánardrottinn eða bankareikningur verður áfram eftir.
* Ef eytt er viðskiptamanni, lánardrottni, starfsmanni eða bankareikningi sem tengiliður er tengdur við er tengiliðurinn enn.

> [!NOTE]  
> Sumar upplýsingar, t.d. upplýsingar um reikningsfærslu og bókun, eru ekki í boði fyrir tengiliði. Þegar tengiliðir eru stofnaðir sem viðskiptamenn, Lánardrottnar, starfsmenn eða Bankareikningar, gæti verið æskilegt að bæta þeim upplýsingum við handvirkt.

Þrjár leiðir eru til að virkja samstillingu gagna á milli tengiliða og viðskiptamanna, lánardrottna, starfsmanna eða bankareikninga:

* Stofna tengiliði úr viðskiptamönnum, lánardrottnum eða bankareikningum. Frekari upplýsingar eru [í til að stofna tengilið úr hlutanum Viðskiptamaður, lánardrottinn eða bankareiknings](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Þegar stofnaðir eru viðskiptamenn, lánardrottnar, starfsmenn eða bankareikningar úr tengiliðum. Frekari upplýsingar eru [í til að stofna viðskiptavin, lánardrottinn, starfsmann eða bankareikning í Tengiliðahluta](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Þegar tengiliðir eru tengd við viðskiptamenn sem fyrir eru, lánardrottna, starfsmenn eða bankareikninga á tengiliðaspjaldinu. Frekari upplýsingar er [að fá í til að tengja tengilið við kaflann Viðskiptamaður, lánardrottinn, starfsmaður eða bankareiknings](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Til að skoða hvaða viðskiptavin, lánardrottin, starfsmann eða bankareikning tengiliður er tengdur við

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tengiliðir** og velja síðan viðkomandi tengil.
2. Velja línuna fyrir tengilið, velja **tengdar aðgerðir upplýsingar** og velja **síðan aðgerð viðskiptavinar/lánardrottins/bankareiknings/starfsmanns**.

## <a name="see-also"></a>Sjá einnig .

[Vinna með tengiliði](marketing-contacts.md)  
[Uppsetning tengiliða](marketing-setup-contacts.md)  
[Notaðu online kort til að finna staðsetningar og áttir](across-online-maps.md)  
[Vinna með Viðskiptaseðla-](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
