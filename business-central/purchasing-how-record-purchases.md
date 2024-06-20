---
title: Skrá innkaup með innkaupareikningum
description: 'Lýsir því hvernig á að kaupa birgðir, vörur sem ekki eru birgðir eða forða með því að stofna og bóka innkaupareikninga eða pantanir.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Skrá innkaup með innkaupareikningum og pöntunum

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Innkaupareikningar og innkaupapantanir eru líka notuð til að uppfæra birgðastig gagnvirkt, sem þýðir að hægt er að lágmarka birgðakostnað og bjóða upp á betri þjónustu við viðskiptamenn. Innkaupakostnaður, þ.m.t. þjónustukostnaður og birgðavirði sem eru afleiðingar bókana innkaupareikninga eða pantana, stuðla að framlegðartölum og fjárhagslegri afkastavísum (afkastavísar) í mitt hlutverk.

## Skrá innkaup með innkaupareikningum

Þegar vörum í birgðum eða keyptri þjónustu er lokið skal bóka innkaupareikninginn til að uppfæra birgðir og fjárhagslegar færslur og virkja greiðslu til lánardrottins samkvæmt greiðsluskilmálunum. [Afgreiðsla](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

### Stofna og bóka innkaupareikning

Eftirfarandi skref útskýra hvernig á að stofna innkaupareikning. Skrefin til að stofna innkaupapöntun eru svipuð. Meginmunurinn er sá að innkaupapantanir hafa nokkra aukareiti og aðgerðir til efnislegrar meðhöndlunar á vörum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar**, velja síðan viðkomandi tengil.  
2. Í reitnum **Nafn lánardrottins** er fært inn nafn núverandi lánardrottins.

    Aðrir reitir á síðunni **Innkaupareikningur** eru nú fylltir út með stöðluðum upplýsingum fyrir valdan lánardrottin. Ef lánardrottinn er ekki skráður skal fylgja eftirfarandi skrefum:

    1. Í reitinn **Heiti** lánardrottins er fært inn heiti nýja lánardrottinsins.
    2. Í svarglugganum um að skrá nýjan lánardrottin skal velja **Já**.
    3. Frekari upplýsingar um hvernig á að fylla út lánardrottnaspjald er að finna í [Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).  
    4. Þegar lokið er við lánardrottnaspjaldið skal velja **Í lagi** til að fara aftur á síðuna **Innkaupareikningur** .

3. Fylltu í eftirstandandi reiti á síðunni **innkaupareikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Nú er hægt að fylla út innkaupareikningslínurnar með vörum eða forða sem keyptur er af lánardrottninum.

    > [!NOTE]  
    > Ef endurteknar innkaupalínur hafa verið settar upp fyrir lánardrottinn, svo sem mánaðarlegar áfyllingarpantanir, er hægt að færa línurnar inn í reikninginn með því að velja aðgerðina **Ítrekaðar innkaupalínur**.
4. Í flýtiflipanum **Línur** í reitnum **Vörunúmer** er sleginn inn fjöldi birgðavöru eða þjónustu.
5. Í reitinn **Magn** er fært fjöldi vara sem á að kaupa.

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **beint innkaupsverð** margfaldað með gildinu í reitnum **magn**.

    Verð- og línuupphæðin er sýnd með eða án söluskatts eftir því hvað er valið í reitnum **Verð með VSK** á lánardrottnaspjaldinu.

    Samtölureitirnir undir línunum eru uppfærðir sjálfkrafa þegar línur eru stofnaðar eða þeim breytt til að sýna upphæðirnar sem bókaðar eru í fjárhaginn.

6. Í reitinn **Reikningsafsl.upphæð** er færð upphæð sem á að draga frá gildinu sem sýnt er í reitnum **Heildarupphæð með VSK** neðst á reikningnum.

    > [!NOTE]  
    > Ef reikningsafslættir hafa verið settir upp fyrir lánardrottin, þá er tilgreint prósentugildi sjálfkrafa sett inn í reitinn **Reikningsafsláttur lánardrottins %** ef skilyrðin hafa verið uppfyllt. Tengda upphæðin er sett í reitinn **Reikningsafsl.upphæð** .
7. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga. Nánari upplýsingar um hvað gerist þegar innkaupaskjöl eru bókuð eru [í Bókun innkaupa](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er yfirleitt vegna sléttunarútreiknings í tengslum við virðisaukaskatt eða söluskatt.
>
> Til að kanna upphæðirnar sem koma til með að vera bókaðar skal fara á síðuna **Tölfræði** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

## Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Til dæmis ef leiðrétta þarf dæmi eða breyta innkaupum snemma í pantanaferlinu. Frekari upplýsingar eru í [Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Til að bakfæra innkaup fyrir vörur eða þjónustu á bókuðum innkaupareikningi sem greiðslan er unnin fyrir skal stofna innkaupakreditreikning. Frekari upplýsingar eru í [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md).

[Opnaðu **Bókaðir innkaupareikningar** listann ](https://businesscentral.dynamics.com/?page=146) í [!INCLUDE [prod_short](includes/prod_short.md)].

## Innkaup á utanbirgðavörum

Línurnar í innkaupareikningi geta verið af tegundinni **Forði** eða **Vara**. Birgðaspjöld er hægt að flokka frekar eins og af tegundinni **Birgðir**, **Þjónusta** eða **Ekki-birgðir, sem tilgreinir hvort varan er raunbirgðaeining**, vinnustundaeining (einnig viðeigandi fyrir forða) eða efnisleg eining sem ekki er í birgðum. Frekari upplýsingar eru á [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningsferlið er það sama fyrir allar tegundirnar.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar má finna á [Setja upp tilföng](projects-how-setup-resources.md).
>
> Ef nota á keyptan forða þarf ef til vill að stilla forðagetuna og úthluta honum handvirkt til verkefnis. Kaup á tilfangi stofnar fjáhagsforðafærslu, en fjárhagsfærslur tilfangs eru hins vegar ekki raktar fyrir magni og virði eins og t.d. vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

## Hvenær á að nota innkaupapantanir

Nota innkaupapantanir ef skrá þarf hlutamóttöku af pöntunarmagni. Til dæmis vegna þess að allt magnið er ekki tiltækt hjá lánardrottninum. Ef seldar vörur eru afhentar beint frá lánardrottni til viðskiptamanns sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).

Að öðru leyti virka innkaupapantanir eins og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## Taka á móti vörum með innkaupapöntun

Eftirfarandi skref útskýra hvernig á að taka á móti vörum með innkaupapöntun. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir**, velja síðan viðkomandi tengil.
2. Opna innkaupapöntun sem þegar er til eða stofna nýja.
3. Í reitnum **Magn til móttöku** er fært inn magnið sem hefur verið móttekið.

   > [!NOTE]
   > Ef móttekið magn er meira en magnið í innkaupapöntuninni og lánardrottinn hefur verið settur upp til að leyfa ofmóttökur skal nota reitinn **Yfirmóttaka** til að sjá um umframmagnið. Fræðast meira um hlutann [Til að fá fleiri vörur en pantaðar voru](purchasing-how-record-purchases.md#receive-more-items-than-you-ordered) .
4. Valið er **Bóka** aðgerðin.

  Gildið í reitnum **Móttekið magn** er uppfært. Ef þessi móttaka er að hluta er gildið lægra en gildið í reitnum **Magn** .

> [!NOTE]
> Ef vöruhúsastjórnun er notuð er ekki hægt að nota aðgerðina **Bóka** á innkaupapöntuninni til að skrá móttöku. Það er vegna þess að starfsmaður í vöruhúsi hefur þegar bókað magn innkaupapöntunarinnar sem móttekið. Nánari upplýsingar um [hönnun - Vöruhúsaflæði](design-details-inbound-warehouse-flow.md) á innleið.

## Taka á móti fleiri vörum en pantaðar voru

Þegar fleiri vörur berast en voru pantaðar er hægt að taka á móti þeim í stað þess að hætta við móttökuna. Það gæti til dæmis verið ódýrara að halda óþarfa vörum í birgðum en skila þeim eða birgir gæti boðið afslátt af því að halda þeim.

Eftirfarandi myndband sýnir hvernig á að vinna með ofmóttökur.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2PE]

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### Setja upp umframmóttöku

Stofna yfirmóttökukóta til að skilgreina prósentu sem móttekið magn getur farið yfir pantað magn. Prósentan er tilgreind í reitnum **Vikmörk yfirmóttöku %** . Síðan er kótanum úthlutað á síðurnar Birgðaspjald eða Lánardrottnaspjald fyrir vörur og lánardrottna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **yfirmóttökukóta** og velja síðan viðeigandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Úthluta vöru ofmóttökukóta

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Opna skal síðuna **Birgðaspjald** fyrir vöruna.
3. Í reitnum **Yfirmóttökukóti** er valinn kótinn sem inniheldur prósentuna sem leyfa á fyrir yfirmóttökur.

Kóði umframmóttöku er úthlutaður á vöruna. Innkaupapantanir eða vöruhúsamóttökur fyrir vöruna gera nú kleift að taka á móti meira en pantað magn innan vikmarkaprósentu ofmóttöku.

> [!NOTE]
> Hægt er að setja upp samþykktarverkflæði til að krefjast þess að umframmóttökur verði samþykktar áður en unnið er með þær. Velja skal gátreitinn **Samþykkt nauðsynlegt** á síðunni **Yfirmóttökukótar** . Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).

### Pöntun of móttekin

Í innkaupalínum og vöruhúsamóttökulínum er reiturinn **Magn umframmóttöku** notaður til að skrá magn umframmóttöku, sem þýðir magn sem fer umfram gildið fyrir pantað magn í reitnum **Magn**.

Þegar ofmóttaka er meðhöndluð er hægt að hækka gildið í reitnum **Magn til móttöku** í móttekið magn. Reiturinn **Magn yfirmóttöku** uppfærist þannig að það sýni umframmagn. Önnur leið er að færa inn umframmagnið í reitinn **Magn umframmóttöku**. Reiturinn **Magn til móttöku** uppfærist þannig að það sýni pantað magn plús umframmagn. Eftirfarandi ferli útskýrir hvernig á að fylla út reitinn **Magn til móttöku**.  

1. Á innkaupapöntun eða vöruhúsamóttökuskjali þar sem móttekið magn er hærra en pantað er fært inn móttekið magn í reitinn **Magn til móttöku** .

    Ef aukningin er innan vikmarkanna sem tilgreind eru með úthlutaðum ofmóttökukóta **uppfærist reiturinn Magn** yfirmóttöku til að sýna magnið sem farið er fram úr gildinu í reitnum **Magn** .

    Ef hækkunin er yfir vikmörkunum er ofmóttakan ekki leyfð. Kanna hvort annar yfirmóttökukóti leyfir hann. Annars er aðeins hægt að taka á móti pöntuðu magni og afgreiða þarf umframmagnið á annan hátt, t.d. með því að skila því til lánardrottins.

2. Móttakan er bókuð eins og aðrar móttökur.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] sér ekki sjálfkrafa um fjárhagslega þætti fyrir ofmóttökur. Þetta þarf að vinna handvirkt í samkomulagi við lánardrottin, til dæmis getur lánardrottinn framsent nýjan eða uppfærðan reikning.

## Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Bókun innkaupa

Í innkaupaskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Forskoðun bókunar**
* **Bóka og prenta**
<!--* **Test Report**-->
* **Bóka runu**

Þegar innkaupaskjal er bókað eru reikningur lánardrottins, fjárhagurinn, birgðabókarfærslur og forðafærslur uppfærðar.

Fyrir hvert innkaupaskjal er innkaupafærsla stofnuð í töflunni **Fjárhagsfærsla**. Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Auk þess getur bókun innkaupanna leitt til virðisaukaskattsfærslu (VSK) og fjárhagsfærslu vegna afsláttarupphæðarinnar. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Innkaupagrunnur**.

Fyrir hverja innkaupalínu, eftir því sem við á, eru færslur stofnaðar í:

* Taflan **Birgðafærsla** ef innkaupalínan er af gerðinni **Vara**.
* Taflan **Fjárhagsfærsla** ef innkaupalínan er af gerðinni **Fjárhagsreikningur**.
* Taflan **Forðafærsla** ef innkaupalínan er af gerðinni **Forði**.

Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**.

Alltaf er hægt að fara yfir ýmsar færslur sem stofnaðar eru vegna bókana. Velja **Forskoðunarbókun** til að staðfesta skjal og skoða áætlaðar færslur.


> [!IMPORTANT]  
> Hægt er að stofna bæði móttöku og reikning þegar innkaupapöntun er bókuð. Það er hægt að gera samhliða eða hvort í sínu lagi. Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er. Athugaðu að ekki er hægt að stofna innkaupareikning úr innkaupapöntun fyrir vörur eða þjónustu sem ekki hefur verið tekið á móti. Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.

Hægt er annað hvort að bóka, eða bóka og prenta. Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar. Einnig er hægt að velja aðgerðina **Bóka runu** til að bóka ýmsar pantanir samtímis. Frekari upplýsingar eru í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

## Fjárhagsfærslur skoðaðar

Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Síðan eru bókaðar færslur tiltækar á ýmsum síðum, þar á meðal á síðunum Lánardr.færslur **,** Fjárhagsfærslur **,** Birgðafærslur **,** Forðafærslur **,** Innkaupamóttökur **og** Bókaðir **innkaupareikningar** .

Í flestum tilfellum er hægt að opna fjárhagsfærslur úr viðkomandi spjaldi eða skjali. Á síðunni **Lánardrottnaspjald** skal t.d. velja aðgerðina **Færslur**.

## Breyta fjárhagsfærslum

Þú getur breytt ákveðnum reitum í bókuðum innkaupaskjölum, t.d. reitnum **Greiðslutilvísun**. Frekari upplýsingar má finna í [Breyting á bókuðum skjölum](across-edit-posted-document.md). Til að fá fleiri mikilvæg svæði sem hafa áhrif á endurskoðunarslóðina þarf að bakfæra eða afturkalla bókun. Frekari upplýsingar eru í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

## Sjá einnig .

[Biðja um tilboð](purchasing-how-request-quotes.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Undirbúa beina sendingu](sales-how-drop-shipment.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Setja upp forða](projects-how-setup-resources.md)  
[Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Bóka mörg skjöl á sama tíma](ui-batch-posting.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
