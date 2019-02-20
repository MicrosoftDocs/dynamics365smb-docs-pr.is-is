---
title: "Stofna fyrirtækjatengiliði| Microsoft Docs"
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: is-is
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Fyrirtækjatengiliðir stofnaðir
Fyrirtækið hefur reglulega samskipti við önnur fyrirtæki sem viðskiptatengsl gætu myndast við í framtíðinni. Þegar nýr tengiliður er stofnaður þarf að skrá þessar upplýsingar svo samskipti geti haldið áfram.

Með því að úthluta eins miklum gögnum og mögulegt er um tiltekið fyrirtæki eru skilvirkt samskipti tryggð. Til dæmis tryggir úthlutun viðeigandi starfsgreinahóps að tiltekin fyrirtæki séu höfð með í öllum viðeigandi samskiptum.

Einnig er hægt að skilgreina viðskiptatengslin við tengilið. Tengiliður gæti til dæmis verið væntanlegur viðskiptamaður, banki eða verktaki.

## <a name="creatinge-contact-companies"></a>Fyrirtækjatengiliðir stofnaðir
Hægt er að stofna tengilið fyrir hvert nýtt fyrirtæki sem notandinn á í samskiptum við, til dæmis viðskiptamann, lánardrottinn, tilvonandi viðskiptamann, banka, lögfræðistofu, ráðgjafa og svo framvegis.

Tvær leiðir eru til að stofna tengilið: frá upphafi eða úr fyrirliggjandi viðskiptamanni, lánadrottni bankareikningi..

Áður en tengiliður er stofnaður er ráðlegt að athuga stillingarnar á síðunni **Tengslastjórnunargrunnur**. Nánari upplýsingar er að finna í [Uppsetning tengslastjórnunar](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Til að stofna fyrirtækjatengilið frá grunni
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Í **reitinn Nr.** er fært inn númer fyrir tengiliðinn.

    Hafi númeraröð fyrir tengiliði verið sett upp á síðunni **Tengslastjórnunargrunnur** er hægt að styðja á Færslulykilinn til að velja næsta lausa tengiliðanúmer.  
4. Setja **Tegund** á **Fyrirtæki**.
5. Hinir reitirnir eru fylltir út eins krafist er.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Stofna fyrirtækistengilið úr viðskiptamanni, lánadrottni eða bankareikning
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

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga
Ef einhverjir tengiliðir eru einnig viðskiptamenn, lánardrottnar eða bankareikningar er hægt að samstilla tengiliðaupplýsingarnar við viðvomandi viðskiptavin, lánardrottinn, eða bankareikning. Samstilling gerir upplýsingarnar sem eru sameiginleg tengiliði og viðskiptamenn, lánardrottna eða bankareikninga þær sömu.  

Áður en tengiliðir eru samstilltir við viðskiptamenn, lánardrottna eða bankareikninga þarf að tilgreina viðskiptatengslakóða fyrir viðskiptamenn, lánardrottna og bankareikninga á síðunni **uppsetning markaðssetningar**. Nánari upplýsingar er að finna í [Uppsetning tengslastjórnunar](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Mismunandi leiðir fyrir tengiliðir til að vera samstilltir við viðskiptamenn, lánardrottna og bankareikninga
Hægt er að samstilla tengiliðina við viðskiptamenn, lánardrottna eða bankareikninga á þrenna vegu:

* Tengja tengiliði við viðskiptamenn sem fyrir eru, lánardrottna, eða bankareikninga á tengiliðaspjaldinu. Frekari upplýsingar eru í [Tengja tengiliði við viðskiptamenn, lánardrottna og bankareikninga.](marketing-how-link-contact.md)
* Stofna viðskiptamenn , lánardrottna, eða bankareikninga úr tengilið. Fyrir frekar upplýsingar, sjá sjá [stofna Viðskiptamann, Lánadrottinn eða Bankareikning út frá tengilið](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Stofna tengiliði úr viðskiptamönnum, lánadrottnum eða bankareikningum. Nánari upplýsingar er að finna í [Búa til tengilið frá viðskiptavini, seljanda eða bankareikningi](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Afleiðingar samstillingar
Meðan tengiliður er samstillt viðskiptavini, lánardrottni eða bankareikningi:

* Aðeins þarf að uppfæra upplýsingar á einum stað. Ef símanúmeri, til dæmis, er breytt fyrir tengilið, er símanúmerið uppfært sjálfkrafa með sömu breytingum á viðskiptavini, lánardrottni eða bankareikningi.
* Hafi númeraröð verið tilgreind fyrir tengilið stofnar kerfið sjálfkrafa tengiliðaspjald fyrir viðskiptamenn, lánardrottna eða bankareikninga í hvert sinn sem stofnað er viðskiptamannaspjald, lánardrottna spjald eða bankareikningsspjald.
* Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.
* Hægt er að láta skrá samskipti þegar aðgerðir eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis, eru framkvæmdar.
* Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni eða bankareikningi, er tengiliður eingöngu fjarlægðu. viðskiptamann, lánardrottin eða bankareikning verður áfram eftir.
* Ef eytt er viðskiptamanni, lánardrottni eða bankareikningi sem tengist tengilið er eingöngu tengiliður eftir.

> [!NOTE]  
>   Sumar upplýsingar, s.s. um reikningsfærslur og bókunarupplýsingar, koma ekki fram á tengiliðarspjaldinu. Því gæti verið ráðlegt að bæta þeim handvirkt í viðskiptamannaspjaldið, lánardrottnaspjaldið eða bankareikningsspjaldið þegar tengiliðir eru stofnaðir sem viðskiptamenn, lánardrottnar eða bankareikningar.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Tengiliðir tengdir við viðskiptamenn, lánardrottna og bankareikninga
Hafir þú tengilið og annaðhvort viðskiptamann, lánardrottin eða bankareikning fyrir sama fyrirtækið er hægt að tengja þessa aðila saman. Það að tengja tvær einingar gerir kleift að samstilla gögnin sem eru sameiginleg þannig að sömu gögn séu á báðum stöðum.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Til að tengja tengilið við viðskiptamann, lánardrottin eða bankareikning sem þegar er til
1. Tengiliðurinn sem þú vilt tengja er opnaður.
2. Veljið aðgerðina **Tengja við fyrirliggjandi** og veljið síðan **Viðskiptamaður**, **Lánardrottinn**, eða **Banki**.
3. Veljið viðskiptamann, lánardrottin eða bankareikning sem tengja á við.

   Í **Gildandi aðalreitir** er tilgreint hvaða reitum kerfið eigi að forgangsraða ef misræmi er í reitum sem eru sameiginlegir tengiliðnum annars vegar og viðskiptamanni, lánardrottni eða bankareikningi hins vegar. Ef kóði sölumanns, til dæmis, er mismunandi milli tengiliðar og viðskiptamanns er hægt að ákveða með því að velja **Tengiliður** að nota upplýsingarnar hjá tengiliðnum.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Viðskiptamaður, lánardrottinn eða bankareikningur stofnaður úr tengilið
   Suma fyrirliggjandi tengiliði er ef til vill æskilegt að skrá sem viðskiptamenn, lánadrottna eða bankareikninga. Stofna viðskiptamanni, lánadrottni eða bankareikning úr tengilið gerir þér kleift að nota fyrirliggjandi gögn. Þegar þú stofnar viðskiptavin, lánardrottinn, eða bankareikning á þennan hátt er það samstillt við tengiliðinn. Samstilling gerir upplýsingarnar sem eru sameiginleg tengiliði og viðskiptamenn, lánardrottna eða bankareikninga þær sömu.

   Áður en þú getur skráð tengiliði á þennan hátt, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga á síðunni **Uppsetning markaðssetningar**. Ef þú munt skrá tengiliði sem bankareikning verður einnig að tilgreina númeraraðir fyrir bankareikninga á síðunni **Fjárhagsgrunnur**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Tengiliðir stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar:
   1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.
   2. Velja skal tengiliðinn sem stofna á sem viðskiptamann, lánadrottinn eða bankareikning.
   3. Veldu aðgerðina **Stofna sem** og síðan valinn annað hvort **Viðskiptamaður**, **Lánadrottinn** eða **Banki**.
   4. Staðfesta þarf eftirfarandi skilaboð.

   Tengslaupplýsingarnar eru fluttar úr spjaldinu **Tengiliður** yfir í spjaldið **Bankareikningur**, spjaldið **Viðskiptamaður**, eða spjaldið **Lánardrottinn**. Hugsanlega þarf að bæta við tilteknum upplýsingum við hvert spjald, svo sem um reikningsfærslu og greiðsluupplýsingar.

## <a name="setting-up-business-relations-on-contact-companies"></a>Uppsetning viðskiptatengsla í tengiliðafyrirtækjum
Þú getur notað Viðskiptatengsl til að tilgreina þau viðskiptatengsl sem eru við tengiliðina, til dæmis viðföng, banka, ráðgjafa eða þjónustuaðila, og svo framvegis.

Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli. Fyrst skilgreinirðu kóða viðskiptatengsla. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl. Þegar kominn er viðskiptatengslakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

> [!NOTE]  
>   Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.

### <a name="to-define-a-business-relation-code"></a>Til að skilgreina viðskiptatengslakóða
Viðskiptatengslarkóðinn skilgreinir flokk eða tegund viðskiptasambandsins, svo sem banka eða lög. Hægt er að hafa nokkrar viðskiptatengslakóða. Til að skilgreina viðskiptatengslin skal nota síðuna **Viðskiptatengsl**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðskiptatengsl** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

### <a name="AssignBusRelContact"></a> Til að úthluta viðskiptatengslum á tengilið
Þú getur ekki Úthluta viðskiptatengslum á tengilið - aðeins fyrirtæki.

1. Tengiliðurinn er opnaður.
2. Valið er **Fyrirtæki** aðgerð, og síðan **Viðskiptatengsl** aðgerð.

    Síðan **Viðskiptatengsl tengiliðar** birtist.
3. Í reitnum **Viðskiptatengslakóti** eru valin þau viðskiptatengsl sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum viðskiptatengslum og óskað er. Einnig má nota sömu aðferð til að úthluta viðskiptatengslum í Tengiliðalisti.

Fjöldi viðskiptatengsla sem tengiliðnum hefur verið úthlutað er birtur í reitnum **Fjöldi viðskiptatengsla** á hlutanum **Hlutun** á síðunni **tengiliður**.

Þegar tengiliðum hefur verið úthlutað viðskiptatengslum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="see-also"></a>Sjá einnig
[Einstaklingstengiliðir stofnaðir](marketing-create-contact-persons.md)   
[Unnið með Business Central](ui-work-product.md)

