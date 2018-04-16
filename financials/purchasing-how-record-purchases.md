---
title: "Stofna innkaupareikning og skrá innkaup | Microsoft Docs"
description: "Lýst hvernig á að kaupa birgðir og þjónustuvörur með því að stofna og bóka innkaupareikninga eða -pantanir."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3228d82190e81198817d0e1fa5c86f6c9d0f784f
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="record-purchases"></a>Skrá innkaup
Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Ef stjórna þarf birgðum eru innkaupareikningar og innkaupapantanir líka notaðir til að uppfæra birgðastig gagnvirkt svo að hægt sé að lágmarka birgðakostnað og veita betri þjónustu við viðskiptavini. Innkaupakostnaður, að þjónustukostnaði meðtöldum, og birgðavirði af völdum bókunar innkaupareikninga eða -pantana verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í Mitt hlutverk.

> [!NOTE]  
>   Verður Að nota innkaupapantanir ef innkaupaferlið krefst þess að hægt sé að skrá hlutamóttökur pöntunarmagns , til dæmis þar sem allt magnið var ekki tiltæk í hjá lánardrottinn. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka innkaupapantanir á sama hátt og innkaupareikningar. Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir innkaupapöntun.

Þegar þú tekur við birgðavörum eða þegar innkaupaaðgerð er lokið bókarðu innkaupareikninginn eða -pöntun til að uppfæra birgðir og fjármálaskrár og til að virkja greiðslu til lánardrottins, samkvæmt greiðsluskilmálum. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).

> [!CAUTION]  
>   Ekki bóka innkaupareikning fyrr en vörur eru mótteknar og lokakostnaður er vitaður, þ.m.t. öll viðbótargjöld. Annars kunna birgðagildi og hagnaðartölur er vera röng.

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning áður en lánardrottinn fær greitt. Þetta er gagnlegt þegar leiðrétta á innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu. Nánari upplýsingar er að finna [Ógreiddir innkaupareikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Ef þegar hefur verið greitt fyrir vörur á bókuðum innkaupareikningi, þá verður að búa til innkaupakreditreikning til að snúa við innkaupunum. Nánari upplýsingar er að finna í [Vinna úr innkaupaskilum eða afturköllunum](purchasing-how-process-purchase-returns-cancellations.md).

Vörurnar geta verið tegund **Birgðir** eða **Þjónustu**. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md). Innkaupareikningaferlið er það sama fyrir báðar vörutegundir.

Hægt er að fylla út  lánardrottnareitina í innkaupareikningunum með tveimur leiðum, eftir því hvort lánardrottinninn hefur þegar verið skráður.

## <a name="to-create-a-purchase-invoice"></a>Að Stofna innkaupareikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.  
2. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.

    Aðrir reitir í glugganum **innkaupareikningur** eru nú fylltir út með stöðluðum upplýsingum um lánardrottinn sem valinn hefur verið. Ef lánardrottinn er ekki skráður, fylgið eftirfarandi skrefum:
3. Í reitnum **lánardrottinn** er fært inn nafn nýs lánardrottinn.
4. Í svarglugganum um að skrá nýja lánardrottinn, veljið hnappinn **Já**.
5. Í glugganum **Velja sniðmát fyrir nýjan lánardrottinn**, skal velja sniðmát til að byggja nýja lánardrottnaspjaldið á og veljið hnappinn **Í lagi**.
6. Nýtt viðskiptamannaspjald opnast, fyrirfram fyllt út með upplýsingnum á valda viðskiptamannasniðmátinu. Reiturinn **Heiti** er fyrirfram fylltur út með nafni nýja lánardrottinsins sem fært var inn á innkaupareikninginn.
7. Haltu áfram að fylla út eftirstandandi reiti á spjaldi lánardrottins. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).  
8. Þegar lokið hefur verið við lánardrottinsspjaldið skal velja hnappinn **Í lagi** til að fara aftur í gluggann **Innkaupareikningur**.

    Margir reitir í glugganum **innkaupareikningur** eru útfylltir með upplýsingar sem tilgreindar eru á nýju lánardrottinnspjaldi.
9. Fylltu í eftirstandandi reiti í glugganum **innkaupareikningur** eftir þörfum. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Þú ert nú tilbúinn að fylla út innkaupareikningslínurnar með birgðavöru eða þjónustu þú hefur keypt af lánardrottninum.

    > [!NOTE]  
   >   Ef endurteknar innkaupalínur hafa verið settar upp fyrir lánardrottinn, svo sem mánaðarlegar áfyllingarpantanir, er hægt að færa línurnar inn í reikninginn með því að velja aðgerðina **Ítrekaðar innkaupalínur**.
10. Í flýtiflipanum **Línur** í reitnum **Vörunúmer** er sleginn inn fjöldi birgðavöru eða þjónustu.
11. Í reitinn **Magn** er fært fjöldi vara sem á að kaupa.

    > [!NOTE]  
    >   Fyrir vörur af tegundinni **Þjónusta** er magnið tímaeining, t.d. klukkutímar, eins og gefið er til kynna í reitnum **Mælieiningarkóði** í línunni

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **beint innkaupsverð** margfaldað með gildinu í reitnum **magn**.

    Verð- og línuupphæð eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á lánardrottinsspjaldinu.
12. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti** neðst á reikningnum.

    > [!NOTE]  
    >   Ef reikningsafslættir hafa verið settir upp fyrir lánardrottinn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur % lánardrottins** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð reiknings**.
13. Þegar tekið er við innkeyptar vörur eða þjónustu velja **Bóka**.

Innkaupin eru nú skráð í birgðafærslum og fjármálafærslum og greiðsla lánardrottins er virkjuð. Innkaupareikningurinn er fjarlægður af lista innkaupareikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupareikninga.

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Biðja um tilboð](purchasing-how-request-quotes.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Undirbúa beina sendingu](sales-how-drop-shipment.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

