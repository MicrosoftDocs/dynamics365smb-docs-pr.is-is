---
title: "Leita að skjölum án viðhengja| Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8219b8a054901f81785ef1376c6f86763560cc31
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-find-posted-documents-without-incoming-document-records"></a>Hvernig á að: Finna bókuð fylgiskjöl án færslu skjals á innleið
Úr gluggunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa- og söluskjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Hvernig á að finna bókuð fylgiskjöl án færslu skjals á innleið
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.
2. Veljið línu fyrir þann fjárhagsreikning þar sem skoða á fjárhagsfærslur og bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið og veljið síðan **bókuð skjöl án skjal á innleið**
3. Einnig, Valið er **fjárhagsfærslur** aðgerð.
4. Í glugganum **fjárhagsfærslur**, veljið aðgerðina **bókuð skjöl án skjala á innleið**.

Glugginn **Bókuð fylgiskjöl án skjals á innleið** opnast og hann sýnir bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið sem tengjast fjárhagsfærslum á fjárhagsreikningi sem gluggninn var opnaður fyrir. Glugginn getur birt mest 1000 línur í einu. Sjálfgefið inniheldur reiturinn **dagsetningarafmörkun** því síu sem takmarkar línurnar við færslur með bókunardagsetningum frá upphafi bókhaldstímabils til vinnudagsetningar.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Til að tengja fundin skjöl við fyrirliggjandi færslur skjala á innleið
1. Í glugganum **Bókuð fylgiskjöl án skjals á innleið** skal velja línu fyrir bókað skjal sem á að tengja við fyrirliggjandi færslu skjals á innleið, og veljið svo aðgerðina velja **skjal á innleið**.
2. Í **skjal á innleið** glugganum skal velja færslu fyrir skjal á innleið sem tengja á við bókað skjal sem fannst og velja svo hnappinn **Í lagi**.
3. Í glugganum **Bókuð fylgiskjöl án skjals á innleið** er valin færsla skjals á innleið nú tengt við bókaða skjalið, eins og sjá má í upplýsingakassanum **skrár fyrir skjal á innleið**.

Ef viðkomandi færsla skjals á innleið er ekki til í glugganum **skjal á innleið** er hægt að stofna hana. Frekari upplýsingar eru í [Hvernig á að stofna færslur fyrir skjal á innleið ](across-how-create-income-document-records.md).

## <a name="see-also"></a>Sjá einnig
[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

