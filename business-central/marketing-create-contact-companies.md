---
title: Stofna viðskiptatengiliði
description: Lýsir verkunum sem þarf til að stofna tengiliði og skilgreina viðskiptatengslin í tengiliðaspjaldinu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.date: 08/30/2022
ms.author: bholtorf
---
# Stofna tengiliði

Þegar komið er á viðskiptatengslum við einhvern í öðru fyrirtæki skal bæta viðkomandi við sem tengiliði í [!INCLUDE[prod_short](includes/prod_short.md)]. Því næst skaltu bæta við upplýsingum um viðkomandi eða fyrirtæki hans sem geta reynst gagnlegar fyrir komandi samskipti. Á síðunni **Tengiliðaspjald** er hægt að stofna eftirfarandi gerðir tengiliða:

* **Einstaklingur** - Notaðu þetta þegar haft er bein samskipti við einhvern og tengiliðaupplýsingar fengnar frá viðkomandi.
* **Fyrirtæki** - Notaðu þetta fyrir tengilið sem er ekki einstaklingur heldur eining, t.d. verktaki eða banki.

Upplýsingarnar sem eiga við um hverja gerð tengiliða eru mismunandi, þannig að tiltækir reitir og aðgerðir eru ólíkar. Til dæmis er aðeins hægt að úthluta starfsábyrgðir á einstakling og starfsgreinarhóp á fyrirtæki.

Hægt er að breyta gildinu seinna í reitnum **Gerð**. Að öðrum kosti skal nota reitina í flýtiflipanum **Erfðir** á síðunni **Uppsetning markaðssetningar** til að tilgreina gögnin sem á að deila milli einstaklings og fyrirtækis hans. Frekari upplýsingar má finna á [Uppsetning tengiliða](marketing-setup-contacts.md).

Þegar tengiliði er breytt í viðskiptamann, til dæmis, verður tengiliðurinn eða tengiliðarfyrirtækið að heiti viðskiptamannsins. Færslunni fyrir tengiliðinn er haldið eftir og hægt er að tengja tengiliðinn og viðskiptamanninn þannig að gögnin verði samstillt héðan í frá.

> [!NOTE]
> Ef þú kveikir á [eiginleikauppfærslu fyrir sniðmát umreiknings](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees) geturðu líka stofnað lánardrottna eða starfsmenn úr viðskiptatengiliðum.
>
> Ef þú hins vegar ert nú þegar að nota innbyggðu virknina til að stofna viðskiptamenn eða vörur sjálfkrafa, þá styður þessi eiginleikauppfærsla ekki sérstillta reiti, og nýlega stofnaðir viðskiptamenn eða vörur munu ekki fela í sér slík gögn.

## Að búa til tengilið handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tengiliðir**, velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Í reitnum **númer** er fært inn númer fyrir tengiliðinn.

   Hafi númeraröð fyrir tengiliði verið sett upp á  **síðu Markaðsuppsetningarinnar**  er hægt að velja  <kbd>Enter</kbd>  til að setja inn næsta tiltæka númer tengiliðar.
4. Önnur svæði eru fyllt út eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning:

Ef þú ert með fyrirliggjandi viðskiptamenn, lánardrottna og bankareikninga sem þú vilt búa tengiliðaspjöld fyrir, geturðu notað runuvinnsluna **Stofna tengiliði úr**. Þegar tengiliður er stofnaður á þennan hátt eru tengiliðaupplýsingarnar samstilltar eftir á við upplýsingar um viðeigandi viðskiptamann, lánadrottin eða bankareikning. Frekari upplýsingar eru í [Samstilla tengiliði við viðskiptamenn, lánardrottna, starfsmenn og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Áður en þú getur stofnað tengiliði á grunni fyrirliggjandi gagna, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í flýtiflipanum **Samskipti** á síðunni **Uppsetning markaðssetningar**. Frekari upplýsingar má finna á [Setja upp tengiliði](marketing-setup-contacts.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn eitt af eftirfarandi sem samsvarar einingunni sem á að stofna tengiliði fyrir, síðan skaltu velja viðeigandi tengil.
   * **Stofna tengiliði útfrá viðskiptamönnum**
   * **Stofna tengiliði út frá lánardrottnum**
   * **Stofna tengiliði út frá bankareikningum**
2. Á beiðnisíðunni sem opnast í hlutanum **Viðskiptamaður**, **Lánadrottin** eða **Bankareikningur** skal setja upp afmarkanir ef stofna á tengiliði úr ákveðnum viðskiptamönnum, lánadrottnum eða bankareikningum.
3. Veldu **Í lagi** til að stofna tengiliði.

Kerfið úthlutar nýju tengiliðunum næstu tengiliðanúmerunum í númeraröðinni. Viðskiptatengslakóðinn sem er tilgreindur á síðunni **Uppsetning markaðssetningar** er úthlutað á nýlega stofnuðu tengiliðina.

> [!TIP]  
> Einnig er hægt að gera þetta á hinn veginn, með því að stofna viðskiptavin, lánardrottin, starfsmann eða bankareikning úr tengilið. Frekari upplýsingar eru í hlutanum [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið

Ef þú ert með viðskiptamann, lánardrottin, starfsmann eða bankareikning fyrir fyrirtækið sem þú vilt stofna tengilið fyrir, er hægt að nota aðgerðina **Stofna sem**. Þegar tengiliður er stofnaður á þennan hátt eru tengslaupplýsingar samstilltar í framhaldinu við viðeigandi viðskiptamann, lánardrottin eða bankareikningsupplýsingar. Frekari upplýsingar eru í [Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Áður en þú getur stofnað viðskiptamenn, starfsmenn eða bankareikninga úr tengiliðum, þarft að tilgreina kóða viðskiptatengsla á síðunni **Uppsetning markaðssetningar** í flýtiflipanum **Samskipti**. Frekari upplýsingar má finna á [Uppsetning tengiliða](marketing-setup-contacts.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tengiliðir**, velja síðan viðkomandi tengil.
2. Velja skal tengiliðinn sem stofna á sem viðskiptamann, starfsmann, lánadrottin eða bankareikning.
3. Veldu aðgerðina **Stofna sem** og veldu síðan annaðhvort **Viðskiptamaður**, **Lánardrottinn**, **Banki** eða **Starfsmaður**.
4. Velja **Í lagi**.

Tengslaupplýsingarnar eru fluttar úr tengiliðaspjaldinu yfir í nýtt spjald viðskiptamanns, lánardrottins, starfsmanns eða bankareiknings. Hugsanlega þarf að bæta við tilteknum upplýsingum við hvert spjald, svo sem um reikningsfærslu og greiðsluupplýsingar. Sjá t.d. [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).

## Til að tengja tengilið við viðskiptamann, lánardrottin, starfsmann eða bankareikning sem þegar er til

Hafir þú tengilið og annaðhvort viðskiptamann, lánardrottin, starfsmann eða bankareikning fyrir sama fyrirtækið er hægt að tengja einingarnar tvær til að samstilla gögn.

1. Opnaðu tengilinn sem þú vilt tengja.
2. Veljið aðgerðina **Tengja við fyrirliggjandi** og veljið síðan aðgerðina **Viðskiptamaður**, **Lánardrottinn**, eða **Banki** eða **Starfsmaður**.
3. Á síðunni sem opnast skal velja viðskiptamann, lánardrottin, starfsmann eða bankareikning sem tengja á við.
4. Í reitnum **Gildandi aðalreitir** skal tilgreina reitina sem á að forgangsraða ef misræmi er á upplýsingum í reitum sem eru sameiginlegir bæði fyrirliggjandi tengilið annars vegar og viðskiptamanni, lánardrottni, starfsmanni eða bankareikningi hins vegar. Þannig að ef kóði sölumanns er mismunandi á milli tengiliðar og viðskiptamanns er hægt að velja að halda þeim sem er í tengiliðaspjaldinu með því að velja **Tengiliður**.
5. Velja **Í lagi**.

## Að fjarlægja tengil milli tengiliðar og fyrirliggjandi viðskiptamanns, lánardrottins, starfsmanns eða bankareiknings

Ef þú tengdir óvart tengilið við viðskipamann, lánardrottin, starfsmann eða bankareikning skaltu fjarlægja tengilinn milli eininganna þannig að gögnin samstillist ekki lengur.

1. Opna skal tengiliðinn sem er með rangan tengil.  
2. Veljið aðgerðina **Viðskiptatengsl**.  
3. Á síðunni sem opnast skal velja viðskiptamann, lánardrottin, starfsmann eða bankareikning þar sem fjarlægja á tengilinn.  
4. Velja skal aðgerðina **Eyða**.  

> [!NOTE]  
> Ekki skal nota gluggann **Viðskiptatengsl** til að breyta tengslum sem fyrir eru. Þess í stað skal fjarlægja tengslin og nota aðgerðina **Tengja v. fyrirliggjandi**. Frekari upplýsingar er að finna í hlutanum [Að tengja tengilið við viðskiptamann, lánardrottin, starfsmann eða bankareikning sem þegar er til](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Samstilla tengiliði við viðskiptamenn, lánardrottna, starfsmenn og bankareikninga

Ef einhverjir tengiliðir eru einnig viðskiptamenn, lánardrottnar eða bankareikningar er hægt að samstilla þá við gögn úr tengiliðnum með eftirfarandi ávinningi:

* Aðeins þarf að uppfæra upplýsingar á einum stað. Þannig að ef þú breytir símanúmeri fyrir tengilið verður símanúmerið uppfært sjálfkrafa fyrir viðskiptamann, lánardrottin, starfsmann eða bankareikning.
* Hafi númeraröð verið tilgreind fyrir tengiliði, þegar starfsmaður, lánardrottin, starfsmaður eða bankareikningur er stofnaður, er tengiliður sjálfkrafa stofnaður.
* Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.
* Hægt er að láta skrá samskipti eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis.
* Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni, starfsmanni eða bankareikningi, er tengiliður eingöngu fjarlægður. Viðskiptamaður, lánardrottinn eða bankareikningur verður áfram eftir.
* Ef viðskiptamaður, lánardrottinn, starfsmaður eða bankareikningur er tengdur við tengilið, helst tengiliðurinn áfram.

> [!NOTE]  
> Sumar upplýsingar, t.d. upplýsingar um reikningsfærslu og bókun, eru ekki í boði fyrir tengiliði. Þegar stofnaðir eru tengiliðir sem viðskiptamenn, lánardrottnar, starfsmenn eða bankareikningar viltu hugsanlega bæta þeim upplýsingum við handvirkt.

Þrjár leiðir eru til að virkja samstillingu gagna á milli tengiliða og viðskiptamanna, lánardrottna, starfsmanna eða bankareikninga:

* Stofna tengiliði úr viðskiptamönnum, lánardrottnum eða bankareikningum. Frekari upplýsingar eru í hlutanum [Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Þegar stofnaðir eru viðskiptamenn, lánardrottnar, starfsmenn eða bankareikningar úr tengiliðum. Frekari upplýsingar eru í hlutanum [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Þegar þú tengir tengiliði við fyrirliggjandi viðskiptamenn, lánardrottna, starfsmenn og bankareikninga úr tengiliðaspjaldinu. Frekari upplýsingar er að finna í hlutanum [Að tengja tengilið við viðskiptamann, lánardrottin, starfsmann eða bankareikning sem þegar er til](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Til að skoða hvaða viðskiptavin, lánardrottin, starfsmann eða bankareikning tengiliður er tengdur við

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tengiliðir** og velja síðan viðkomandi tengil.
2. Veldu línuna fyrir tengilið, veldu aðgerðina **Tengdar upplýsingar** og veldu  síðan aðgerðina **Viðskiptamaður/Lánardrottinn/Bankareikningur/Starfsmaður**.

## Sjá einnig .

[Vinna með tengiliði](marketing-contacts.md)  
[Uppsetning tengiliða](marketing-setup-contacts.md)  
[Nota kortaþjónustu til að finna staðsetningar og leiðsagnir](across-online-maps.md)  
[Vinna með Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
