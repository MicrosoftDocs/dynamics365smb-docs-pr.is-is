---
title: Skrá innkaup með innkaupareikningum (inniheldur myndskeið)
description: Lýsir því hvernig á að kaupa birgðir, vörur sem eru ekki birgðavara eða forða með því að stofna og bóka innkaupareikninga eða -pantanir.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310
ms.date: 09/01/2022
ms.author: edupont
ms.openlocfilehash: daedfacb3e496fa668095916b07caa7488765a83
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535478"
---
# <a name="record-purchases-with-purchase-invoices"></a>Skrá innkaup með innkaupareikningum

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Innkaupareikningar og innkaupapantanir eru líka notuð til að uppfæra birgðastig gagnvirkt, sem þýðir að hægt er að lágmarka birgðakostnað og bjóða upp á betri þjónustu við viðskiptamenn. Innkaupakostnaður, að þjónustukostnaði meðtöldum og birgðavirði af völdum bókunar innkaupareikninga eða -pantana verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í „Mínu hlutverki“.

## <a name="create-purchase-invoices"></a>Stofna innkaupareikninga

Ásamt því að kaupa efnislegar vörur (vörugerðina **Birgðir**), sem hefur áhrif á birgðamat, er hægt að kaupa þjónustu sem gefin er upp í tímaeiningum. Hægt er að gera þetta annaðhvort með vörugerðinni **Þjónusta** eða línugerðinni **Forði**.

Þegar þú tekur við birgðavörum eða þegar innkaupaaðgerð er lokið bókarðu innkaupareikninginn eða -pöntun til að uppfæra birgðir og fjármálaskrár og til að virkja greiðslu til lánardrottins, samkvæmt greiðsluskilmálum. Frekari upplýsingar er að finna í [Bókun innkaupa](ui-post-purchases.md), [Taka á móti vörum](warehouse-how-receive-items.md) og [Framkvæma greiðslur](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

### <a name="create-a-purchase-invoice"></a>Stofna innkaupareikning

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

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.  

> [!NOTE]
> Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er yfirleitt vegna sléttunarútreiknings í tengslum við virðisaukaskatt eða söluskatt.
>
> Til að kanna upphæðirnar sem koma til með að vera bókaðar skal fara á síðuna **Tölfræði** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

## <a name="when-to-use-purchase-orders"></a>Hvenær á að nota innkaupapantanir

Nota þarf innkaupapantanir ef innkaupaferlið krefst þess að hægt sé að skrá hlutamóttökur pöntunarmagns, til dæmis þar sem allt magnið er ekki tiltækt hjá lánardrottni. Ef seldar vörur eru afhentar beint frá lánardrottni til viðskiptamanns sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).

Að öðru leyti virka innkaupapantanir eins og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="purchasing-non-inventory-items"></a>Vöruinnkaup á öðru en birgðavörum

Línurnar í innkaupareikningi geta verið af tegundinni **Forði** eða **Vara**. Hægt er að flokka birgðaspjöld enn frekar sem tegundin **Birgðir**, **Þjónusta** eða **Ekki birgðavara**, sem gefur til kynna hvort varan sé efnisleg birgðaeining, vinnutímaeining (á einnig við um forða) eða efnisleg eining sem ekki er geymd í birgðum. Frekari upplýsingar eru á [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningsferlið er það sama fyrir allar tegundirnar.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar má finna á [Setja upp tilföng](projects-how-setup-resources.md).
>
> Til að nota keypt tilfang getur þurft að stilla afkastagetu tilfangs og tengja það handvirkt við verk. Kaup á tilfangi stofnar fjáhagsforðafærslu, en fjárhagsfærslur tilfangs eru hins vegar ekki raktar fyrir magni og virði eins og t.d. vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

## <a name="posted-invoices"></a>Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt þegar leiðrétta þarf innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu. Frekari upplýsingar eru í [Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Ef þegar hefur verið greitt fyrir vörur eða þjónustu á bókuðum innkaupareikningi, þá verður að búa til innkaupakreditreikning til að snúa við innkaupunum. Frekari upplýsingar eru í [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md).

[Opnaðu **Bókaðir innkaupareikningar** listann ](https://businesscentral.dynamics.com/?page=146) í [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Bókun innkaupa](ui-post-purchases.md)  
[Móttaka vara](warehouse-how-receive-items.md)  
[Biðja um tilboð](purchasing-how-request-quotes.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Undirbúa beina sendingu](sales-how-drop-shipment.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Setja upp forða](projects-how-setup-resources.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
