---
title: Skrá innkaup með innkaupareikningum (inniheldur myndskeið)
description: 'Lýsir því hvernig á að kaupa birgðir, vörur sem eru ekki birgðavara eða forða með því að stofna og bóka innkaupareikninga eða -pantanir.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 12/19/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Skráðu innkaup með innkaupareikningum og pöntunum

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Innkaupareikningar og innkaupapantanir eru líka notuð til að uppfæra birgðastig gagnvirkt, sem þýðir að hægt er að lágmarka birgðakostnað og bjóða upp á betri þjónustu við viðskiptamenn. Innkaupakostnaðurinn, þ.mt þjónustukostnaður, og birgðaverðmæti sem verða til við bókun innkaupareikninga eða pantana, stuðla að hagnaðartölum og öðrum fjárhagslegum lykilárangursvísum (KPIs) í hlutverkamiðstöðinni þinni.

## Skrá innkaup með innkaupareikningum

Þegar þú færð birgðavörurnar eða keyptri þjónustu er lokið skaltu bóka innkaupareikninginn til að uppfæra birgða- og fjárhagsfærslur og virkja greiðslu til lánardrottins samkvæmt greiðsluskilmálum. [Að gera greiðslur](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

### Stofna og bóka innkaupareikning

Eftirfarandi skref lýsa því hvernig á að búa til innkaupareikning. Skrefin til að búa til innkaupapöntun eru svipuð. Helsti munurinn er sá að innkaupapantanir hafa nokkra aukareiti og aðgerðir fyrir líkamlega meðhöndlun á hlutum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar**, velja síðan viðkomandi tengil.  
2. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.

    Aðrir reitir á síðunni **Innkaupareikningur** eru nú fylltir út með stöðluðum upplýsingum fyrir valdan lánardrottin. Ef söluaðilinn er ekki skráður skaltu fylgja þessum skrefum:

    1. Í reitnum **lánardrottinn** er fært inn nafn nýs lánardrottinn.
    2. Í svarglugganum um að skrá nýjan lánardrottin skal velja **Já**.
    3. Frekari upplýsingar um hvernig á að fylla út lánardrottnaspjald er að finna í [Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).  
    4. Þegar þú hefur lokið við lánardrottinspjaldið skaltu velja **Í lagi** til að fara aftur á  **Innreikningur** síðuna.

3. Fylltu í eftirstandandi reiti á síðunni **innkaupareikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Þú ert nú tilbúinn til að fylla út innkaupareikningslínurnar með vörum eða tilföngum sem keypt eru af lánardrottni.

    > [!NOTE]  
    > Ef endurteknar innkaupalínur hafa verið settar upp fyrir lánardrottinn, svo sem mánaðarlegar áfyllingarpantanir, er hægt að færa línurnar inn í reikninginn með því að velja aðgerðina **Ítrekaðar innkaupalínur**.
4. Í flýtiflipanum **Línur** í reitnum **Vörunúmer** er sleginn inn fjöldi birgðavöru eða þjónustu.
5. Í reitinn **Magn** er fært fjöldi vara sem á að kaupa.

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **beint innkaupsverð** margfaldað með gildinu í reitnum **magn**.

    Verð og línuupphæð eru sýnd með eða án söluskatts eftir því sem þú velur í  **Verð með skatti** reitnum á lánardrottinsspjaldinu.

    Heildarreitirnir undir línunum eru sjálfkrafa uppfærðir þegar þú býrð til eða breytir línum til að birta upphæðirnar sem eru bókaðar í fjárhagsbókina.

6. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti** neðst á reikningnum.

    > [!NOTE]  
    > Ef reikningsafslættir hafa verið settir upp fyrir lánardrottin, þá er tilgreint prósentugildi sjálfkrafa sett inn í reitinn **Reikningsafsláttur lánardrottins %** ef skilyrðin hafa verið uppfyllt. Tengda upphæðin er sett inn í reitinn **Reikningsafsláttarupphæð**.
7. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.  Fyrir frekari upplýsingar um hvað gerist þegar þú bókar innkaupaskjöl, sjá [Bóka innkaup](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er yfirleitt vegna sléttunarútreiknings í tengslum við virðisaukaskatt eða söluskatt.
>
> Til að kanna upphæðirnar sem koma til með að vera bókaðar skal fara á síðuna **Tölfræði** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

## Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt þegar leiðrétta þarf innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu. Frekari upplýsingar eru í [Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Til að bakfæra kaup fyrir vörur eða þjónustu sem skráðar eru á bókuðum innkaupareikningi sem greiðslan er afgreidd fyrir, verður að búa til innkaupakreditreikning. Frekari upplýsingar eru í [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md).

[Opnaðu **Bókaðir innkaupareikningar** listann ](https://businesscentral.dynamics.com/?page=146) í [!INCLUDE [prod_short](includes/prod_short.md)].


## Vöruinnkaup á öðru en birgðavörum

Línurnar í innkaupareikningi geta verið af tegundinni **Forði** eða **Vara**. Hægt er að flokka vörukort frekar eftir  **birgðum**, **þjónustu** eða **Non -Birgða** gerð, sem tilgreinir hvort varan sé efnisleg birgðaeining, vinnutímaeining (á við um tilföng) eða efnisleg eining sem er ekki geymd í birgðum. Frekari upplýsingar eru á [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningsferlið er það sama fyrir allar tegundirnar.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar má finna á [Setja upp tilföng](projects-how-setup-resources.md).
>
> Til að nota keypt tilfang getur þurft að stilla afkastagetu tilfangs og tengja það handvirkt við verk. Kaup á tilfangi stofnar fjáhagsforðafærslu, en fjárhagsfærslur tilfangs eru hins vegar ekki raktar fyrir magni og virði eins og t.d. vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

## Hvenær á að nota innkaupapantanir

Þú verður að nota innkaupapantanir ef innkaupaferli þitt krefst þess að þú skráir hlutakvittanir á pöntunarmagni, til dæmis vegna þess að allt magnið er ekki tiltækt hjá lánardrottni. Ef seldar vörur eru afhentar beint frá lánardrottni til viðskiptamanns sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).

Að öðru leyti virka innkaupapantanir eins og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## Taka á móti vörum með innkaupapöntun

Eftirfarandi skref lýsa því hvernig á að taka á móti vörum með innkaupapöntun. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir**, velja síðan viðkomandi tengil.
2. Opna innkaupapöntun sem þegar er til eða stofna nýja.
3. Í reitnum **Magn til móttöku** er fært inn magnið sem hefur verið móttekið.

   > [!NOTE]
   > Ef móttekið magn er meira en magnið í innkaupapöntuninni, og seljandi hefur verið settur upp til að leyfa ofgreiðslur, skal nota reitinn **Ofmóttaka** til að meðhöndla umfram magn. Lærðu meira í [Til að fá fleiri vörur en pantaðar](purchasing-how-record-purchases.md#receive-more-items-than-ordered) hlutanum.
4. Valið er **Bóka** aðgerðin.

  Gildið í reitnum **Móttekið magn** er uppfært. Ef þetta er kvittun að hluta er gildið lægra en gildið í **Magn** reitnum.

> [!NOTE]
> Ef þú notar vöruhúsameðferð geturðu ekki notað **Posta** aðgerðina á innkaupapöntuninni til að skrá kvittun. Það er vegna þess að starfsmaður vöruhúss hefur þegar bókað innkaupapöntunarmagnið eins og það var móttekið. Lærðu meira á [Hönnunarupplýsingar - Innleið vöruhúsaflæði](design-details-inbound-warehouse-flow.md).

## Taka á móti fleiri vörum en pantað er

Þegar fleiri vörur berast en pantaðar voru gætirðu viljað fá þær í staðinn fyrir að hætta við móttökuna. Til dæmis gæti verið ódýrara að geyma umframvörur í birgðum en skila þeim, eða söluaðili gæti boðið afslátt fyrir að halda þeim.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### Setja upp umframmóttöku

Stofna yfir móttökukóða til að skilgreina prósentu sem móttekið magn getur farið yfir pantað magn. Tilgreindu hlutfallið í reitnum **Umskilið umfram móttöku %** . Þú úthlutar síðan kóðanum á Vörukorti eða Lánardrottnaspjaldi síðum fyrir vörur og lánardrottna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Kóða fyrir yfirtöku** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Úthlutaðu ofurkvittunarkóða til vöru

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Opnaðu **Vörukort** síðuna fyrir hlutinn.
3. Í reitnum **Kóði fyrir ofurkvittun**  skaltu velja kóðann sem inniheldur prósentuna sem þú vilt leyfa fyrir ofgreiðslur.

Kóði umframmóttöku er úthlutaður á vöruna. Innkaupapantanir eða vöruhúsakvittanir fyrir vöruna gera þér nú kleift að fá meira en pantað magn innan vikmörkunarprósentu umfram móttöku.

> [!NOTE]
> Hægt er að setja upp samþykktarverkflæði til að krefjast þess að umframmóttökur verði samþykktar áður en unnið er með þær. Veljið gátreitinn **Samþykki krafist** á síðunni **Kóðar fyrir yfirtöku** . Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).

### Taka of mikið á móti pöntun

Í innkaupalínum og vöruhúsamóttökulínum er reiturinn **Magn umframmóttöku** notaður til að skrá magn umframmóttöku, sem þýðir magn sem fer umfram gildið fyrir pantað magn í reitnum **Magn**.

Þegar unnið er úr umframmóttöku er hægt að hækka gildið í reitnum **Magn til móttöku** upp í móttekið raunmagn. Reiturinn **Mikið magn af móttöku** uppfærslur til að sýna umframmagnið. Önnur leið er að færa inn umframmagnið í reitinn **Magn umframmóttöku**.  **Magn. til að fá** uppfærslur á reit til að sýna pantað magn auk umframmagns. Eftirfarandi ferli útskýrir hvernig á að fylla út reitinn **Magn til móttöku**.  

1. Í innkaupapöntun eða fylgiskjali vöruhúsamóttöku, þar sem móttekið magn er hærra en pantað magn, skal færa inn raunverulegt móttekið magn í reitinn **Magn til móttöku**.

    Ef aukningin er innan vikmörkanna sem tilgreind er með úthlutaðri ofurkvittunarkóða, uppfærist **Magn umframkvittunar** til að sýna magnið sem gildið í **Farið er yfir Magn** reitinn.

    Ef hækkunin er yfir vikmörkunum er ofurkvittun ekki leyfð. Kanna hvort annar ofurkvittunarkóði leyfir það. Annars er aðeins hægt að taka á móti pöntuðu magni og afgreiða þarf umframmagnið á annan hátt, t.d. með því að skila því til lánardrottins.

2. Bókaðu kvittunina eins og þú myndir gera allar aðrar kvittanir.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] sinnir ekki sjálfkrafa fjárhagslegum þáttum oftekna. Þetta þarf að vinna handvirkt í samkomulagi við lánardrottin, til dæmis getur lánardrottinn framsent nýjan eða uppfærðan reikning.

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

Fyrir hvert innkaupaskjal er innkaupafærsla stofnuð í töflunni **Fjárhagsfærsla**. Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Að auki getur bókun kaupanna leitt til virðisaukaskatts (VSK) færslu og bókunarfærslu fyrir afsláttarupphæðina. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Innkaupagrunnur**.

Fyrir hverja innkaupalínu, eftir því sem við á, eru færslur stofnaðar í:

* Taflan **Birgðafærsla** ef innkaupalínan er af gerðinni **Vara**.
* Taflan **Fjárhagsfærsla** ef innkaupalínan er af gerðinni **Fjárhagsreikningur**.
* Taflan **Forðafærsla** ef innkaupalínan er af gerðinni **Forði**.

Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**.

Þú getur alltaf skoðað ýmsar fjárhagsfærslur sem eru búnar til vegna bókana. Veldu **Forskoða bókun** til að staðfesta skjal og skoða væntanlegar fjárhagsfærslur.


> [!IMPORTANT]  
> Hægt er að stofna bæði móttöku og reikning þegar innkaupapöntun er bókuð. Það er hægt að gera samhliða eða hvort í sínu lagi. Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er. Athugaðu að ekki er hægt að stofna innkaupareikning úr innkaupapöntun fyrir vörur eða þjónustu sem ekki hefur verið tekið á móti. Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.

Hægt er annað hvort að bóka, eða bóka og prenta. Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar. Einnig er hægt að velja aðgerðina **Bóka runu** til að bóka ýmsar pantanir samtímis. Frekari upplýsingar eru í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

## Fjárhagsfærslur skoðaðar

Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að þessu loknu verður hægt að sjá bókuðu færslurnar á ýmsum síðum, þ.m.t. síðunum **Lánardrottnafærslur**, **Fjárhagsfærslur**, **Birgðabókafærslur**, **Forðafærslur**, **Innkaupakvittanir** og **Bókaðir innkaupareikningar**.

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
