---
title: Skrá innkaup með innkaupareikningum (inniheldur myndskeið)
description: 'Lýsir því hvernig á að kaupa birgðir, vörur sem eru ekki birgðavara eða forða með því að stofna og bóka innkaupareikninga eða -pantanir.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="record-purchases-with-purchase-invoices-and-orders" />Skrá innkaup með innkaupareikningum og pöntunum

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Innkaupareikningar og innkaupapantanir eru líka notuð til að uppfæra birgðastig gagnvirkt, sem þýðir að hægt er að lágmarka birgðakostnað og bjóða upp á betri þjónustu við viðskiptamenn. Innkaupakostnaður, að þjónustukostnaði meðtöldum og birgðavirði af völdum bókunar innkaupareikninga eða -pantana verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í „Mínu hlutverki“.

## <a name="record-purchases-with-purchase-invoices" />Skrá innkaup með innkaupareikningum

Þegar birgðavörum eða aðkeyptri þjónustu er lokið skal bóka innkaupareikning til að uppfæra birgðir og fjárhagslegar færslur og til að virkja greiðslu til lánardrottins samkvæmt greiðsluskilmálum. [Að ganga frá greiðslum](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

### <a name="create-a-and-post-purchase-invoice" />Stofna og bóka innkaupareikning

Hér er því lýst hvernig á að búa til innkaupareikning. Skrefin eru svipuð fyrir innkaupapöntun. Helsti munurinn er sá að innkaupapantanir eru með viðbótarreiti og aðgerðir fyrir efnislega meðhöndlun á vörum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar**, velja síðan viðkomandi tengil.  
2. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.

    Aðrir reitir á síðunni **Innkaupareikningur** eru nú fylltir út með stöðluðum upplýsingum fyrir valdan lánardrottin. Ef lánardrottinn er ekki skráður skal fylgja eftirfarandi skrefum:

    1. Í reitnum **lánardrottinn** er fært inn nafn nýs lánardrottinn.
    2. Í svarglugganum um að skrá nýjan lánardrottin skal velja **Já**.
    3. Frekari upplýsingar um hvernig á að fylla út lánardrottnaspjald er að finna í [Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).  
    4. Þegar lokið hefur verið við lánardrottnaspjaldið skal velja **Í lagi** til að fara aftur á síðuna **Innkaupareikningur**.

3. Fylltu í eftirstandandi reiti á síðunni **innkaupareikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Þú ert nú tilbúinn að fylla út innkaupareikningslínurnar með vörum eða tilföngum sem þú hefur keypt af lánardrottninum.

    > [!NOTE]  
    > Ef endurteknar innkaupalínur hafa verið settar upp fyrir lánardrottinn, svo sem mánaðarlegar áfyllingarpantanir, er hægt að færa línurnar inn í reikninginn með því að velja aðgerðina **Ítrekaðar innkaupalínur**.
4. Í flýtiflipanum **Línur** í reitnum **Vörunúmer** er sleginn inn fjöldi birgðavöru eða þjónustu.
5. Í reitinn **Magn** er fært fjöldi vara sem á að kaupa.

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **beint innkaupsverð** margfaldað með gildinu í reitnum **magn**.

    Verð- og línuupphæð eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á lánardrottinsspjaldinu.

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

6. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti** neðst á reikningnum.

    > [!NOTE]  
    > Ef reikningsafslættir hafa verið settir upp fyrir lánardrottin, þá er tilgreint prósentugildi sjálfkrafa sett inn í reitinn **Reikningsafsláttur lánardrottins %** ef skilyrðin hafa verið uppfyllt. Tengda upphæðin er sett inn í reitinn **Reikningsafsláttarupphæð**.
7. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.  Sjá  [posting innkaup fyrir frekari upplýsingar um hvað gerist þegar innkaupaskjöl eru bókuð](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er yfirleitt vegna sléttunarútreiknings í tengslum við virðisaukaskatt eða söluskatt.
>
> Til að kanna upphæðirnar sem koma til með að vera bókaðar skal fara á síðuna **Tölfræði** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

## <a name="posted-invoices" />Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt þegar leiðrétta þarf innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu. Frekari upplýsingar eru í [Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Ef þegar hefur verið greitt fyrir vörur eða þjónustu á bókuðum innkaupareikningi, þá verður að búa til innkaupakreditreikning til að snúa við innkaupunum. Frekari upplýsingar eru í [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md).

[Opnaðu **Bókaðir innkaupareikningar** listann ](https://businesscentral.dynamics.com/?page=146) í [!INCLUDE [prod_short](includes/prod_short.md)].


## <a name="purchasing-non-inventory-items" />Vöruinnkaup á öðru en birgðavörum

Línurnar í innkaupareikningi geta verið af tegundinni **Forði** eða **Vara**. Hægt er að flokka birgðaspjöld enn frekar sem tegundin **Birgðir**, **Þjónusta** eða **Ekki birgðavara**, sem gefur til kynna hvort varan sé efnisleg birgðaeining, vinnutímaeining (á einnig við um forða) eða efnisleg eining sem ekki er geymd í birgðum. Frekari upplýsingar eru á [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningsferlið er það sama fyrir allar tegundirnar.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar má finna á [Setja upp tilföng](projects-how-setup-resources.md).
>
> Til að nota keypt tilfang getur þurft að stilla afkastagetu tilfangs og tengja það handvirkt við verk. Kaup á tilfangi stofnar fjáhagsforðafærslu, en fjárhagsfærslur tilfangs eru hins vegar ekki raktar fyrir magni og virði eins og t.d. vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

## <a name="when-to-use-purchase-orders" />Hvenær á að nota innkaupapantanir

Nota þarf innkaupapantanir ef innkaupaferlið krefst þess að hægt sé að skrá hlutamóttökur pöntunarmagns, til dæmis þar sem allt magnið er ekki tiltækt hjá lánardrottni. Ef seldar vörur eru afhentar beint frá lánardrottni til viðskiptamanns sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).

Að öðru leyti virka innkaupapantanir eins og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order" />Taka á móti vörum með innkaupapöntun

Eftirfarandi lýsir því hvernig skal taka á móti vörum með innkaupapöntun. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir**, velja síðan viðkomandi tengil.
2. Opna innkaupapöntun sem þegar er til eða stofna nýja.
3. Í reitnum **Magn til móttöku** er fært inn magnið sem hefur verið móttekið.

   > [!NOTE]
   > Ef móttekið magn er meira en magnið í innkaupapöntuninni og lánardrottinn hefur verið settur upp við að leyfa afkvittanir er reiturinn yfir móttekið  **notaður**  til að sjá um umframmagnið. Frekari upplýsingar eru  [í til að taka á móti fleiri atriðum en pöntuðum](purchasing-how-record-purchases.md#receive-more-items-than-ordered)  kafla.
4. Valið er **Bóka** aðgerðin.

  Gildið í reitnum **Móttekið magn** er uppfært. Ef þetta er hlutainnhreyfing er gildið lægra en gildið í  **reitnum Magn** .

> [!NOTE]
> Ef vöruhúsaafgreiðsla er notuð er ekki hægt að nota  **aðgerðina Bóka**  á innkaupapöntuninni til að skrá móttöku. Það er vegna þess að starfsmaður vöruhúss hefur þegar bókað magn innkaupapöntunar sem móttekið. Frekari upplýsingar í hönnunarupplýsingum-flæði  [á innleið í](design-details-inbound-warehouse-flow.md) vöruhúsi.

## <a name="receive-more-items-than-ordered" />Taka á móti fleiri vörum en pantað er

Þegar fleiri vörur berast en voru pantaðar er heimilt að taka á móti þeim í stað þess að ógilda kvittunina. Til dæmis getur verið ódýrara að halda umframvörunum í birgðum en að skila þeim, eða seljanda er heimilt að bjóða afslátt fyrir að halda þeim.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts" />Setja upp umframmóttöku

Stofna yfir-kvittunarkóða til að skilgreina prósentu sem móttekið magn getur farið fram úr pöntuðu magni. Tilgreinið prósentuna í  **reitnum yfir-Innhreyfingarvikmörk%** . Síðan er kótinn á birgðaspjaldinu eða síðum lánardrottnaspjaldinu úthlutuð fyrir vörur og lánardrottna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **yfir-Móttökukóta** og veljið síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item" />Úthluta vörukvittunarkóta til vöru

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2.  **Opnið Vörukortasíðuna**  fyrir vöruna.
3.  **Í reitnum yfir-Móttökukóti**  er kótinn valinn sem inniheldur prósentuna sem á að leyfa fyrir yfir-innhreyfingar.

Kóði umframmóttöku er úthlutaður á vöruna. Innkaupapantanir eða vöruhúsamóttökur vörunnar leyfa nú að fá meira en pantað magn innan um vikmarkaprósentu yfir innhreyfingar.

> [!NOTE]
> Hægt er að setja upp samþykktarverkflæði til að krefjast þess að umframmóttökur verði samþykktar áður en unnið er með þær. Gátreiturinn samþykki er  **valinn á**  síðunni yfir-Kvittunarkótar  **.**  Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).

### <a name="over-receive-an-order" />Yfir-taka við pöntun

Í innkaupalínum og vöruhúsamóttökulínum er reiturinn **Magn umframmóttöku** notaður til að skrá magn umframmóttöku, sem þýðir magn sem fer umfram gildið fyrir pantað magn í reitnum **Magn**.

Þegar unnið er úr umframmóttöku er hægt að hækka gildið í reitnum **Magn til móttöku** upp í móttekið raunmagn.  **Uppfærslur magns**  -kvittunar sem sýna umframmagn. Önnur leið er að færa inn umframmagnið í reitinn **Magn umframmóttöku**.  **Magn til að taka**  við uppfærslum á svæði til að sýna pantað magn auk umframmagns. Eftirfarandi ferli útskýrir hvernig á að fylla út reitinn **Magn til móttöku**.  

1. Í innkaupapöntun eða fylgiskjali vöruhúsamóttöku, þar sem móttekið magn er hærra en pantað magn, skal færa inn raunverulegt móttekið magn í reitinn **Magn til móttöku**.

    Ef Hækkunin er innan vikmarka sem tilgreind eru í úthlutuðu magni yfir-kvittunarkóða,  **uppfærist reiturinn yfir-innhreyfingar magn**  til að sýna magnið með því að farið er yfir gildið í  **reitnum Magn** .

    Ef Hækkunin er yfir vikmörkin er ekki leyfilegt að fá yfir-kvittunina. Rannsaka hvort annar yfir-kvittunarkóði leyfir það. Annars er aðeins hægt að taka á móti pöntuðu magni og afgreiða þarf umframmagnið á annan hátt, t.d. með því að skila því til lánardrottins.

2. Móttakan er bókuð eins og önnur kvittun.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] ræður ekki sjálfkrafa fjárhagslegum þáttum yfir-kvittunum. Þetta þarf að vinna handvirkt í samkomulagi við lánardrottin, til dæmis getur lánardrottinn framsent nýjan eða uppfærðan reikning.

## <a name="external-document-number" />Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases" />Bókun innkaupa

Í innkaupaskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Forskoðun bókunar**
* **Bóka og prenta**
<!--* **Test Report**-->
* **Bóka runu**

Þegar innkaupaskjal er bókað eru reikningur lánardrottins, fjárhagurinn, birgðabókarfærslur og forðafærslur uppfærðar.

Fyrir hvert innkaupaskjal er innkaupafærsla stofnuð í töflunni **Fjárhagsfærsla**. Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu fyrir afsláttarupphæðina. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Innkaupagrunnur**.

Fyrir hverja innkaupalínu, eftir því sem við á, eru færslur stofnaðar í:

* Taflan **Birgðafærsla** ef innkaupalínan er af gerðinni **Vara**.
* Taflan **Fjárhagsfærsla** ef innkaupalínan er af gerðinni **Fjárhagsreikningur**.
* Taflan **Forðafærsla** ef innkaupalínan er af gerðinni **Forði**.

Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**.

Alltaf er hægt að fara yfir ýmsar færslur sem stofnaðar verða í kjölfar bókanna. Velja  **forskoðunarbókun**  til að villuleita í skjalinu og skoða væntanlegar færslur.


> [!IMPORTANT]  
> Hægt er að stofna bæði móttöku og reikning þegar innkaupapöntun er bókuð. Það er hægt að gera samhliða eða hvort í sínu lagi. Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er. Athugaðu að ekki er hægt að stofna innkaupareikning úr innkaupapöntun fyrir vörur eða þjónustu sem ekki hefur verið tekið á móti. Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.

Hægt er annað hvort að bóka, eða bóka og prenta. Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar. Einnig er hægt að velja aðgerðina **Bóka runu** til að bóka ýmsar pantanir samtímis. Frekari upplýsingar eru í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

## <a name="viewing-ledger-entries" />Fjárhagsfærslur skoðaðar

Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að þessu loknu verður hægt að sjá bókuðu færslurnar á ýmsum síðum, þ.m.t. síðunum **Lánardrottnafærslur**, **Fjárhagsfærslur**, **Birgðabókafærslur**, **Forðafærslur**, **Innkaupakvittanir** og **Bókaðir innkaupareikningar**.

Í flestum tilfellum er hægt að opna fjárhagsfærslur úr viðkomandi spjaldi eða skjali. Á síðunni **Lánardrottnaspjald** skal t.d. velja aðgerðina **Færslur**.

## <a name="editing-ledger-entries" />Breyta fjárhagsfærslum

Þú getur breytt ákveðnum reitum í bókuðum innkaupaskjölum, t.d. reitnum **Greiðslutilvísun**. Frekari upplýsingar má finna í [Breyting á bókuðum skjölum](across-edit-posted-document.md). Til að fá fleiri mikilvæg svæði sem hafa áhrif á endurskoðunarslóðina þarf að bakfæra eða afturkalla bókun. Frekari upplýsingar eru í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-trainingtrainingmodulesreceive-invoice-dynamics-d365-business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-related-microsoft-trainingtrainingmodulesprocessing-invoices-dynamics-365-business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also" />Sjá einnig .

[Biðja um tilboð](purchasing-how-request-quotes.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Undirbúa beina sendingu](sales-how-drop-shipment.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Setja upp forða](projects-how-setup-resources.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Bóka mörg skjöl á sama tíma](ui-batch-posting.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
