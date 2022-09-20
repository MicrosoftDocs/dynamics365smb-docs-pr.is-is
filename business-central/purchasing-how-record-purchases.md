---
title: Skrá innkaup með innkaupareikningum (inniheldur Video)
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
ms.openlocfilehash: e6f918a33b81ab7986fd0f2ec6bddb9dcc62fcc3
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460833"
---
# <a name="record-purchases-with-purchase-invoices"></a>Skrá innkaup með innkaupareikningum

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Innkaupareikningar og innkaupapantanir eru einnig notuð til að uppfæra birgðastig, sem þýðir að hægt er að lágmarka birgðakostnað og veita viðskiptavinum betri þjónustu. Innkaupakostnaður, þ.m.t. þjónustugjöld, og birgðagildi sem verða til við bókun innkaupareikninga eða pantana leggja til hagnaðartölur og aðra afkastavísa Afkastavídda (Afkastavísar) í hlutverkamiðstöðinni.

## <a name="create-purchase-invoices"></a>Stofna innkaupareikninga

Auk þess að kaupa efnislegar vörur (**birgðavörutegund**), sem hefur áhrif á birgðamat, er hægt að kaupa þjónustu fulltrúa tímaeininga. Hægt er að gera þetta annaðhvort með vörugerðinni **Þjónusta** eða línugerðinni **Forði**.

Þegar birgðavörum eða aðkeyptri þjónustu er lokið skal bóka innkaupareikning eða pöntun til að uppfæra birgðir og fjárhagslegar færslur og til að virkja greiðslu til lánardrottins samkvæmt greiðsluskilmálum. Frekari upplýsingar við [bókun innkaupa](ui-post-purchases.md), [taka á móti vörum](warehouse-how-receive-items.md) og [gera greiðslur](payables-make-payments.md).

> [!CAUTION]  
> Ekki bóka innkaupareikning efnislegra vara fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

### <a name="create-a-purchase-invoice"></a>Stofna innkaupareikning

Hér er því lýst hvernig á að búa til innkaupareikning. Skrefin eru svipuð fyrir innkaupapöntun. Helsti munurinn er sá að innkaupapantanir eru með viðbótarreiti og aðgerðir fyrir efnislega meðhöndlun á vörum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **innkaupareikninga** og velja síðan tengda tengilinn.  
2. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.

    Önnur svæði á **innkaupareikningi** eru nú fyllt út með stöðluðum upplýsingum um valinn lánardrottinn. Ef lánardrottinn er ekki skráður skal fara eftir þessum leiðbeiningum:

    1. Í reitnum **lánardrottinn** er fært inn nafn nýs lánardrottinn.
    2. Í svarglugganum um skráningu nýja lánardrottinsins er valið **Já**.
    3. Til að fræðast nánar um hvernig á að fylla út af lánardrottnaspjaldinu er farið í að [skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).  
    4. Þegar lánardrottnaspjaldinu hefur verið lokið er valið **í lagi** til að fara aftur **á síðuna innkaupareikningur**.

3. Fylltu í eftirstandandi reiti á síðunni **innkaupareikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Nú er hægt að fylla út innkaupareikning í línum með vörum eða forða sem keyptir hafa verið af lánardrottni.

    > [!NOTE]  
    > Ef endurteknar innkaupalínur hafa verið settar upp fyrir lánardrottinn, svo sem mánaðarlegar áfyllingarpantanir, er hægt að færa línurnar inn í reikninginn með því að velja aðgerðina **Ítrekaðar innkaupalínur**.
4. **Á fastflipanum línur** í **reitnum Vörunr.** er fært inn númer birgðavöru eða þjónustu.
5. Í reitinn **Magn** er fært fjöldi vara sem á að kaupa.

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **beint innkaupsverð** margfaldað með gildinu í reitnum **magn**.

    Verð og Línuupphæð er sýnd með eða án virðisaukaskatts eftir því hvað var valið í **svæðinu verð er með skattsvæði** á lánardrottnaspjaldinu.

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

6. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti** neðst á reikningnum.

    > [!NOTE]  
    > Ef settur hefur verið upp reikningsafsláttur fyrir lánardrottinn þá er tilgreint prósentugildið sjálfkrafa sett inn í **reitinn reikningsafsláttur Lánardrottinsafsláttar** ef skilyrðin eru uppfyllt. Tengd upphæð er sett inn í **reitinn Upphæð** reikningsafsláttar.
7. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðum, forðabókum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.  

> [!NOTE]
> Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er vanalega vegna sléttunarútreikninga í tengslum við virðisauka (VAT) eða virðisaukaskatt.
>
> Til að kanna upphæðirnar sem í raun verður bókað er farið á **upplýsingasíðuna**, sem tekur sléttunar útreikninga með í reikninginn. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.

## <a name="when-to-use-purchase-orders"></a>Hvenær á að nota innkaupapantanir

Nota verður innkaupapantanir ef innkaupaferliferlið krefst þess að notandi skrái hluta af pöntunarmagni, til dæmis, þar sem fullt magn er ekki tiltækt hjá lánardrottni. Ef seldar vörur eru afhendar beint frá lánardrottni til viðskiptavinar sem bein afhending þarf einnig að nota innkaupapantanir. Frekari upplýsingar er að gera í [beinni afhendingu](sales-how-drop-shipment.md).

Í öllum öðrum þáttum vinnur innkaupapöntunum það sama og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="purchasing-non-inventory-items"></a>Kaup á vörum sem ekki eru í birgðum

Línurnar á innkaupareikningi geta verið af **forðagerð** eða **vöru**. Hægt er að flokka birgðaspjöld jafnt fyrir birgðir **,** þjónustu **eða** **tegund af** gerðinni sem ekki eru í birgðum, sem tilgreinir hvort varan sé raunbirgðaeining, vinnutímaeining (á einnig við um forða), eða efnislega einingu sem ekki er geymd í birgðum. Lærðu meira á að [skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningur ferlisins er sá sami fyrir allar framangreindar gerðir.

> [!NOTE]
> Með innkaupalínugerðinni **Tilfang** er einnig hægt að kaupa ytri tilföng, til dæmis til að senda reikning á lánardrottin fyrir afhenta vinnu. Frekari upplýsingar um [uppsetningu forða](projects-how-setup-resources.md).
>
> Til að nota keypt tilfang getur þurft að stilla afkastagetu tilfangs og tengja það handvirkt við verk. Innkaupatilfang stofnar forðafærslu; forðafærslur eru hins vegar ekki raktar fyrir magn og gildi eins og til dæmis vörur eru. Ef rakning á magni og virði er nauðsynlegt, skal íhuga að nota aðrar vörulínugerðir.

## <a name="posted-invoices"></a>Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt ef leiðrétta þarf innsláttarmistök eða breyta innkaupum snemma í pöntunarferlinu. Frekari upplýsingar við rétt eða hætta á [ógreiddum innkaupareikningum](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Ef þú hefur þegar greitt fyrir vörur eða þjónustu á bókaða innkaupareikningnum þá þarf að stofna innkaupakreditreikning til að bakfæra innkaupin. Frekari upplýsingar í [vinnslu Kaupskilum eða afturköllunum](purchasing-how-process-purchase-returns-cancellations.md).

[Opnaðu **Bókaðir innkaupareikningar** listann ](https://businesscentral.dynamics.com/?page=146) í [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index).

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
