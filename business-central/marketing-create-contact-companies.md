---
title: Stofna fyrirtækjatengiliði| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: aaeb98aa5e3c48a92be71546be33b1494a751cb9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799516"
---
# <a name="creating-contacts"></a>Stofnun tengiliða
Fyrirtækið hefur reglulega samskipti við önnur fyrirtæki sem viðskiptatengsl gætu myndast við í framtíðinni. Þegar nýr tengiliður er stofnaður þarf að skrá þessar upplýsingar svo samskipti geti haldið áfram.

Með því að úthluta eins miklum gögnum og mögulegt er um tiltekið fyrirtæki eru skilvirkt samskipti tryggð. Til dæmis tryggir úthlutun viðeigandi starfsgreinahóps að tiltekin fyrirtæki séu höfð með í öllum viðeigandi samskiptum. Einnig er hægt að skilgreina viðskiptatengslin við tengilið. Tengiliður gæti til dæmis verið væntanlegur viðskiptamaður, banki eða verktaki.

> [!NOTE]
> Í reitnum **Gerð** á síðunni **Tengiliðaspjald** er hægt að setja upp tengilið sem einstakling eða fyrirtæki, fer venjulega eftir því hvort nafn tengiliðar er þekkt við stofnun. Virkni er sú sama fyrir báðar gerðirnar, nema fyrir nokkrar gerðir viðbótarupplýsinga sem hægt er að úthluta. Hægt er að breyta gildi reitsins seinna eða nota reitina í flýtiflipanum **Erfðir** á síðunni **Uppsetning markaðssetningar** til að stjórna því hvaða gögnum er deilt milli einstaklings og viðeigandi fyrirtækis.

Hægt er að stofna tengilið fyrir hvern nýjan einstakling eða nýtt fyrirtæki sem notandinn á í samskiptum við, til dæmis viðskiptamann, lánardrottin, tilvonandi viðskiptamann, banka, lögfræðistofu, ráðgjafa og svo framvegis.

Til eru tvær leiðir til að stofna nýjan tengilið:
 * Handvirkt.
 * Úr viðskiptavini, lánardrottni eða bankareikningi sem þegar eru til.

## <a name="to-create-a-contact-manually"></a>Að búa til tengilið handvirkt
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Í reitnum **númer** er fært inn númer fyrir tengiliðinn.

    Hafi númeraröð fyrir tengiliði verið sett upp á síðunni **Uppsetning markaðssetningar** er hægt að styðja á færslulykilinn til að færa inn næsta lausa tengiliðanúmer.  
5. Önnur svæði eru fyllt út eins og þörf krefur. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning:
Ef þú ert með viðskiptavini, lánardrottna og bankareikninga sem þú vilt búa tengiliðaspjöld fyrir, geturðu notað runuvinnsluna **Stofna tengiliði úr** til að stofna tengiliði á grunni fyrirliggjandi gagna. Þegar tengiliður er stofnaður á þennan hátt eru tengiliðaupplýsingarnar samstilltar eftir á við upplýsingar um viðeigandi viðskiptamann, lánadrottin eða bankareikning. Fyrir frekar upplýsingar, sjá [Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts)

> [!NOTE]  
> Áður en þú getur stofnað tengiliði á grunni fyrirliggjandi gagna, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í flýtiflipanum **Samskipti** á síðunni **Uppsetning markaðssetningar**. Nánari upplýsingar er að finna í [Uppsetning tengiliða](marketing-setup-contacts.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn eitt af eftirfarandi, fer eftir úr hverju þú vilt búa til tengiliði, og veldu síðan viðeigandi tengil.
   * **Stofna tengiliði út frá viðskiptamönnum**
   * **Stofna tengiliði út frá lánardrottnum**
   * **Stofna tengiliði út frá bankareikningum**
2. Á beiðnisíðunni sem opnast í hlutanum **Viðskiptamaður**, **Lánadrottin** eða **Bankareikningur** skal setja upp afmarkanir ef stofna á tengiliði úr ákveðnum viðskiptamönnum, lánadrottnum eða bankareikningum.
3. Veldu hnappinn **Í lagi** til að hefja stofnun tengiliða.

Kerfið úthlutar nýju tengiliðunum næstu tengiliðanúmerunum í númeraröðinni. Viðskiptatengsl sem eru tilgreind á síðunni **Uppsetning markaðssetningar** er úthlutað á nýlega stofnuðu tengiliðina.

> [!TIP]  
> Einnig er hægt að gera þetta á hinn veginn, með því að stofna viðskiptavin, lánardrottin eða bankareikning úr tengilið. Frekari upplýsingar er að finna í [Tengiliðir stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga
Ef einhverjir tengiliðir eru einnig viðskiptamenn, lánardrottnar eða bankareikningar er hægt að samstilla tengiliðaupplýsingarnar við viðvomandi viðskiptavin, lánardrottinn, eða bankareikning.

Eftirfarandi fríðindi eru til þegar tengiliður er samstilltur við viðskiptavin, lánardrottin eða bankareikning.

* Aðeins þarf að uppfæra upplýsingar á einum stað. Ef símanúmeri, til dæmis, er breytt fyrir tengilið, er símanúmerið uppfært sjálfkrafa með sömu breytingum á viðskiptavini, lánardrottni eða bankareikningi.
* Hafi númeraröð verið tilgreind fyrir tengilið stofnar kerfið sjálfkrafa tengiliðaspjald fyrir viðskiptamenn, lánardrottna eða bankareikninga í hvert sinn sem stofnað er viðskiptamannaspjald, lánardrottna spjald eða bankareikningsspjald.
* Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.
* Hægt er að láta skrá samskipti þegar aðgerðir eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis, eru framkvæmdar.
* Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni eða bankareikningi, er tengiliður eingöngu fjarlægður. viðskiptamann, lánardrottin eða bankareikning verður áfram eftir.
* Ef eytt er viðskiptamanni, lánardrottni eða bankareikningi sem tengist tengilið er eingöngu tengiliður eftir.

> [!NOTE]  
> Ákveðnar upplýsingar, s.s. um reikningsfærslur og bókunarupplýsingar, koma ekki fram á tengiliðarspjaldinu. Því gæti verið ráðlegt að bæta þeim handvirkt í viðskiptamannaspjaldið, lánardrottnaspjaldið eða bankareikningsspjaldið þegar tengiliðir eru stofnaðir sem viðskiptamenn, lánardrottnar eða bankareikningar.

Samstilling á algengum gögnum milli tengiliða og viðeigandi viðskiptavinum, lánardrottnum eða bankareikningum er virkjuð á þrjá vegu:

* Þegar tengiliðir eru tengdir við viðskiptamenn, lánardrottna, eða bankareikninga sem fyrir eru á tengiliðaspjaldinu. Sjá [Til að tengja tengilið við viðskiptamann, lánardrottin eða bankareikning sem þegar er til](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).
* Þegar þú stofnar viðskiptamenn , lánardrottna, eða bankareikninga úr tengilið. Sjá [Tengiliðir stofnaðir úr viðskiptamanni, lánadrottni eða bankareikning:](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Þegar tengiliðir eru stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar. Sjá [Tengiliðir stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Til að tengja tengilið við viðskiptamann, lánardrottin eða bankareikning sem þegar er til
Hafir þú tengilið og annaðhvort viðskiptamann, lánardrottin eða bankareikning fyrir sama fyrirtækið er hægt að tengja þessa aðila saman svo algeng gögn samstillast.

1. Tengiliðurinn sem þú vilt tengja er opnaður.
2. Veljið aðgerðina **Tengja við fyrirliggjandi** og veljið síðan aðgerðina **Viðskiptamaður**, **Lánardrottinn**, eða **Banki**.
3. Á síðunni sem opnast skal velja viðskiptamann, lánardrottin eða bankareikning sem tengja á við.
4. Í reitnum **Gildandi aðalreitir** er tilgreint hvaða reitum kerfið eigi að forgangsraða ef misræmi er í reitum sem eru sameiginlegir tengiliðnum annars vegar og viðskiptamanni, lánardrottni eða bankareikningi hins vegar. Ef kóði sölumanns er til dæmis öðruvísi á tengiliðarspjaldinu heldur en viðskiptavinaspjaldinu, er hægt að velja að halda þeim sem er á tengiliðarspjaldinu með því að velja **Tengiliður**.
5. Velja hnappinn **Í lagi**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Tengiliðir stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar:
Ef þú hefur valið viðskiptavin, lánardrottin eða bankareikning fyrir fyrirtækið þitt sem þú vilt stofna tengilið fyrir, geturðu notað virknina **Stofna sem**. Þegar tengiliður er stofnaður á þennan hátt eru tengiliðaupplýsingarnar samstilltar eftir á við upplýsingar um viðeigandi viðskiptamann, lánadrottin eða bankareikning. Fyrir frekar upplýsingar, sjá [Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts)

> [!NOTE]  
> Áður en þú getur stofnað viðskiptavini, lánardrottna eða bankareikninga úr tengiliðum, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna og bankareikninga í flýtiflipanum **Samskipti** á síðunni **Uppsetning markaðssetningar**. Nánari upplýsingar er að finna í [Uppsetning tengiliða](marketing-setup-contacts.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Velja skal tengiliðinn sem stofna á sem viðskiptamann, lánadrottinn eða bankareikning.
3. Veldu aðgerðina **Stofna sem** og síðan valinn annað hvort **Viðskiptamaður**, **Lánadrottinn** eða **Banki**.
4. Velja hnappinn **Í lagi**.

Tengslaupplýsingarnar eru fluttar úr tengiliðarspjaldinu yfir í nýtt spjald viðskiptavinar, lánardrottins eða bankareiknings. Hugsanlega þarf að bæta við tilteknum upplýsingum við hvert spjald, svo sem um reikningsfærslu og greiðsluupplýsingar. Nánari upplýsingar má til dæmis finna í [Skrá nýja viðskiptavini](sales-how-register-new-customers.md).

## <a name="see-also"></a>Sjá einnig
[Vinna með tengiliði](marketing-contacts.md)  
[Uppsetning tengiliða](marketing-setup-contacts.md)  
[Unnið með Business Central](ui-work-product.md)
