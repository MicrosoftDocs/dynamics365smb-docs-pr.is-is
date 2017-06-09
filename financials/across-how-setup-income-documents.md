---
title: "Hvernig á að: Setja upp skjöl á innleið | Microsoft Docs"
description: "Hvernig á að: Setja upp skjöl á innleið"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: be99b334117c2e0cb7fe989ecc87dcf71a1d765d
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-incoming-documents"></a>Hvernig á að: Setja upp skjöl á innleið
Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í í glugganum **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.

Ef notendur eiga ekki að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt verður að setja upp samþykkjendur í glugganum **Samþykkjendur skjala á innleið**.

Til að breyta PDF og myndaskrám í rafræn skjöl sem er hægt að breyta í til dæmis innkaupareikninga innan [!INCLUDE[d365fin](includes/d365fin_md.md)], verður að fyrst að setja upp eiginleikann OCR og virkja þjónustuna.

Þegar eiginleikinn Skjöl á innleið er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til. Nánari upplýsingar er að finna í [Vinna skjöl á innleið](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Setja upp valkostinn fyrir skjal á innleið
1. Efst í hægra horni skal velja táknið fyrir **Leit að síðu eða skýrslu** táknið fyrir ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "táknið fyrir Leit að síðu eða skýrslu táknið"), slá inn **Uppsetning á skjali á innleið**, og velja síðan viðeigandi tengil.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Að setja upp samþykkjendur fyrir skjöl á innleið
1. Efst í hægra horni skal velja táknið fyrir **Leit að síðu eða skýrslu** táknið fyrir ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "táknið fyrir Leit að síðu eða skýrslu táknið"), slá inn **Uppsetning á skjali á innleið**, og velja síðan viðeigandi tengil.  
2. Í glugganum **Skjal á innleið** skal velja aðgerðina **Samþykkjendur**

    Glugginn **Samþykkjendur skjala á innleið** sýnir alla notendur sem hafa verið settir upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Veldu einn eða fleiri notendur sem geta samþykkt innsent skjal áður en hægt er að stofna fylgiskjals - eða bókarlínu.

Þegar samþykkjendur hafa verið settir upp í glugganum **Samþykkjendur skjala á innleið ** geta aðeins þessir notendur samþykkt skjal á innleið ef gátreitur **Krefjast samþykkis fyrir stofnun** í glugganum **uppsetning skjala á innleið** er valinn.

**Athugasemd**: þessi uppsetning samþykkis er ekki tengt samþykktarverkflæðum. Nánari upplýsingar sjá [hvernig á að: nota Samþykkisverkflæði](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Til að setja upp OCR-þjónustu
1. Efst í hægra horni skal velja táknið fyrir **Leit að síðu eða skýrslu** táknið fyrir ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "táknið fyrir Leit að síðu eða skýrslu táknið"), slá inn **Uppsetning á OCR-þjónustu**, og velja síðan viðeigandi tengil.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>Til að dulrita innskráningarupplýsingar
Mælt er með því að vernda innskráningarupplýsingar sem slegnar eru inn í **uppsetning OCR-þjónustu** gluggann. Hægt er að dulrita gögn á  netþjóninum með því að stofna nýjan dulritunarlykil eða flytja inn fyrirliggjandi lykla sem eru virkjaðir er á netþjónstilviki sem tengist við gagnagrunninn.

1. Í **uppsetning fyrir OCR-þjónusta ** glugganum, veldu **stjórnun dulritunar**.
2.  Í glugganum **gagnadulritun**, virkja dulritun gagnanna.

## <a name="see-also"></a>Sjá einnig
[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

