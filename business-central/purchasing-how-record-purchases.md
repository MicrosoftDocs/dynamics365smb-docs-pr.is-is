---
title: Skrá innkaup með innkaupareikningum (inniheldur Video)
description: Lýsir því hvernig á að kaupa birgðir, vörur sem eru ekki birgðavara eða forða með því að stofna og bóka innkaupareikninga eða -pantanir.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146
ms.date: 09/07/2021
ms.author: edupont
ms.openlocfilehash: 3d634e1ffb34cfdc0e4e7f6fc5e6ad4805cdabb5
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953035"
---
# <a name="record-purchases-with-purchase-invoices"></a>Skrá innkaup með innkaupareikningum

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Ef stjórna þarf birgðum eru innkaupareikningar og innkaupapantanir líka notaðir til að uppfæra birgðastig gagnvirkt svo að hægt sé að lágmarka birgðakostnað og veita betri þjónustu við viðskiptavini. Innkaupakostnaður, að þjónustukostnaði meðtöldum, og birgðavirði af völdum bókunar innkaupareikninga eða -pantana verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í Mitt hlutverk.

## <a name="create-purchase-invoices"></a>Stofna innkaupareikninga

Ásamt því að kaupa efnislegar vörur (vörugerðina **Birgðir**), sem hefur áhrif á birgðamat, er hægt að kaupa þjónustu sem gefin er upp í tímaeiningum. Hægt er að gera þetta annaðhvort með vörugerðinni **Þjónusta** eða línugerðinni **Forði**.

Þegar þú tekur við birgðavörum eða þegar innkaupaaðgerð er lokið bókarðu innkaupareikninginn eða -pöntun til að uppfæra birgðir og fjármálaskrár og til að virkja greiðslu til lánardrottins, samkvæmt greiðsluskilmálum. Frekari upplýsingar eru í [Bókun innkaupa](ui-post-purchases.md) og [Greiðslur framkvæmdar](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

### <a name="to-create-a-purchase-invoice"></a>Að Stofna innkaupareikning

Hér er því lýst hvernig á að búa til innkaupareikning. Skrefin eru svipuð fyrir innkaupapöntun. Helsti munurinn er sá að innkaupapantanir eru með viðbótarreiti og aðgerðir fyrir efnislega meðhöndlun á vörum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.  
2. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.

    Aðrir reitir á síðunni **Innkaupareikningur** eru nú fylltir út með stöðluðum upplýsingum um lánardrottin sem valinn hefur verið. Ef lánardrottinn er ekki skráður, fylgið eftirfarandi skrefum:

    1. Í reitnum **lánardrottinn** er fært inn nafn nýs lánardrottinn.
    2. Í svarglugganum um að skrá nýja lánardrottinn, veljið hnappinn **Já**.
    3. Frekari upplýsingar um hvernig á að fylla út kort lánardrottins er að finna í [Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).  
    4. Þegar lokið hefur verið við lánardrottinsspjaldið skal velja hnappinn **Í lagi** til að fara aftur á síðuna **Innkaupareikningur**.

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
    > Ef reikningsafslættir hafa verið settir upp fyrir lánardrottinn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur % lánardrottins** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð reiknings**.
7. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.  

> [!NOTE]
> Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Venjulega gerist það vegna sléttunarútreiknings í tengslum við virðisaukaskatt.
>
> Til að kanna upphæðirnar sem koma til með að vera bókaðar er hægt að nota síðuna **Tölfræðilegar upplýsingar** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

## <a name="when-to-use-purchase-orders"></a>Hvenær á að nota innkaupapantanir

Verður Að nota innkaupapantanir ef innkaupaferlið krefst þess að hægt sé að skrá hlutamóttökur pöntunarmagns , til dæmis þar sem allt magnið var ekki tiltæk í hjá lánardrottinn. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka innkaupapantanir á sama hátt og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="selling-non-inventory-items"></a>Sala vara sem eru ekki birgðavörur

Vörur á innkaupareikningi geta verið af gerðinni **Birgðir**, **Þjónusta**, **Tilföng** og **Ekki brigðir** til að tilgreina hvort vara er raunbirgðaeining, launatímaeining eða efnisleg eining sem ekki er geymd í birgðum. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningaferlið er það sama fyrir allar þrjár vörutegundir.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md).
>
> Til að nota keypt tilfang getur þurft að stilla afkastagetu tilfangs og tengja það handvirkt við verk. Kaup á tilfangi stofnar fjáhagsforðafærslu, en fjárhagsfærslur tilfangs eru hins vegar ekki raktar fyrir magni og virði eins og t.d. vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

## <a name="posted-invoices"></a>Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt þegar leiðrétta á innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu. Nánari upplýsingar er að finna [Ógreiddir innkaupareikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Ef þegar hefur verið greitt fyrir vörur eða þjónustu á bókuðum innkaupareikningi, þá verður að búa til innkaupakreditreikning til að snúa við innkaupunum. Nánari upplýsingar er að finna í [Vinna úr innkaupaskilum eða afturköllunum](purchasing-how-process-purchase-returns-cancellations.md).

[Opnaðu **Bókaðir innkaupareikningar** listann ](https://businesscentral.dynamics.com/?page=146) í [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

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
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]