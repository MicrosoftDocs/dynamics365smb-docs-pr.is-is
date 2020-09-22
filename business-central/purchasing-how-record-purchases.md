---
title: Stofna innkaupareikning og skrá innkaup | Microsoft Docs
description: Lýsir því hvernig á að kaupa birgðir, vörur sem eru ekki birgðavara eða forða með því að stofna og bóka innkaupareikninga eða -pantanir.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 7d01903b88919c498e804429c10be1beae7baf05
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783000"
---
# <a name="record-purchases"></a>Skrá innkaup
Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Ef stjórna þarf birgðum eru innkaupareikningar og innkaupapantanir líka notaðir til að uppfæra birgðastig gagnvirkt svo að hægt sé að lágmarka birgðakostnað og veita betri þjónustu við viðskiptavini. Innkaupakostnaður, að þjónustukostnaði meðtöldum, og birgðavirði af völdum bókunar innkaupareikninga eða -pantana verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í Mitt hlutverk.

Ásamt því að kaupa efnislegar vörur (vörugerðina **Birgðir**), sem hefur áhrif á birgðamat, er hægt að kaupa þjónustu sem gefin er upp í tímaeiningum. Hægt er að gera þetta annaðhvort með vörugerðinni **Þjónusta** eða línugerðinni **Forði**.

> [!NOTE]  
> Verður Að nota innkaupapantanir ef innkaupaferlið krefst þess að hægt sé að skrá hlutamóttökur pöntunarmagns , til dæmis þar sem allt magnið var ekki tiltæk í hjá lánardrottinn. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka innkaupapantanir á sama hátt og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

Þegar þú tekur við birgðavörum eða þegar innkaupaaðgerð er lokið bókarðu innkaupareikninginn eða -pöntun til að uppfæra birgðir og fjármálaskrár og til að virkja greiðslu til lánardrottins, samkvæmt greiðsluskilmálum. Frekari upplýsingar eru í [Bókun innkaupa](ui-post-purchases.md) og [Greiðslur framkvæmdar](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt þegar leiðrétta á innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu. Nánari upplýsingar er að finna [Ógreiddir innkaupareikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Ef þegar hefur verið greitt fyrir vörur eða þjónustu á bókuðum innkaupareikningi, þá verður að búa til innkaupakreditreikning til að snúa við innkaupunum. Nánari upplýsingar er að finna í [Vinna úr innkaupaskilum eða afturköllunum](purchasing-how-process-purchase-returns-cancellations.md).

Birgðaspjaldið getur verið af gerðinni **Birgðir**, **Þjónusta** og **Ekki birgðir** til að tilgreina hvort vara er raunbirgðaeining, launatímaeining eða efnisleg eining sem ekki er geymd í birgðum. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningaferlið er það sama fyrir allar þrjár vörutegundir.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md).<br /><br />
> Til að nota keypt tilfang getur þurft að stilla afkastagetu tilfangs og tengja það handvirkt við verk. Kaup á tilfangi stofnar fjáhagsforðafærslu, en fjárhagsfærslur tilfangs eru hins vegar ekki raktar fyrir magni og virði eins og t.d. vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

Hægt er að fylla út  lánardrottnareitina í innkaupareikningunum með tveimur leiðum, eftir því hvort lánardrottinninn hefur þegar verið skráður.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="to-create-a-purchase-invoice"></a>Að Stofna innkaupareikning
Hér er því lýst hvernig á að búa til innkaupareikning. Skrefin eru svipuð fyrir innkaupapöntun. Helsti munurinn er sá að innkaupapantanir eru með viðbótarreiti og aðgerðir fyrir efnislega meðhöndlun á vörum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.  
2. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.

    Aðrir reitir á síðunni **Innkaupareikningur** eru nú fylltir út með stöðluðum upplýsingum um lánardrottin sem valinn hefur verið. Ef lánardrottinn er ekki skráður, fylgið eftirfarandi skrefum:
3. Í reitnum **lánardrottinn** er fært inn nafn nýs lánardrottinn.
4. Í svarglugganum um að skrá nýja lánardrottinn, veljið hnappinn **Já**.
5. Á síðunni **Velja sniðmát fyrir nýjan lánardrottinn**, skal velja sniðmát til að byggja nýja lánardrottnaspjaldið á og veljið hnappinn **Í lagi**.
6. Nýtt viðskiptamannaspjald opnast, fyrirfram fyllt út með upplýsingnum á valda viðskiptamannasniðmátinu. Reiturinn **Heiti** er fyrirfram fylltur út með nafni nýja lánardrottins sem fært var inn á innkaupareikninginn.
7. Haltu áfram að fylla út eftirstandandi reiti á spjaldi lánardrottins. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).  
8. Þegar lokið hefur verið við lánardrottinsspjaldið skal velja hnappinn **Í lagi** til að fara aftur á síðuna **Innkaupareikningur**.

    Margir reitir á síðunni **innkaupareikningur** eru útfylltir með upplýsingar sem tilgreindar eru á nýju lánardrottinnspjaldi.
9. Fylltu í eftirstandandi reiti á síðunni **innkaupareikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Þú ert nú tilbúinn að fylla út innkaupareikningslínurnar með vörum eða tilföngum sem þú hefur keypt af lánardrottninum.

    > [!NOTE]  
    >   Ef endurteknar innkaupalínur hafa verið settar upp fyrir lánardrottinn, svo sem mánaðarlegar áfyllingarpantanir, er hægt að færa línurnar inn í reikninginn með því að velja aðgerðina **Ítrekaðar innkaupalínur**.
10. Í flýtiflipanum **Línur** í reitnum **Vörunúmer** er sleginn inn fjöldi birgðavöru eða þjónustu.
11. Í reitinn **Magn** er fært fjöldi vara sem á að kaupa.

    > [!NOTE]  
    >   Fyrir vörur af tegundinni **Þjónusta** og línur af gerðinni **Tilfang** er magnið tímaeining, t.d. klukkutímar, eins og gefið er til kynna í reitnum **Mælieiningarkóði** í línunni.

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **beint innkaupsverð** margfaldað með gildinu í reitnum **magn**.

    Verð- og línuupphæð eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á lánardrottinsspjaldinu.

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Venjulega gerist það vegna sléttunarútreiknings í tengslum við virðisaukaskatt.<br /><br />Til að kanna upphæðirnar sem koma til með að vera bókaðar er hægt að nota síðuna **Tölfræðilegar upplýsingar** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

12. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti** neðst á reikningnum.

    > [!NOTE]  
    >   Ef reikningsafslættir hafa verið settir upp fyrir lánardrottinn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur % lánardrottins** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð reiknings**.
13. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Setja upp forða](projects-how-setup-resources.md)  
[Bókun innkaupa](ui-post-purchases.md)  
[Biðja um tilboð](purchasing-how-request-quotes.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Undirbúa beina sendingu](sales-how-drop-shipment.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
